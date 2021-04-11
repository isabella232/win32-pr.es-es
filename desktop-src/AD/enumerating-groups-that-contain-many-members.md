---
title: Enumerar grupos que contienen muchos miembros
description: Los miembros de un grupo se almacenan en un atributo de varios valores denominado Member.
ms.assetid: 78f81b09-2223-4b74-b8d5-7a97494c0324
ms.tgt_platform: multiple
keywords:
- Enumerar grupos que contienen muchos miembros Active Directory
- grupos Active Directory, enumerar grupos con muchos miembros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe2d9a5c9abc6e77ac72672379789d1028f92c3f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149180"
---
# <a name="enumerating-groups-that-contain-many-members"></a>Enumerar grupos que contienen muchos miembros

Los miembros de un grupo se almacenan en un atributo de varios valores denominado **member**. El atributo de **miembro** puede contener un gran número de valores. La enumeración de miembros puede ser ineficaz cuando el número de valores de un atributo con varios valores llega a ser grande. El servidor también limitará el número máximo de valores que se pueden recuperar en una sola consulta. Esto significa que si un grupo puede tener más miembros de los que puede proporcionar el servidor, la única manera de enumerar todos los miembros es usar la recuperación incremental de los datos, lo que se conoce como *recuperación de intervalo*.

La recuperación por rangos implica solicitar un número limitado de valores de atributo en una sola consulta. El número de valores solicitados debe ser menor o igual que el número máximo de valores admitidos por el servidor. Para reducir el número de veces que la consulta debe ponerse en contacto con el servidor, el número de valores solicitados debe ser lo más cercano posible a este máximo. Para permitir que una aplicación funcione correctamente con todos los servidores, debe usarse un número máximo de 1000.

La versión del servidor que proporciona los datos solicitados determina el número máximo de valores que se pueden recuperar en una sola consulta. En la tabla siguiente se muestra la versión del servidor y el número máximo de valores que se pueden recuperar en una sola consulta.



| Versión del sistema operativo del servidor | Máximo de valores recuperados |
|---------------------------------|--------------------------|
| Windows 2000                    | 1000                     |
| Windows Server 2003             | 1.500                     |



 

Para obtener más información sobre cómo recuperar rangos de valores de atributo con ADSI, consulte recuperación de intervalos de [atributos](/windows/desktop/ADSI/attribute-range-retrieval).

Para obtener más información sobre cómo recuperar intervalos de valores de atributo con [System. DirectoryServices](/dotnet/api/system.directoryservices), consulte [enumeración de miembros en un grupo de gran tamaño](https://msdn.microsoft.com/library/ms180907(v=VS.80).aspx).

 

 