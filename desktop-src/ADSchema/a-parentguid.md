---
title: Atributo primario-GUID
description: Se trata de un atributo construido, inventado para admitir el control DirSync. Este atributo contiene el objectGuid del elemento primario de un objeto al replicar la creación, el cambio de nombre o el desplazamiento de un objeto.
ms.assetid: caf2491b-c0bf-4ea1-80ec-d44cf9307551
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo primario-GUID
- parentGUID esquema de AD de atributos
topic_type:
- apiref
api_name:
- Parent-GUID
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38b01faf958f4add9c7788d630321d7c225f5026
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103906134"
---
# <a name="parent-guid-attribute"></a>Atributo primario-GUID

Se trata de un atributo construido, inventado para admitir el control DirSync. Este atributo contiene el objectGuid del elemento primario de un objeto al replicar la creación, el cambio de nombre o el desplazamiento de un objeto.



| Entrada | Value |
|-------------------|-------------------------------------------------------|
| CN                | Primario-GUID                                           |
| Nombre para mostrar de LDAP | parentGUID                                            |
| Tamaño              | 16 bytes                                              |
| Actualizar privilegio  | El sistema establece este valor.                      |
| Frecuencia de actualización  | Durante la replicación                                    |
| Attribute-Id      | 1.2.840.113556.1.4.1224                               |
| System-ID-GUID    | 2df90d74-009f-11d2-aa4c-00c04fd7d83a                  |
| Sintaxis            | [**Object(Replica-Link)**](s-object-replica-link.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|--------------|
| Identificador de vínculo                | \-           |
| MAPI-Id                | \-           |
| System-Only            | True         |
| Tiene un único valor       | True         |
| Está indexado             | False        |
| En el catálogo global      | False        |
| Descriptor de NT-Security- | O:BAG: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Clases usadas en        | \-           |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------|
| Identificador de vínculo                | \-           |
| MAPI-Id                | \-           |
| System-Only            | True         |
| Tiene un único valor       | True         |
| Está indexado             | False        |
| En el catálogo global      | False        |
| Descriptor de NT-Security- | O:BAG: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Clases usadas en        | \-           |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------|
| Identificador de vínculo                | \-           |
| MAPI-Id                | \-           |
| System-Only            | True         |
| Tiene un único valor       | True         |
| Está indexado             | False        |
| En el catálogo global      | False        |
| Descriptor de NT-Security- | O:BAG: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Clases usadas en        | \-           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------|
| Identificador de vínculo                | \-           |
| MAPI-Id                | \-           |
| System-Only            | True         |
| Tiene un único valor       | True         |
| Está indexado             | False        |
| En el catálogo global      | False        |
| Descriptor de NT-Security- | O:BAG: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Clases usadas en        | \-           |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------|
| Identificador de vínculo                | \-           |
| MAPI-Id                | \-           |
| System-Only            | True         |
| Tiene un único valor       | True         |
| Está indexado             | False        |
| En el catálogo global      | False        |
| Descriptor de NT-Security- | O:BAG: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Clases usadas en        | \-           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------|
| Identificador de vínculo                | \-           |
| MAPI-Id                | \-           |
| System-Only            | True         |
| Tiene un único valor       | True         |
| Está indexado             | False        |
| En el catálogo global      | False        |
| Descriptor de NT-Security- | O:BAG: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Clases usadas en        | \-           |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------|
| Identificador de vínculo                | \-           |
| MAPI-Id                | \-           |
| System-Only            | True         |
| Tiene un único valor       | True         |
| Está indexado             | False        |
| En el catálogo global      | False        |
| Descriptor de NT-Security- | O:BAG: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000000   |
| System-Flags           | 0x08000014   |
| Clases usadas en        | \-           |



 

 




