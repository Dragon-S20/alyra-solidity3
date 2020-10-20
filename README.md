# alyra-solidity3

## FirstErc20.sol

Ajouter une fonction cap()qui retournera le maximum de tokens qui pourront être créés.

## FirstErc20.sol

Ajouter une fonction burn qui prend en paramètre une addresse et une quantité de tokens, et qui détruira cette quantité de tokens reduisant ainsi le nombre de tokens en circulation. Cette fonction ne pourra être appelée que par l'owner du smart contract.

## FirstErc20.sol

Afin d'ajouter de la gouvernance, créer un mapping(address => bool) admins; Ce mapping contiendra tous les administrateurs du smart contracts. Leur adresse sera mappée à true dans le mapping.

Désormais les fonctions de mint et burn ne pourront être appelées que par un admin.
Ajouter une fonction addAdmin(address \_account) et delAdmin(address \_account) qui ne pourront être appelées que par un administrateur.
Ces fonctions permettront d'ajouter ou d'enlever un admin du mapping.

Au déploiement du contrat, il faudra absolument définir l'adresse qui déploie le smart contrat comme un admin.

Il faudra remplacer le modifier onlyOwner par onlyAdmin.

## FirstIco.sol

Ajouter la fonction receive qui transférera au sender le nombre de token en fonction du nombre d'ethers envoyés. Les ethers seront toujours transférés à l'adresse de l'owner qui a déployé le contrat. Les tokens seront toujours transférés depuis \_seller vers l'acheteur. Il faudra donc que l'adresse du \_seller approve l'adresse du smart contract FirstIco.
