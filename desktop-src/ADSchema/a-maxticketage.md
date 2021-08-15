---
title: Atributo Max-Ticket-Age
description: Este atributo determina la cantidad máxima de tiempo, en horas, que se puede usar el vale de concesión de vales (TGT) de un usuario para la autenticación Kerberos.
ms.assetid: 54ab0f2b-31eb-45d7-9a43-e70dc78136b5
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Max-Ticket-Age
- Esquema de AD del atributo maxTicketAge
topic_type:
- apiref
api_name:
- Max-Ticket-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9c876bbab2b60d655464129d0a59aeda110f78d8e2514866a3bcf28a859cb3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301015"
---
# <a name="max-ticket-age-attribute"></a>Atributo Max-Ticket-Age

Este atributo determina la cantidad máxima de tiempo, en horas, que se puede usar el vale de concesión de vales (TGT) de un usuario para la autenticación Kerberos. Cuando expira el TGT de un usuario, se debe solicitar uno nuevo o se debe renovar el existente. De forma predeterminada, esta configuración se establece en 10 horas en el objeto de directiva de grupo predeterminado (GPO).



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Max-Ticket-Age                       |
| Ldap-Display-Name | maxTicketAge                         |
| Size              | \-                                   |
| Privilegio actualizar  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.77                |
| System-Id-Guid    | bf9679be-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Intervalo**](s-interval.md)       |



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
| Id. de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Es de un solo valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Id. de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Es de un solo valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Id. de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Es de un solo valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Id. de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Es de un solo valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Id. de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Es de un solo valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|----------------------------------------------------|
| Id. de vínculo                | \-                                                 |
| MAPI-Id                | \-                                                 |
| System-Only            | False                                              |
| Es de un solo valor       | True                                               |
| Está indexado             | False                                              |
| En el catálogo global      | False                                              |
| NT-Security-Descriptor | O:BAG:BAD:S:                                       |
| Range-Lower            | \-                                                 |
| Range-Upper            | \-                                                 |
| Search-Flags           | 0x00000000                                         |
| System-Flags           | 0x00000010                                         |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> |



 

 





