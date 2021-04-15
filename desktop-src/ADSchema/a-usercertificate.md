---
title: X509-Cert atributo)
description: Contiene los certificados X. 509v3 codificados en DER emitidos para el usuario. Tenga en cuenta que esta propiedad contiene los certificados de clave pública emitidos para este usuario por el servicio de certificados de Microsoft.
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de X509-Cert
- atributo userCertificate esquema de AD
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faa6f0dfb5acc25890361a124e52b8b24958915f
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104493906"
---
# <a name="x509-cert-attribute"></a>X509-Cert atributo)

Contiene los certificados X. 509v3 codificados en DER emitidos para el usuario. Tenga en cuenta que esta propiedad contiene los certificados de clave pública emitidos para este usuario por el servicio de certificados de Microsoft.



| Entrada | Value |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| Nombre para mostrar de LDAP | userCertificate                                                                                                         |
| Tamaño              | Este atributo requerirá aproximadamente 4 KB para cada certificado de agente de recuperación de claves emitido por la entidad de certificación mediante la instancia de KRA. |
| Actualizar privilegio  | Administrador de dominio                                                                                                    |
| Frecuencia de actualización  | Cada vez que se emite un certificado.                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| System-ID-GUID    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
| Sintaxis            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                                   |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                     |
| MAPI-Id                | 0x8C6A                                                                                 |
| System-Only            | False                                                                                  |
| Tiene un único valor       | False                                                                                  |
| Está indexado             | False                                                                                  |
| En el catálogo global      | True                                                                                   |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Clases usadas en        | [**Destinatario de correo**](c-mailrecipient.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**User**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | False                                                                                                                                                                                                                              |
| Tiene un único valor       | False                                                                                                                                                                                                                              |
| Está indexado             | False                                                                                                                                                                                                                              |
| En el catálogo global      | True                                                                                                                                                                                                                               |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**MS-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuario**](c-user.md)<br/> |



 

 





