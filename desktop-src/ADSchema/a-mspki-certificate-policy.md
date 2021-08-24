---
title: Atributo ms-PKI-Certificate-Policy
description: Contiene la lista de ID de directiva y sus CSP opcionales en el certificado emitido.
ms.assetid: bc84c5ff-9cb1-406c-825c-97fa479d52eb
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-PKI-Certificate-Policy
- Esquema de AD del atributo msPKI-Certificate-Policy
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8abe92cda39428e397f06105a0ca8c5b151f84989615e06ec2f6c8371f87fc75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081689"
---
# <a name="ms-pki-certificate-policy-attribute"></a>Atributo ms-PKI-Certificate-Policy

Contiene la lista de ID de directiva y sus CSP opcionales en el certificado emitido.



| Entrada | Valor |
|-------------------|---------------------------------------------------------------------------------------------------|
| CN                | ms-PKI-Certificate-Policy                                                                         |
| Ldap-Display-Name | msPKI-Certificate-Policy                                                                          |
| Size              | 64 bytes veces el número de entradas.                                                             |
| Privilegio actualizar  | Administrador de dominio                                                                              |
| Frecuencia de actualización  | Cuando se edita, crea o clona el objeto de plantilla de certificado (ms-PKI-Certificate-Template). |
| Attribute-Id      | 1.2.840.113556.1.4.1439                                                                           |
| System-Id-Guid    | 38942346-cc5b-424b-a7d8-6ffd12029c5f                                                              |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                                       |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| Es de un solo valor       | Falso                                                                   |
| Está indexado             | Falso                                                                   |
| En el catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Clases usadas en        | [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| Es de un solo valor       | Falso                                                                   |
| Está indexado             | Falso                                                                   |
| En el catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Clases usadas en        | [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| Es de un solo valor       | Falso                                                                   |
| Está indexado             | Falso                                                                   |
| En el catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Clases usadas en        | [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| Es de un solo valor       | Falso                                                                   |
| Está indexado             | Falso                                                                   |
| En el catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Clases usadas en        | [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Falso                                                                   |
| Es de un solo valor       | Falso                                                                   |
| Está indexado             | Falso                                                                   |
| En el catálogo global      | Falso                                                                   |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Clases usadas en        | [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> |



 

 





