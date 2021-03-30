---
title: Atributo Primary-Group-token
description: Atributo calculado que se usa para recuperar la lista de miembros de un grupo, como usuarios del dominio. La pertenencia completa de estos grupos no se almacena explícitamente por motivos de escala.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de grupo principal-de-token
- primaryGroupToken esquema de AD de atributos
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b237ab5998ca3f38f2d07128b36d9337c96935d
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151595"
---
# <a name="primary-group-token-attribute"></a>Atributo Primary-Group-token

Atributo calculado que se usa para recuperar la lista de miembros de un grupo, como usuarios del dominio. La pertenencia completa de estos grupos no se almacena explícitamente por motivos de escala.



| Entrada | Value |
|-------------------|--------------------------------------------|
| CN                | Token de grupo principal                        |
| Nombre para mostrar de LDAP | primaryGroupToken                          |
| Tamaño              | 4 bytes                                    |
| Actualizar privilegio  | El sistema establece este valor.           |
| Frecuencia de actualización  | Cada vez que cambia un grupo primario de objetos. |
| Attribute-Id      | 1.2.840.113556.1.4.1412                    |
| System-ID-GUID    | c0ed8738-7efd-4481-84d9-66d2db8be369       |
| Sintaxis            | [**Enumeración**](s-enumeration.md)       |



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
|------------------------|-------------------------------------|
| Identificador de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| Tiene un único valor       | True                                |
| Está indexado             | False                               |
| En el catálogo global      | False                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------|
| Identificador de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| Tiene un único valor       | True                                |
| Está indexado             | False                               |
| En el catálogo global      | False                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|-------------------------------------|
| Identificador de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| Tiene un único valor       | True                                |
| Está indexado             | False                               |
| En el catálogo global      | False                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------|
| Identificador de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| Tiene un único valor       | True                                |
| Está indexado             | False                               |
| En el catálogo global      | False                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------|
| Identificador de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| Tiene un único valor       | True                                |
| Está indexado             | False                               |
| En el catálogo global      | False                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------|
| Identificador de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| Tiene un único valor       | True                                |
| Está indexado             | False                               |
| En el catálogo global      | False                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------|
| Identificador de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | True                                |
| Tiene un único valor       | True                                |
| Está indexado             | False                               |
| En el catálogo global      | False                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



 

 





