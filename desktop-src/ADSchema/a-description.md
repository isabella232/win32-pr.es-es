---
title: Description (atributo) (esquema de AD)
description: Contiene la descripción que se va a mostrar para un objeto. Este valor se restringe como de valor único para la compatibilidad con versiones anteriores en algunos casos, pero puede tener varios valores en otros. Vea la sección Comentarios.
ms.assetid: 97dad871-5db0-4d1e-b931-1b053559f9c2
ms.tgt_platform: multiple
keywords:
- Atributo de Descripción esquema de AD
- atributo de Descripción esquema de AD
topic_type:
- apiref
api_name:
- Description
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ccb155c9c65a42c29a022a6912b7aea7087477
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804357"
---
# <a name="description-attribute-ad-schema"></a>Description (atributo) (esquema de AD)

Contiene la descripción que se va a mostrar para un objeto. Este valor se restringe como de valor único para la compatibilidad con versiones anteriores en algunos casos, pero puede tener varios valores en otros. Vea la sección Comentarios.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Descripción                                 |
| Nombre para mostrar de LDAP | description                                 |
| Tamaño              | \-                                          |
| Actualizar privilegio  | Administrador de dominio o propietario de la cuenta.      |
| Frecuencia de actualización  | Siempre que sea necesario cambiar la descripción.   |
| Attribute-Id      | 2.5.4.13                                    |
| System-ID-GUID    | bf967950-0de6-11d0-a285-00aa003049e2        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                           |
| MAPI-Id                | 0x806F                                                                       |
| System-Only            | False                                                                        |
| Tiene un único valor       | False                                                                        |
| Está indexado             | False                                                                        |
| En el catálogo global      | True                                                                         |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                 |
| Range-Lower            | 0                                                                            |
| Range-Upper            | 1024                                                                         |
| Search-Flags           | 0x00000000                                                                   |
| System-Flags           | 0x00000010                                                                   |
| Clases usadas en        | [**Sam-dominio**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                         |
| MAPI-Id                | 0x806F                                                                                                                                     |
| System-Only            | False                                                                                                                                      |
| Tiene un único valor       | False                                                                                                                                      |
| Está indexado             | False                                                                                                                                      |
| En el catálogo global      | True                                                                                                                                       |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                               |
| Range-Lower            | 0                                                                                                                                          |
| Range-Upper            | 1024                                                                                                                                       |
| Search-Flags           | 0x00000000                                                                                                                                 |
| System-Flags           | 0x00000010                                                                                                                                 |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | 0x806F                          |
| System-Only            | False                           |
| Tiene un único valor       | False                           |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 1024                            |
| Search-Flags           | 0x00000000                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**Red IP**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**Red IP**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**Red IP**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x806F                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Range-Upper            | 1024                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Clases usadas en        | [**groupOfUniqueNames**](c-groupofuniquenames.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Arriba**](c-top.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> [**shadowAccount**](c-shadowaccount.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**ipService**](c-ipservice.md)<br/> [**ipProtocol**](c-ipprotocol.md)<br/> [**oncRpc**](c-oncrpc.md)<br/> [**ipHost**](c-iphost.md)<br/> [**Red IP**](c-ipnetwork.md)<br/> [**nisNetgroup**](c-nisnetgroup.md)<br/> [**nisMap**](c-nismap.md)<br/> [**nisObject**](c-nisobject.md)<br/> |



## <a name="remarks"></a>Observaciones

El atributo Description se implementa como un atributo de varios valores en el esquema para los casos en los que se permite. Para un objeto que no es una clase administrada SAM, la descripción tiene varios valores. Para un atributo que es una clase administrada SAM, el atributo Description tiene un solo valor. Las clases administradas de SAM son para elementos como las entidades de seguridad, por lo que si tiene, por ejemplo, un contenedor o una clase propia, el esquema le permitirá usar varios valores. Este comportamiento del atributo Description es para la compatibilidad con versiones anteriores de sistemas operativos, ya que el atributo existía en las API de SAM antes de que existiera AD.

 

 





