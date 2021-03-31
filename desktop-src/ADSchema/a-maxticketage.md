---
title: Atributo Max-ticket-Age
description: Este atributo determina el tiempo máximo, en horas, que se puede usar el vale de concesión de vales (TGT) de un usuario para la autenticación Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo Max-ticket-Age
- maxTicketAge esquema de AD de atributos
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d68bca2f8dd87d37be7215e26f549424cd32b9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804411"
---
# <a name="max-ticket-age-attribute"></a>Atributo Max-ticket-Age

Este atributo determina el tiempo máximo, en horas, que se puede usar el vale de concesión de vales (TGT) de un usuario para la autenticación Kerberos. Cuando expire el TGT de un usuario, se debe solicitar uno nuevo o se debe renovar el existente. De forma predeterminada, este valor se establece en 10 horas en el dominio predeterminado directiva de grupo objeto (GPO).



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Max-ticket-Age                       |
| Nombre para mostrar de LDAP | maxTicketAge                         |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| System-ID-GUID    | bf9679be-0de6-11d0-a285-00aa003049e2 |
| Sintaxis            | [**Interval**](s-interval.md)       |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Identificador de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Tiene un único valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Identificador de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Tiene un único valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Identificador de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Tiene un único valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Identificador de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Tiene un único valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Identificador de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Tiene un único valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Identificador de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Tiene un único valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



 

 





