# seal-profile

Bitcoin L1 single-use seal profile for a hardware deed and a sovereign-agent control seal.

This is not The Gem. The Gem record is a design ledger and is not a chain.

The contract id is the thing. The unspent seal is the controller. A right moves only when that seal closes.

## Scripts

- `hwdeed_regtest.py` — in-process hardware deed: tagged commitments, witness threshold, seal close.
- `agent_seal_regtest.py` — agent rules: pure rotation, witness on mint, cold sweep burns the right, confirmed close wins.
- `operator_cold_leaf.py` — operator wallet check that a rotation still commits to the genesis cold leaf.
- `agent_regtest_rpc.py` — Bitcoin Core regtest sequence. `--dry-run` builds the transactions. Live mode needs a local regtest node.

Signatures in the in-process scripts are stand-ins. The RPC script uses BIP-340 Schnorr via embit. The script-path spend has not been accepted by a node in the environment that produced it.

## License

MIT
