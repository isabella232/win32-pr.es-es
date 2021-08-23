---
title: X509-Cert atributo
description: Contiene los certificados X.509v3 codificados con DER emitidos al usuario. Tenga en cuenta que esta propiedad contiene los certificados de clave pública emitidos a este usuario por Microsoft Certificate Service.
ms.assetid: bdd6b9a4-c402-462c-be2c-8e7e582a899a
ms.tgt_platform: multiple
keywords:
- X509-Cert esquema de AD de atributo
- UserCertificate attribute AD Schema
topic_type:
- apiref
api_name:
- X509-Cert
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0d6d95ab05047c19ba978a02957dca3870c2f93cf26b323bd6aa55c2f35472a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644595"
---
# <a name="x509-cert-attribute"></a>X509-Cert atributo

Contiene los certificados X.509v3 codificados con DER emitidos al usuario. Tenga en cuenta que esta propiedad contiene los certificados de clave pública emitidos a este usuario por Microsoft Certificate Service.



| Entrada | Valor |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| CN                | X509-Cert                                                                                                               |
| Ldap-Display-Name | userCertificate                                                                                                         |
| Size              | Este atributo requerirá aproximadamente 4 KB para cada certificado del agente de recuperación de claves emitido por la entidad de certificación mediante la instancia DERON. |
| Actualizar privilegios  | Administrador de dominio                                                                                                    |
| Frecuencia de actualización  | Cada vez que se emite un certificado.                                                                                      |
| Attribute-Id      | 2.5.4.36                                                                                                                |
| System-Id-Guid    | bf967a7f-0de6-11d0-a285-00aa003049e2                                                                                    |
| Syntax            | [**Object(Replica-Link)**](s-object-replica-link.md)                                                                   |



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
| Id. de vínculo                | \-                                                                                     |
| MAPI-Id                | 0x8C6A                                                                                 |
| System-Only            | Falso                                                                                  |
| Es de un solo valor       | Falso                                                                                  |
| Está indexado             | Falso                                                                                  |
| En el catálogo global      | Verdadero                                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Clases usadas en        | [**Destinatario de correo**](c-mailrecipient.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                 |
| MAPI-Id                | 0x8C6A                                                                                                                                                                                                                             |
| System-Only            | Falso                                                                                                                                                                                                                              |
| Es de un solo valor       | Falso                                                                                                                                                                                                                              |
| Está indexado             | Falso                                                                                                                                                                                                                              |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                       |
| Range-Lower            | \-                                                                                                                                                                                                                                 |
| Range-Upper            | \-                                                                                                                                                                                                                                 |
| Search-Flags           | 0x00000000                                                                                                                                                                                                                         |
| System-Flags           | 0x00000010                                                                                                                                                                                                                         |
| Clases usadas en        | [**inetOrgPerson**](c-inetorgperson.md)<br/> [**Destinatario de correo**](c-mailrecipient.md)<br/> [**ms-PKI-Private-Key-Recovery-Agent**](c-mspki-privatekeyrecoveryagent.md)<br/> [**Usuario**](c-user.md)<br/> |



 

 





