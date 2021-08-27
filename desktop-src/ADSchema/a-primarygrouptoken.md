---
title: Atributo Primary-Group-Token
description: Atributo calculado que se usa para recuperar la lista de pertenencia de un grupo, como Usuarios del dominio. La pertenencia completa de estos grupos no se almacena explícitamente por motivos de escalado.
ms.assetid: b23d3b7f-074b-4f1b-bc06-b22738a8a79e
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Primary-Group-Token
- Esquema de AD del atributo primaryGroupToken
topic_type:
- apiref
api_name:
- Primary-Group-Token
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd83e89a25a81f6d62207e48053fff5cafd279e29b482a9b80cb02de580ad3fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065925"
---
# <a name="primary-group-token-attribute"></a>Atributo Primary-Group-Token

Atributo calculado que se usa para recuperar la lista de pertenencia de un grupo, como Usuarios del dominio. La pertenencia completa de estos grupos no se almacena explícitamente por motivos de escalado.



| Entrada | Value |
|-------------------|--------------------------------------------|
| CN                | Primary-Group-Token                        |
| Ldap-Display-Name | primaryGroupToken                          |
| Size              | 4 bytes                                    |
| Privilegio actualizar  | El sistema establece este valor.           |
| Frecuencia de actualización  | Cada vez que cambia un grupo principal de objetos. |
| Attribute-Id      | 1.2.840.113556.1.4.1412                    |
| System-Id-Guid    | c0ed8738-7efd-4481-84d9-66d2db8be369       |
| Syntax            | [**Enumeración**](s-enumeration.md)       |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-------------------------------------|
| Id. de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadero                                |
| Es de un solo valor       | Verdadero                                |
| Está indexado             | Falso                               |
| En el catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------|
| Id. de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadero                                |
| Es de un solo valor       | Verdadero                                |
| Está indexado             | Falso                               |
| En el catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|-------------------------------------|
| Id. de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadero                                |
| Es de un solo valor       | Verdadero                                |
| Está indexado             | Falso                               |
| En el catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------|
| Id. de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadero                                |
| Es de un solo valor       | Verdadero                                |
| Está indexado             | Falso                               |
| En el catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------|
| Id. de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadero                                |
| Es de un solo valor       | Verdadero                                |
| Está indexado             | Falso                               |
| En el catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------|
| Id. de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadero                                |
| Es de un solo valor       | Verdadero                                |
| Está indexado             | Falso                               |
| En el catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------|
| Id. de vínculo                | \-                                  |
| MAPI-Id                | \-                                  |
| System-Only            | Verdadero                                |
| Es de un solo valor       | Verdadero                                |
| Está indexado             | Falso                               |
| En el catálogo global      | Falso                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                        |
| Range-Lower            | \-                                  |
| Range-Upper            | \-                                  |
| Search-Flags           | 0x00000000                          |
| System-Flags           | 0x00000014                          |
| Clases usadas en        | [**Group (Grupo)**](c-group.md)<br/> |



 

 





