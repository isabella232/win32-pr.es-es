---
title: Atributo ms-DS-Supported-Encryption-Types
description: Algoritmos de cifrado admitidos por cuentas de usuario, equipo o confianza. Nota El KDC usa esta información al generar un vale de servicio para esta cuenta.
ms.assetid: 6f9055a9-531e-4f4b-8703-aca5531a3bcb
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo ms-DS-Supported-Encryption-Types
- Esquema de AD del atributo msDS-SupportedEncryptionTypes
topic_type:
- apiref
api_name:
- ms-DS-Supported-Encryption-Types
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d092061dfebcea8e9a0e4f4a060010e16102108d1e2e74f05e6df2db706141
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544345"
---
# <a name="ms-ds-supported-encryption-types-attribute"></a>Atributo ms-DS-Supported-Encryption-Types

Algoritmos de cifrado admitidos por cuentas de usuario, equipo o confianza.

> [!Note]  
> El KDC usa esta información al generar un vale de servicio para esta cuenta. Los servicios y equipos pueden actualizar automáticamente este atributo en sus respectivas cuentas de Active Directory y, por tanto, necesitan acceso de escritura a este atributo.

 



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | ms-DS-Supported-Encryption-Types     |
| Ldap-Display-Name | msDS-SupportedEncryptionTypes        |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1963              |
| System-Id-Guid    | 20119867-1d04-4ab7-9371-cfc3d5df0afd |
| Syntax            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| Es de un solo valor       | Verdadero                                                                                   |
| Está indexado             | Falso                                                                                  |
| En el catálogo global      | Falso                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|----------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| Es de un solo valor       | Verdadero                                                                                   |
| Está indexado             | Falso                                                                                  |
| En el catálogo global      | Falso                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> [**Usuario**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|----------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                     |
| MAPI-Id                | \-                                                                                     |
| System-Only            | Falso                                                                                  |
| Es de un solo valor       | Verdadero                                                                                   |
| Está indexado             | Falso                                                                                  |
| En el catálogo global      | Falso                                                                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                           |
| Range-Lower            | \-                                                                                     |
| Range-Upper            | \-                                                                                     |
| Search-Flags           | 0x00000000                                                                             |
| System-Flags           | 0x00000010                                                                             |
| Clases usadas en        | [**Dominio de confianza**](c-trusteddomain.md)<br/> [**Usuario**](c-user.md)<br/> |



 

 





