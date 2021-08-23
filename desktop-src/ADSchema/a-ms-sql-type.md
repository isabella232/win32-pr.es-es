---
title: Atributo MS-SQL-Type
description: Tipo de replicación utilizado por este SQL servidor.
ms.assetid: 8e7fa9ab-9a25-4ee3-9134-68af698a5fb8
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo MS-SQL-Type
- Esquema de AD del atributo mS-SQL-Type
topic_type:
- apiref
api_name:
- MS-SQL-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15850884b8071fc103abf2c8d3f12ad68d4f5ed946ef2b491b4907b87b1cb524
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583295"
---
# <a name="ms-sql-type-attribute"></a>Atributo MS-SQL-Type

Tipo de replicación utilizado por este SQL servidor. Los valores siguientes son los valores posibles para este atributo.



| Valor        | Descripción                           |
|--------------|---------------------------------------|
| 0<br/> | Replicación transaccional.<br/> |
| 1<br/> | Replicación de instantáneas.<br/>      |
| 2<br/> | Replicación de mezcla.<br/>         |



 



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | MS-SQL-Type                                 |
| Ldap-Display-Name | mS-SQL-Type                                 |
| Size              | \-                                          |
| Actualizar privilegios  | Administrador de dominio                        |
| Frecuencia de actualización  | Cuando se configura la replicación.                 |
| Attribute-Id      | 1.2.840.113556.1.4.1391                     |
| System-Id-Guid    | ca48eba8-ccee-11d2-9993-0000f87a57d4        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| Es de un solo valor       | Verdadero                                                                                                                                |
| Está indexado             | Falso                                                                                                                               |
| En el catálogo global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Clases usadas en        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| Es de un solo valor       | Verdadero                                                                                                                                |
| Está indexado             | Falso                                                                                                                               |
| En el catálogo global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Clases usadas en        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| Es de un solo valor       | Verdadero                                                                                                                                |
| Está indexado             | Falso                                                                                                                               |
| En el catálogo global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Clases usadas en        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| Es de un solo valor       | Verdadero                                                                                                                                |
| Está indexado             | Falso                                                                                                                               |
| En el catálogo global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Clases usadas en        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| Es de un solo valor       | Verdadero                                                                                                                                |
| Está indexado             | Falso                                                                                                                               |
| En el catálogo global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Clases usadas en        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                  |
| MAPI-Id                | \-                                                                                                                                  |
| System-Only            | Falso                                                                                                                               |
| Es de un solo valor       | Verdadero                                                                                                                                |
| Está indexado             | Falso                                                                                                                               |
| En el catálogo global      | Falso                                                                                                                               |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                        |
| Range-Lower            | \-                                                                                                                                  |
| Range-Upper            | \-                                                                                                                                  |
| Search-Flags           | 0x00000000                                                                                                                          |
| System-Flags           | 0x00000010                                                                                                                          |
| Clases usadas en        | [**MS-SQL-SQLPublication**](c-ms-sql-sqlpublication.md)<br/> [**MS-SQL-OLAPDatabase**](c-ms-sql-olapdatabase.md)<br/> |



 

 





