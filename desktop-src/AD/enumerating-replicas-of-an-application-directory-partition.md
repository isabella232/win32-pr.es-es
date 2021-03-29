---
title: Enumerar réplicas de una partición de directorio de aplicaciones
description: En este tema se muestra cómo enumerar las réplicas de una partición de directorio de aplicaciones.
ms.assetid: a1d6865b-ec77-4687-9da7-7fc717568bda
ms.tgt_platform: multiple
keywords:
- Enumerar réplicas de una partición de directorio de aplicaciones AD
- Particiones de directorio de aplicaciones AD, enumerar réplicas de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1415c147fe4320e5f8169487a656db4f365f03a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995093"
---
# <a name="enumerating-replicas-of-an-application-directory-partition"></a>Enumerar réplicas de una partición de directorio de aplicaciones

Cuando se agrega una réplica de una partición de directorio de aplicaciones, se agrega el nombre distintivo del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para el controlador de dominio que contendrá la réplica al atributo [**MSDS-NC-Replica-locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) . El objeto **crossRef** utilizado representa la partición del directorio de aplicaciones.

**Para enumerar las réplicas de una partición de directorio de aplicaciones**

1.  Busque en el contenedor de particiones un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) que tenga un valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) que sea igual al nombre distintivo de la partición de directorio de aplicaciones.
2.  Use cada valor del atributo [**MSDS-NC-Replica-locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) para enlazar con el objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del servidor.
3.  Obtenga el ADsPath para el elemento primario de cada objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) . Se trata de un objeto que representa el servidor de controlador de dominio. Use el ADsPath para enlazar con el objeto de servidor.
4.  Obtenga el valor del atributo [**DnsHostName**](/windows/desktop/ADSchema/a-dnshostname) del objeto de servidor. Se trata de una propiedad de un solo valor que contiene el nombre DNS del servidor.

Debido a la latencia de replicación y a los retrasos programados de KCC, es posible que las réplicas activas reales de una partición de directorio de aplicaciones no coincidan con la lista de controladores de dominio indicados por el atributo [**MSDS-NC-Replica-locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) . Una forma más precisa, pero menos eficaz de determinar las réplicas activas reales de una partición de directorio de aplicaciones es buscar todos los objetos [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del bosque que tienen un atributo [**MSDS-hasMasterNCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) que contiene el nombre distintivo de la partición de directorio de aplicaciones. El atributo **MSDS-hasMasterNCs** contiene los nombres distintivos de todas las particiones de directorio de escritura que hospeda el controlador de dominio, incluidas las particiones de directorio de aplicaciones.

 

 