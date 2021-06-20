---
title: Enumeración de grupos que contienen muchos miembros
description: Obtenga información sobre cómo enumerar Azure Active Directory que contienen muchos miembros mediante la recuperación incremental de datos (recuperación de intervalos).
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Enumeración de grupos que contienen muchos miembros Active Directory
- grupos Active Directory , enumerando grupos con muchos miembros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7cab63b809fdbd2666f39a09d32f601346da00e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405158"
---
# <a name="enumerating-groups-that-contain-many-members"></a>Enumeración de grupos que contienen muchos miembros

Los miembros de un grupo se almacenan en un atributo de varios valores denominado **miembro**. El **atributo** miembro puede contener un gran número de valores. La enumeración de miembros puede ser ineficaz cuando el número de valores de un atributo con varios valores se vuelve grande. El servidor también limitará el número máximo de valores que se pueden recuperar en una sola consulta. Esto significa que si un grupo puede tener más miembros de los que puede proporcionar el servidor, la única manera de enumerar todos los miembros es usar la recuperación incremental de datos, conocida como recuperación de *intervalos.*

La recuperación de intervalos implica solicitar un número limitado de valores de atributo en una sola consulta. El número de valores solicitados debe ser menor o igual que el número máximo de valores admitidos por el servidor. Para reducir el número de veces que la consulta debe ponerse en contacto con el servidor, el número de valores solicitados debe ser lo más cercano posible a este máximo. Para permitir que una aplicación funcione correctamente con todos los servidores, se debe usar un número máximo de 1000.

La versión del servidor que proporciona los datos solicitados determina el número máximo de valores que se pueden recuperar en una sola consulta. En la tabla siguiente se muestra la versión del servidor y el número máximo de valores que se pueden recuperar en una sola consulta.



| Versión del sistema operativo del servidor | Valores máximos recuperados |
|---------------------------------|--------------------------|
| Windows 2000                    | 1000                     |
| Windows Server 2003             | 1.500                     |



 

Para obtener más información sobre cómo recuperar intervalos de valores de atributo con ADSI, vea [Recuperación de intervalos de atributos.](/windows/desktop/ADSI/attribute-range-retrieval)

Para obtener más información sobre cómo recuperar intervalos de valores de atributo [con System.DirectoryServices](/dotnet/api/system.directoryservices), vea [Enumerar miembros en un grupo grande.](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx)

 

 