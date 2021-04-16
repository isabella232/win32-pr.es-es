---
title: MS-DNS-Signature-incepción-atributo offset
description: Atributo que define en segundos hasta qué punto deben comenzar los períodos de validez de la firma DNSSEC anterior al firmar la zona DNS.
ms.assetid: 2d929ec8-38ff-481e-a926-eb1251dd7a86
ms.tgt_platform: multiple
keywords:
- MS-DNS-Signature-incepción-esquema de AD de atributo de desplazamiento
- msDN-SignatureInceptionOffset atributo AD Schema
topic_type:
- apiref
api_name:
- ms-DNS-Signature-Inception-Offset
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f81e3e278b3c37531a4e537fe45583421bce8928
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104494056"
---
# <a name="ms-dns-signature-inception-offset-attribute"></a>MS-DNS-Signature-incepción-atributo offset

Atributo que define en segundos hasta qué punto deben comenzar los períodos de validez de la firma DNSSEC anterior al firmar la zona DNS.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | MS-DNS-firma-Inicio-desfase    |
| Nombre para mostrar de LDAP | msDN: SignatureInceptionOffset       |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.2141              |
| System-ID-GUID    | 03d4c32e-e217-4a61-9699-7bbc4729a026 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------|
| Identificador de vínculo                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | False                                    |
| Tiene un único valor       | True                                     |
| Está indexado             | False                                    |
| En el catálogo global      | False                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                             |
| Range-Lower            | 0                                        |
| Range-Upper            | 2592000                                  |
| Search-Flags           | 0x00000008                               |
| System-Flags           | 0x00000010                               |
| Clases usadas en        | [**Zona DNS**](c-dnszone.md)<br/> |



 

 





