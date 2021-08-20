---
title: UAS-Compat atributo
description: Indica si el administrador de cuentas de seguridad aplicará tamaños de datos para que Active Directory compatible con el sistema de cuentas de usuario (UAS) de LanManager.
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- UAS-Compat esquema de AD de atributo
- Esquema de AD del atributo uASCompat
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7a0cb7b8787a55c710f283dbcd37bbe0f6a296505c75a5335bf35ea69c34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118681544"
---
# <a name="uas-compat-attribute"></a>UAS-Compat atributo

Indica si el administrador de cuentas de seguridad aplicará tamaños de datos para que Active Directory compatible con el sistema de cuentas de usuario (UAS) de LanManager. Si este valor es 0, no se aplica ningún límite. Si este valor es 1, se aplican los límites siguientes.



| Value                          | Length                         |
|--------------------------------|--------------------------------|
| Contraseña<br/>            | De 0 a 14 caracteres<br/>  |
| Nombre de cuenta<br/>        | De 0 a 20 caracteres<br/>  |
| Nombre de dominio<br/>         | De 0 a 15 caracteres<br/>  |
| Nombre del equipo<br/>       | De 0 a 15 caracteres<br/>  |
| Comentarios<br/>            | De 0 a 48 caracteres<br/>  |
| Directorio particular<br/>      | De 0 a 256 caracteres<br/> |
| Ruta de acceso del script<br/>         | De 0 a 256 caracteres<br/> |
| Unidades de tiempo por semana<br/> | 168 bits (21 bytes)<br/> |



 



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | UAS-Compat                           |
| Ldap-Display-Name | uASCompat                            |
| Size              | \-                                   |
| Actualizar privilegios  | Realizado por un administrador.       |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.155               |
| System-Id-Guid    | bf967a61-0de6-11d0-a285-00aa003049e2 |
| Syntax            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Id. de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Es de un solo valor       | True                                                  |
| Está indexado             | Falso                                                 |
| En el catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Id. de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Es de un solo valor       | True                                                  |
| Está indexado             | Falso                                                 |
| En el catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Id. de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Es de un solo valor       | Verdadero                                                  |
| Está indexado             | Falso                                                 |
| En el catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Id. de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Es de un solo valor       | True                                                  |
| Está indexado             | Falso                                                 |
| En el catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Id. de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Es de un solo valor       | True                                                  |
| Está indexado             | Falso                                                 |
| En el catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Id. de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | Falso                                                 |
| Es de un solo valor       | True                                                  |
| Está indexado             | Falso                                                 |
| En el catálogo global      | Falso                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



 

 





