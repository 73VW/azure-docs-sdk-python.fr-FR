---
title: Bibliothèques Redis Azure pour Python
description: Consulter la documentation sur les bibliothèques de client Python pour Redis
keywords: Azure, Python, Redis, API, Kit de développement logiciel (SDK), base de données, NoSQL
author: sptramer
ms.author: sttramer
manager: douge
ms.date: 06/26/2017
ms.topic: article
ms.devlang: python
ms.service: redis
ms.openlocfilehash: c2f8ebcbcbd7b71c1fa96e46a8148a3c0b88877f
ms.sourcegitcommit: 41e90fe75de03d397079a276cdb388305290e27e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/23/2018
ms.locfileid: "29479242"
---
# <a name="azure-redis-cache-libraries-for-python"></a>Bibliothèques Cache Redis Azure pour Python

## <a name="overview"></a>Vue d'ensemble

Le Cache Redis Azure se base sur le projet Redis open source connu. Il vous permet d’accéder à une instance Redis sécurisée et dédiée, gérée par Microsoft et accessible depuis vos applications Azure.

Redis est un stockage clé/valeur avancé, dont les clés peuvent contenir des structures de données telles que des chaînes, des hachages, des listes, des groupes et des groupes triés. Redis prend en charge un ensemble d'opérations atomiques pour ces types de données.

En savoir plus sur le [Cache Redis Azure](https://docs.microsoft.com/azure/redis-cache/).

## <a name="management-api"></a>API de gestion

Créez et gérez vos ressources Redis dans votre abonnement avec l’API de gestion de Redis.

```bash
pip install redis
pip install azure-mgmt-redis
```

### <a name="example"></a>exemples

L’exemple suivant crée un Cache Redis :

```python
from azure.mgmt.redis import RedisManagementClient
from azure.mgmt.redis.models import Sku, RedisCreateOrUpdateParameters

redis_client = RedisManagementClient(
    credentials,
    subscription_id
)
group_name = 'myresourcegroup'
cache_name = 'mycachename'
redis_cache = redis_client.redis.create_or_update(
    group_name,
    cache_name,
    RedisCreateOrUpdateParameters(
        sku = Sku(name = 'Basic', family = 'C', capacity = '1'),
        location = "East US"
    )
)
# redis_cache is a RedisResourceWithAccessKey instance
```

> [!div class="nextstepaction"]
> [Explorer les API de gestion](/python/api/overview/azure/redis/management)

