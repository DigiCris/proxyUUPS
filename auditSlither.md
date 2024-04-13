Summary
 - [unused-return](#unused-return) (2 results) (Medium)
 - [assembly](#assembly) (10 results) (Informational)
 - [dead-code](#dead-code) (18 results) (Informational)
 - [solc-version](#solc-version) (1 results) (Informational)
 - [low-level-calls](#low-level-calls) (4 results) (Informational)
## unused-return
Impact: Medium
Confidence: Medium
 - [ ] ID-0
[ERC1967Utils.upgradeToAndCall(address,bytes)](proxy.sol#L398-L407) ignores return value by [Address.functionDelegateCall(newImplementation,data)](proxy.sol#L403)

proxy.sol#L398-L407


 - [ ] ID-1
[ERC1967Utils.upgradeBeaconToAndCall(address,bytes)](proxy.sol#L488-L497) ignores return value by [Address.functionDelegateCall(IBeacon(newBeacon).implementation(),data)](proxy.sol#L493)

proxy.sol#L488-L497


## assembly
Impact: Informational
Confidence: High
 - [ ] ID-2
[StorageSlot.getBytes32Slot(bytes32)](proxy.sol#L76-L81) uses assembly
	- [INLINE ASM](proxy.sol#L78-L80)

proxy.sol#L76-L81


 - [ ] ID-3
[StorageSlot.getBytesSlot(bytes32)](proxy.sol#L116-L121) uses assembly
	- [INLINE ASM](proxy.sol#L118-L120)

proxy.sol#L116-L121


 - [ ] ID-4
[Proxy._delegate(address)](proxy.sol#L533-L556) uses assembly
	- [INLINE ASM](proxy.sol#L534-L555)

proxy.sol#L533-L556


 - [ ] ID-5
[StorageSlot.getStringSlot(string)](proxy.sol#L106-L111) uses assembly
	- [INLINE ASM](proxy.sol#L108-L110)

proxy.sol#L106-L111


 - [ ] ID-6
[Address._revert(bytes)](proxy.sol#L281-L293) uses assembly
	- [INLINE ASM](proxy.sol#L286-L289)

proxy.sol#L281-L293


 - [ ] ID-7
[StorageSlot.getUint256Slot(bytes32)](proxy.sol#L86-L91) uses assembly
	- [INLINE ASM](proxy.sol#L88-L90)

proxy.sol#L86-L91


 - [ ] ID-8
[StorageSlot.getAddressSlot(bytes32)](proxy.sol#L56-L61) uses assembly
	- [INLINE ASM](proxy.sol#L58-L60)

proxy.sol#L56-L61


 - [ ] ID-9
[StorageSlot.getStringSlot(bytes32)](proxy.sol#L96-L101) uses assembly
	- [INLINE ASM](proxy.sol#L98-L100)

proxy.sol#L96-L101


 - [ ] ID-10
[StorageSlot.getBooleanSlot(bytes32)](proxy.sol#L66-L71) uses assembly
	- [INLINE ASM](proxy.sol#L68-L70)

proxy.sol#L66-L71


 - [ ] ID-11
[StorageSlot.getBytesSlot(bytes)](proxy.sol#L126-L131) uses assembly
	- [INLINE ASM](proxy.sol#L128-L130)

proxy.sol#L126-L131


## dead-code
Impact: Informational
Confidence: Medium
 - [ ] ID-12
[ERC1967Utils._setAdmin(address)](proxy.sol#L430-L435) is never used and should be removed

proxy.sol#L430-L435


 - [ ] ID-13
[StorageSlot.getBytesSlot(bytes)](proxy.sol#L126-L131) is never used and should be removed

proxy.sol#L126-L131


 - [ ] ID-14
[Address.sendValue(address,uint256)](proxy.sol#L176-L185) is never used and should be removed

proxy.sol#L176-L185


 - [ ] ID-15
[Address.functionCallWithValue(address,bytes,uint256)](proxy.sol#L218-L224) is never used and should be removed

proxy.sol#L218-L224


 - [ ] ID-16
[StorageSlot.getUint256Slot(bytes32)](proxy.sol#L86-L91) is never used and should be removed

proxy.sol#L86-L91


 - [ ] ID-17
[ERC1967Utils.upgradeBeaconToAndCall(address,bytes)](proxy.sol#L488-L497) is never used and should be removed

proxy.sol#L488-L497


 - [ ] ID-18
[StorageSlot.getStringSlot(bytes32)](proxy.sol#L96-L101) is never used and should be removed

proxy.sol#L96-L101


 - [ ] ID-19
[ERC1967Utils.getAdmin()](proxy.sol#L423-L425) is never used and should be removed

proxy.sol#L423-L425


 - [ ] ID-20
[ERC1967Utils.getBeacon()](proxy.sol#L457-L459) is never used and should be removed

proxy.sol#L457-L459


 - [ ] ID-21
[ERC1967Utils._setBeacon(address)](proxy.sol#L464-L475) is never used and should be removed

proxy.sol#L464-L475


 - [ ] ID-22
[Address.functionStaticCall(address,bytes)](proxy.sol#L230-L233) is never used and should be removed

proxy.sol#L230-L233


 - [ ] ID-23
[ERC1967Utils.changeAdmin(address)](proxy.sol#L442-L445) is never used and should be removed

proxy.sol#L442-L445


 - [ ] ID-24
[StorageSlot.getStringSlot(string)](proxy.sol#L106-L111) is never used and should be removed

proxy.sol#L106-L111


 - [ ] ID-25
[StorageSlot.getBooleanSlot(bytes32)](proxy.sol#L66-L71) is never used and should be removed

proxy.sol#L66-L71


 - [ ] ID-26
[StorageSlot.getBytes32Slot(bytes32)](proxy.sol#L76-L81) is never used and should be removed

proxy.sol#L76-L81


 - [ ] ID-27
[Address.verifyCallResult(bool,bytes)](proxy.sol#L270-L276) is never used and should be removed

proxy.sol#L270-L276


 - [ ] ID-28
[StorageSlot.getBytesSlot(bytes32)](proxy.sol#L116-L121) is never used and should be removed

proxy.sol#L116-L121


 - [ ] ID-29
[Address.functionCall(address,bytes)](proxy.sol#L205-L207) is never used and should be removed

proxy.sol#L205-L207


## solc-version
Impact: Informational
Confidence: High
 - [ ] ID-30
Version constraint ^0.8.20 contains known severe issues (https://solidity.readthedocs.io/en/latest/bugs.html)
	- VerbatimInvalidDeduplication (Not using yul optimizer)
	- FullInlinerNonExpressionSplitArgumentEvaluationOrder (version > 0.8.21)
	- MissingSideEffectsOnSelectorAccess. (version > 0.8.21)
 It is used by:
	- proxy.sol#2
	- proxy.sol#139
	- proxy.sol#301
	- proxy.sol#320
	- proxy.sol#515
	- proxy.sol#587

## low-level-calls
Impact: Informational
Confidence: High
 - [ ] ID-31
Low level call in [Address.functionCallWithValue(address,bytes,uint256)](proxy.sol#L218-L224):
	- [(success,returndata) = target.call{value: value}(data)](proxy.sol#L222)

proxy.sol#L218-L224


 - [ ] ID-32
Low level call in [Address.sendValue(address,uint256)](proxy.sol#L176-L185):
	- [(success,None) = recipient.call{value: amount}()](proxy.sol#L181)

proxy.sol#L176-L185


 - [ ] ID-33
Low level call in [Address.functionStaticCall(address,bytes)](proxy.sol#L230-L233):
	- [(success,returndata) = target.staticcall(data)](proxy.sol#L231)

proxy.sol#L230-L233


 - [ ] ID-34
Low level call in [Address.functionDelegateCall(address,bytes)](proxy.sol#L239-L242):
	- [(success,returndata) = target.delegatecall(data)](proxy.sol#L240)

proxy.sol#L239-L242


