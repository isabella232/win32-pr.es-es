---
title: Atributo Description (esquema de AD)
description: Contiene la descripción que se mostrará para un objeto . Este valor está restringido como de un solo valor por compatibilidad con versiones anteriores en algunos casos, pero puede tener varios valores en otros. Vea la sección Comentarios.
ms.assetid: 97dad871-5db0-4d1e-b931-1b053559f9c2
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo description
- esquema de AD del atributo description
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f53c344b026a89a3f579d1eb7fc7002a8a0410d28fd9b43d05882a4285eb73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961734"
---
# <a name="description-attribute-ad-schema"></a>Atributo Description (esquema de AD)

Contiene la descripción que se mostrará para un objeto . Este valor está restringido como de un solo valor por compatibilidad con versiones anteriores en algunos casos, pero puede tener varios valores en otros. Vea la sección Comentarios.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Descripción                                 |
| Ldap-Display-Name | description                                 |
| Size              | \-                                          |
| Actualizar privilegios  | Administrador de dominio o propietario de la cuenta.      |
| Frecuencia de actualización  | Siempre que sea necesario cambiar la descripción.   |
| Attribute-Id      | 2.5.4.13                                    |
| System-Id-Guid    | bf967950-0de6-11d0-a285-00aa003049e2        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                           |
| MAPI-Id                | 0x806F                                                                       |
| System-Only            | Falso                                                                        |
| Es de un solo valor       | Falso                                                                        |
| Está indexado             | Falso                                                                        |
| En el catálogo global      | Verdadero                                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                 |
| Range-Lower            | 0                                                                            |
| Range-Upper            | 1024                                                                         |
| Search-Flags           | 0x00000000                                                                   |
| System-Flags           | 0x00000010                                                                   |
| Clases usadas en        | [**Sam-Domain**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                         |
| MAPI-Id                | 0x806F                                                                                                                                     |
| System-Only            | Falso                                                                                                                                      |
| Es de un solo valor       | Falso                                                                                                                                      |
| Está indexado             | Falso                                                                                                                                      |
| En el catálogo global      | Verdadero                                                                                                                                       |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                               |
| Range-Lower            | 0                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | 0x806F                          |
| System-Only            | Falso                           |
| Es de un solo valor       | Falso                           |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 1024                            |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**ipNetwork**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="remarks"></a>Comentarios

El atributo description se implementa como un atributo de varios valores en el esquema para los casos en los que se permite. Para un objeto que no es una clase administrada de SAM, la descripción es multivalor. Para un atributo que es una clase administrada de SAM, el atributo description es de un solo valor. Las clases administradas por SAM son para cosas como las entidades de seguridad, por lo que, si tiene, por ejemplo, un contenedor o una clase propia, el esquema le permitirá usar varios valores. Este comportamiento del atributo description es por compatibilidad con versiones anteriores con sistemas operativos anteriores porque el atributo existía en las API sam antes de que existiera AD.

 

 





