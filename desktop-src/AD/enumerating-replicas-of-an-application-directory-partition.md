---
title: Enumeración de réplicas de una partición de directorio de aplicación
description: En este tema se muestra cómo enumerar las réplicas de una partición de directorio de aplicación.
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- Enumeración de réplicas de una partición de directorio de aplicación de AD
- Application Directory Partitions AD , Enumerating Replicas of
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52ff0ea5c2b4737079f4a44997f39dd027299f50c8acd96fe0456b0e5b60d03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694892"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>Enumeración de réplicas de una partición de directorio de aplicación

Cuando se agrega una réplica de una partición de directorio de aplicación, el nombre distintivo del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para el controlador de dominio que contendrá la réplica se agrega al atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto [**crossRef.**](/windows/desktop/ADSchema/c-crossref) El **objeto crossRef** utilizado representa la partición del directorio de la aplicación.

**Para enumerar las réplicas de una partición de directorio de aplicación**

1.  Busque en el contenedor Partitions un [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) que tenga un valor de atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) que sea igual al nombre distintivo de la partición del directorio de la aplicación.
2.  Use cada valor del atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) para enlazar con el objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del servidor.
3.  Obtenga el ADsPath para el elemento primario de cada [**objeto nTDSDSA.**](/windows/desktop/ADSchema/c-ntdsdsa) Se trata de un objeto que representa el servidor del controlador de dominio. Use ADsPath para enlazar con el objeto de servidor.
4.  Obtenga el [**valor del atributo dNSHostName**](/windows/desktop/ADSchema/a-dnshostname) del objeto de servidor. Se trata de una propiedad de un solo valor que contiene el nombre DNS del servidor.

Debido a la latencia de replicación y a los retrasos de ejecución de KCC programados, es posible que las réplicas activas reales de una partición de directorio de aplicación no coincidan con la lista de controladores de dominio indicados por el atributo [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto [**crossRef.**](/windows/desktop/ADSchema/c-crossref) Una manera más precisa, pero menos eficaz de determinar las réplicas activas reales de una partición de directorio de aplicación es buscar todos los objetos [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del bosque que tengan un atributo [**msDS-hasMasterNCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) que contenga el nombre distintivo de la partición del directorio de la aplicación. El **atributo msDS-hasMasterNCs** contiene los nombres distintivos de todas las particiones de directorio grabables que hospeda el controlador de dominio, incluidas las particiones del directorio de la aplicación.

 

 