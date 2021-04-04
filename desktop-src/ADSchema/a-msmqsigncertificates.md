---
title: Atributo MSMQ-Sign-Certificates
description: Este atributo contiene una serie de certificados. Un usuario puede generar un certificado por equipo. Para cada certificado, también se mantiene un resumen.
ms.assetid: 70e182c7-3544-43d7-b27a-6e8d03bd2d47
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MSMQ-Sign-Certificates
- mSMQSignCertificates esquema de AD de atributos
topic_type:
- apiref
api_name:
- MSMQ-Sign-Certificates
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd7e81cf145ac249b78e0a3e20be657df68b4af
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103905998"
---
# <a name="msmq-sign-certificates-attribute"></a>Atributo MSMQ-Sign-Certificates

Este atributo contiene una serie de certificados. Un usuario puede generar un certificado por equipo. Para cada certificado, también se mantiene un resumen.



| Entrada | Value |
|-------------------|----------------------------------------------------------------------------------------|
| CN                | Certificados de firma MSMQ                                                                 |
| Nombre para mostrar de LDAP | mSMQSignCertificates                                                                   |
| Tamaño              | El tipo de atributo es un BLOB, el tamaño no es limitado y los datos se mantienen en nuestro propio formato. |
| Actualizar privilegio  | \-                                                                                     |
| Frecuencia de actualización  | \-                                                                                     |
| Attribute-Id      | 1.2.840.113556.1.4.947                                                                 |
| System-ID-GUID    | 9a0dc33b-c100-11d1-bbc5-0080c76670c0                                                   |
| Sintaxis            | [**Object(Replica-Link)**](s-object-replica-link.md)                                  |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | False                                                                                         |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | False                                                                                         |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | False                                                                                         |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | False                                                                                         |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | False                                                                                         |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                            |
| MAPI-Id                | \-                                                                                            |
| System-Only            | False                                                                                         |
| Tiene un único valor       | True                                                                                          |
| Está indexado             | False                                                                                         |
| En el catálogo global      | True                                                                                          |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                  |
| Range-Lower            | \-                                                                                            |
| Range-Upper            | \-                                                                                            |
| Search-Flags           | 0x00000000                                                                                    |
| System-Flags           | 0x00000010                                                                                    |
| Clases usadas en        | [**MSMQ-Migrated: usuario**](c-msmqmigrateduser.md)<br/> [**Usuario**](c-user.md)<br/> |



 

 





