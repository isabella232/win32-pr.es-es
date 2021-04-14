---
title: UAS-Compat atributo)
description: Indica si el administrador de cuentas de seguridad aplicará tamaños de datos para que Active Directory compatibles con el sistema de cuentas de usuario LanManager (UAS).
ms.assetid: 745e271e-28f4-4012-83a8-606d88de0221
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de UAS-Compat
- uASCompat esquema de AD de atributos
topic_type:
- apiref
api_name:
- UAS-Compat
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6bbf1088f48c697b03c4ef423930be2dbd24617
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658965"
---
# <a name="uas-compat-attribute"></a>UAS-Compat atributo)

Indica si el administrador de cuentas de seguridad aplicará tamaños de datos para que Active Directory compatibles con el sistema de cuentas de usuario LanManager (UAS). Si este valor es 0, no se aplica ningún límite. Si este valor es 1, se aplican los límites siguientes.



| Value                          | Length                         |
|--------------------------------|--------------------------------|
| Contraseña<br/>            | de 0 a 14 caracteres<br/>  |
| Nombre de cuenta<br/>        | de 0 a 20 caracteres<br/>  |
| Nombre de dominio<br/>         | de 0 a 15 caracteres<br/>  |
| Nombre del equipo<br/>       | de 0 a 15 caracteres<br/>  |
| Comentarios<br/>            | de 0 a 48 caracteres<br/>  |
| Directorio particular<br/>      | de 0 a 256 caracteres<br/> |
| Ruta de acceso del script<br/>         | de 0 a 256 caracteres<br/> |
| Unidades de tiempo por semana<br/> | 168 bits (21 bytes)<br/> |



 



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | UAS-Compat                           |
| Nombre para mostrar de LDAP | uASCompat                            |
| Tamaño              | \-                                   |
| Actualizar privilegio  | Lo lleva a cabo un administrador.       |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.155               |
| System-ID-GUID    | bf967a61-0de6-11d0-a285-00aa003049e2 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



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
| Identificador de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Tiene un único valor       | True                                                  |
| Está indexado             | False                                                 |
| En el catálogo global      | False                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Identificador de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Tiene un único valor       | True                                                  |
| Está indexado             | False                                                 |
| En el catálogo global      | False                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Identificador de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Tiene un único valor       | True                                                  |
| Está indexado             | False                                                 |
| En el catálogo global      | False                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Identificador de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Tiene un único valor       | True                                                  |
| Está indexado             | False                                                 |
| En el catálogo global      | False                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Identificador de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Tiene un único valor       | True                                                  |
| Está indexado             | False                                                 |
| En el catálogo global      | False                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------|
| Identificador de vínculo                | \-                                                    |
| MAPI-Id                | \-                                                    |
| System-Only            | False                                                 |
| Tiene un único valor       | True                                                  |
| Está indexado             | False                                                 |
| En el catálogo global      | False                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                          |
| Range-Lower            | \-                                                    |
| Range-Upper            | \-                                                    |
| Search-Flags           | 0x00000000                                            |
| System-Flags           | 0x00000010                                            |
| Clases usadas en        | [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



 

 





