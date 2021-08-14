---
title: Identificadores de objeto (AD DS)
description: Los identificadores de objeto (ID) son valores numéricos únicos emitidos por varias autoridades emisoras para identificar de forma única los elementos de datos, las sintaxis y otras partes de las aplicaciones distribuidas.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificadores de objeto de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af458a003c5a5a8586c32449674019fb6b241d52c4300e107898d91c75047214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185516"
---
# <a name="object-identifiers-ad-ds"></a>Identificadores de objeto (AD DS)

Los identificadores de objeto (ID) son valores numéricos únicos emitidos por varias autoridades emisoras para identificar de forma única los elementos de datos, las sintaxis y otras partes de las aplicaciones distribuidas. Los SSID se encuentran en aplicaciones OSI, directorios X.500, SNMP y otras aplicaciones donde la unidad es importante. Los ORI se basan en una estructura de árbol, en la que una autoridad emisora superior, como la ISO, asigna una rama del árbol a una subautoridad, que a su vez puede asignar subbranches.

El protocolo LDAP (RFC 2251) requiere un servicio de directorio para identificar las clases de objetos, los atributos y las sintaxis con los DIRECCIONAMIENTO. Esto forma parte del ldap X.500 heredado.

Los ID de Active Directory Domain Services incluyen algunos emitidos por la norma ISO para clases y atributos X.500, y algunos emitidos por Microsoft y otras autoridades emisoras. La notación OID es una cadena de números de puntos, por ejemplo "1.2.840.113556.1.5.9", que se describe en la tabla siguiente.



| Valor  | Significado          | Descripción                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | Identifica la autoridad raíz.                           |
| 2      | ANSI             | Designación de grupos asignada por ISO.                       |
| 840    | EE. UU.              | Designación de país o región asignada por el grupo.        |
| 113556 | Microsoft        | Designación de la organización asignada por el país o región. |
| 1      | Active Directory | Asignado por la organización.                            |
| 5      | Clases          | Asignado por la organización.                            |
| 9      | **user (clase)**   | Asignado por la organización.                            |



 

Para obtener más información y una explicación de dos procedimientos usados para obtener identificadores adicionales válidos para su uso en la extensión del esquema Active Directory, vea [Obtener un](obtaining-an-object-identifier.md)identificador de objeto .

 

 




