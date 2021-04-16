---
title: Lockout-Duration atributo)
description: La cantidad de tiempo que se bloquea una cuenta debido a que el Lockout-Threshold se supera.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Lockout-Duration
- lockoutDuration esquema de AD de atributos
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "105658624"
---
# <a name="lockout-duration-attribute"></a>Lockout-Duration atributo)

La cantidad de tiempo que se bloquea una cuenta debido a que se supera el [**umbral de bloqueo**](a-lockoutthreshold.md) . Este valor se almacena como un entero grande que representa el negativo del número de intervalos de 100 segundos a partir del momento en que se supera el [**umbral de bloqueo y**](a-lockoutthreshold.md) que debe transcurrir antes de que se desbloquee la cuenta.



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Lockout-Duration                     |
| Nombre para mostrar de LDAP | lockoutDuration                      |
| Tamaño              | \-                                   |
| Actualizar privilegio  | Administrador de dominio                 |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.60                |
| System-ID-GUID    | bf9679a5-0de6-11d0-a285-00aa003049e2 |
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Bloqueo: umbral**](a-lockoutthreshold.md)
</dt> </dl>

 

 





