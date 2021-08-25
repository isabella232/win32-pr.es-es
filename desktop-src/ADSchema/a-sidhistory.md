---
title: SID-History atributo
description: Contiene los SID anteriores usados para el objeto si el objeto se movió desde otro dominio.
ms.assetid: d738002b-fc05-4c60-aaf9-b83be61ed5a9
ms.tgt_platform: multiple
keywords:
- SID-History esquema de AD del atributo
- Esquema de AD del atributo sIDHistory
topic_type:
- apiref
api_name:
- SID-History
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c2dbfb3572392bdbed3f13683adc1cbf64b70e061962975a178f8380f55f5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119836295"
---
# <a name="sid-history-attribute"></a>SID-History atributo

Contiene los SID anteriores usados para el objeto si el objeto se movió desde otro dominio. Cada vez que se mueve un objeto de un dominio a otro, se crea un nuevo SID y ese nuevo SID se convierte en objectSID. El SID anterior se agrega a la propiedad sIDHistory.



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | SID-History                                    |
| Ldap-Display-Name | Sidhistory                                     |
| Size              | \-                                             |
| Privilegio actualizar  | El sistema establece este valor.               |
| Frecuencia de actualización  | Cada vez que el objeto se mueve a un nuevo dominio. |
| Attribute-Id      | 1.2.840.113556.1.4.609                         |
| System-Id-Guid    | 17eb4278-d167-11d0-b002-0000f80367c1           |
| Syntax            | [**String(Sid)**](s-string-sid.md)            |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Verdadero                                                         |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|--------------------------------------------------------------|
| Id. de vínculo                | \-                                                           |
| MAPI-Id                | \-                                                           |
| System-Only            | Falso                                                        |
| Es de un solo valor       | Falso                                                        |
| Está indexado             | Verdadero                                                         |
| En el catálogo global      | Verdadero                                                         |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                 |
| Range-Lower            | \-                                                           |
| Range-Upper            | \-                                                           |
| Search-Flags           | 0x00000001                                                   |
| System-Flags           | 0x00000012                                                   |
| Clases usadas en        | [**Entidad de seguridad**](c-securityprincipal.md)<br/> |



 

 





