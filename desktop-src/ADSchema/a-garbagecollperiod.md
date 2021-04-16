---
title: Atributo Garbage-COLLATE-period
description: Este atributo se encuentra en el servicio de directorio CN, CN Windows NT, CN Services, CN Configuration,... objeto. Representa el tiempo, en horas, entre ejecuciones de recolección de elementos no utilizados de DS.
ms.assetid: 982a75f9-04b5-489e-99b3-a9fd3fb280c8
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Garbage-COLLATE-period
- garbageCollPeriod esquema de AD de atributos
topic_type:
- apiref
api_name:
- Garbage-Coll-Period
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64890df97cf4c131ad0dcdbed8cb80bf20b66a83
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658521"
---
# <a name="garbage-coll-period-attribute"></a>Atributo Garbage-COLLATE-period

Este atributo se encuentra en el CN = Directory Service, CN = Windows NT, CN = Services, CN = Configuration,... objeto. Representa el tiempo, en horas, entre ejecuciones de recolección de elementos no utilizados de DS.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Tiempo de intercalación de elementos no utilizados                  |
| Nombre para mostrar de LDAP | garbageCollPeriod                    |
| Tamaño              | 4 bytes                              |
| Actualizar privilegio  | Administrador de dominio                 |
| Frecuencia de actualización  | Muy poco frecuente.                           |
| Attribute-Id      | 1.2.840.113556.1.2.301               |
| System-ID-GUID    | 5fd424a1-1262-11d0-a060-00aa006c33ed |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | False                                                                                                 |
| Tiene un único valor       | True                                                                                                  |
| Está indexado             | False                                                                                                 |
| En el catálogo global      | False                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Clases usadas en        | [**Destinatario de correo**](c-mailrecipient.md)<br/> [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | False                                                                                                 |
| Tiene un único valor       | True                                                                                                  |
| Está indexado             | False                                                                                                 |
| En el catálogo global      | False                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Clases usadas en        | [**Destinatario de correo**](c-mailrecipient.md)<br/> [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------------------------------------------|
| Identificador de vínculo                | \-                                               |
| MAPI-Id                | 0x80AF                                           |
| System-Only            | False                                            |
| Tiene un único valor       | True                                             |
| Está indexado             | False                                            |
| En el catálogo global      | False                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                     |
| Range-Lower            | \-                                               |
| Range-Upper            | \-                                               |
| Search-Flags           | 0x00000000                                       |
| System-Flags           | 0x00000010                                       |
| Clases usadas en        | [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | False                                                                                                 |
| Tiene un único valor       | True                                                                                                  |
| Está indexado             | False                                                                                                 |
| En el catálogo global      | False                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Clases usadas en        | [**Destinatario de correo**](c-mailrecipient.md)<br/> [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | False                                                                                                 |
| Tiene un único valor       | True                                                                                                  |
| Está indexado             | False                                                                                                 |
| En el catálogo global      | False                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Clases usadas en        | [**Destinatario de correo**](c-mailrecipient.md)<br/> [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | False                                                                                                 |
| Tiene un único valor       | True                                                                                                  |
| Está indexado             | False                                                                                                 |
| En el catálogo global      | False                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Clases usadas en        | [**Destinatario de correo**](c-mailrecipient.md)<br/> [**NTDS-servicio**](c-ntdsservice.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                    |
| MAPI-Id                | 0x80AF                                                                                                |
| System-Only            | False                                                                                                 |
| Tiene un único valor       | True                                                                                                  |
| Está indexado             | False                                                                                                 |
| En el catálogo global      | False                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                          |
| Range-Lower            | \-                                                                                                    |
| Range-Upper            | \-                                                                                                    |
| Search-Flags           | 0x00000000                                                                                            |
| System-Flags           | 0x00000010                                                                                            |
| Clases usadas en        | [**Destinatario de correo**](c-mailrecipient.md)<br/> [**NTDS-servicio**](c-ntdsservice.md)<br/> |



 

 





