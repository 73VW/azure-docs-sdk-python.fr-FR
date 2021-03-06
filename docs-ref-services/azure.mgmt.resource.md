---
title: Bibliothèques de ressources Azure pour Python
description: ''
keywords: Azure, Python, Kit de développement logiciel (SDK), API, ressources
author: lisawong19
ms.author: liwong
manager: douge
ms.date: 06/19/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: python
ms.service: resources
ms.openlocfilehash: 32e13bee27db091f0bca12c7d9ae4fc62165f4c0
ms.sourcegitcommit: 3617d0db0111bbc00072ff8161de2d76606ce0ea
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/18/2017
ms.locfileid: "20909392"
---
# <a name="azure-resources-libraries-for-python"></a>Bibliothèques de ressources Azure pour Python 

## <a name="overview"></a>Vue d'ensemble 
Gérez des ressources Azure dans des groupes de ressources.

| Package  |  Description |
|---|---|
|[azure.mgmt.resource.features][1]|Le contrôle d’exposition aux fonctionnalités d’Azure (AFEC) fournit un mécanisme permettant aux fournisseurs de ressources de contrôler l’exposition aux fonctionnalités des utilisateurs.|
|[azure.mgmt.resource.links][2]|Les ressources Azure peuvent être liées pour établir des relations logiques. Vous pouvez établir des liens entre les ressources de différents groupes de ressources.|
|[azure.mgmt.resource.locks][3]|Les ressources Azure peuvent être verrouillées pour empêcher les autres utilisateurs de votre organisation de supprimer ou modifier des ressources.|
|[azure.mgmt.resource.managedapplications][4]|Applications gérées ARM (appliances).|
|[azure.mgmt.resource.policy][5]|Pour gérer et contrôler l’accès à vos ressources, vous pouvez définir des stratégies personnalisées et leurs portées.|
|[azure.mgmt.resource.resources][6]| Fournit des opérations utiliser des ressources et des groupes de ressources.|
|[azure.mgmt.resource.subscriptions][7]|Tous les groupes de ressources et les ressources existent dans les abonnements. Ces opérations vous permettent d’obtenir des informations sur vos abonnements et vos clients.|

[1]: /python/api/azure.mgmt.resource.features
[2]: /python/api/azure.mgmt.resource.links
[3]: /python/api/azure.mgmt.resource.locks
[4]: /python/api/azure.mgmt.resource.managedapplications
[5]: /python/api/azure.mgmt.resource.policy
[6]: /python/api/azure.mgmt.resource.resources
[7]: /python/api/azure.mgmt.resource.subscriptions

## <a name="install-the-libraries"></a>Installer les bibliothèques 
```bash
pip install azure-mgmt-resource
```

## <a name="example"></a>Exemple
L’exemple suivant montre comment créer un groupe de ressources. 

```python
from azure.mgmt.resource import ResourceManagementClient
client = ResourceManagementClient(credentials, subscription_id)
client.resource_groups.create(RESOURCE_GROUP_NAME, {'location':'eastus'})
```

Découvrez d’autres [exemples de code Python](https://azure.microsoft.com/resources/samples/?platform=python) à utiliser dans vos applications. 