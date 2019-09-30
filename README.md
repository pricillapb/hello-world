
import Web3 from 'web3';


let web3;
if (typeof window !== 'undefined' && typeof window.web3 !== 'undefined') {
  // we check if metamask is running
  web3 = new Web3(window.web3.currentProvider);
} else {
  // set up provider through infura
  const provider = new Web3.providers.HttpProvider(
    // pass url of remote node
    'rinkeby infura link that you receive after signing up'
  );
  web3 = new Web3(provider);

}

export default web3;
