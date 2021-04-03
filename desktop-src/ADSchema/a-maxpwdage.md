---
title: Atributo Max-pwd-Age
description: La cantidad máxima de tiempo, en intervalos de 100 segundos, una contraseña es válida.
ms.assetid: b4b48207-6481-42a1-b848-6baf37a367ce
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo Max-pwd-Age
- maxPwdAge esquema de AD de atributos
topic_type:
- apiref
api_name:
- Max-Pwd-Age
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc754b7cab86dc205eb14d58db73aab64685d07a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103997463"
---
# <a name="max-pwd-age-attribute"></a>Atributo Max-pwd-Age

La cantidad máxima de tiempo, en intervalos de 100 segundos, una contraseña es válida. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el momento en que se estableció la contraseña antes de que expire la contraseña.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Max-pwd-Age                          |
| Nombre para mostrar de LDAP | maxPwdAge                            |
| Tamaño              | \-                                   |
| Actualizar privilegio  | Administrador de dominio                 |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.74                |
| System-ID-GUID    | bf9679bb-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | False                                                                                                                                                 |
| Tiene un único valor       | True                                                                                                                                                  |
| Está indexado             | False                                                                                                                                                 |
| En el catálogo global      | False                                                                                                                                                 |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



 

 





