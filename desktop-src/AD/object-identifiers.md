---
title: Identificadores de objeto (AD DS)
description: Los identificadores de objeto (OID) son valores numéricos únicos emitidos por varias autoridades emisoras para identificar de forma única los elementos de datos, las sintaxis y otras partes de las aplicaciones distribuidas.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificadores de objeto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "105656305"
---
# <a name="object-identifiers-ad-ds"></a>Identificadores de objeto (AD DS)

Los identificadores de objeto (OID) son valores numéricos únicos emitidos por varias autoridades emisoras para identificar de forma única los elementos de datos, las sintaxis y otras partes de las aplicaciones distribuidas. Los OID se encuentran en aplicaciones OSI, directorios X. 500, SNMP y otras aplicaciones en las que la unicidad es importante. Los OID se basan en una estructura de árbol, en la que una entidad de emisión superior, como la ISO, asigna una rama del árbol a un subautoridad, que a su vez puede asignar subramas.

El protocolo LDAP (RFC 2251) requiere un servicio de directorio para identificar las clases de objetos, atributos y sintaxis con OID. Esto forma parte de las versiones anteriores de LDAP X. 500.

Los OID de Active Directory Domain Services incluyen algunos emitidos por la ISO para las clases y atributos X. 500 y otros emitidos por Microsoft y otras entidades emisoras. La notación OID es una cadena de números con puntos, por ejemplo "1.2.840.113556.1.5.9", que se describe en la tabla siguiente.



| Value  | Significado          | Descripción                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | Identifica la entidad de certificación raíz.                           |
| 2      | ANSI             | Designación de grupo asignada por ISO.                       |
| 840    | EE. UU.              | Designación de país o región asignada por el grupo.        |
| 113556 | Microsoft        | Designación de la organización asignada por el país o la región. |
| 1      | Active Directory | Asignado por la organización.                            |
| 5      | Clases          | Asignado por la organización.                            |
| 9      | clase de **usuario**   | Asignado por la organización.                            |



 

Para obtener más información y una explicación de los dos procedimientos utilizados para obtener OID válidos para su uso en la extensión del esquema de Active Directory, vea [obtener un identificador de objeto](obtaining-an-object-identifier.md).

 

 




