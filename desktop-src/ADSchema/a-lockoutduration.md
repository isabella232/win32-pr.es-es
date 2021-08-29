---
title: Lockout-Duration atributo
description: La cantidad de tiempo que una cuenta está bloqueada debido a la Lockout-Threshold se supera.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Lockout-Duration esquema de AD de atributo
- LockoutDuration attribute AD Schema
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af4657b46e4f6750352cef4c48b550770b21d9b24d6332882f52b03a22c835ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119301775"
---
# <a name="lockout-duration-attribute"></a>Lockout-Duration atributo

La cantidad de tiempo que una cuenta está bloqueada debido a que [**se supera el**](a-lockoutthreshold.md) umbral de bloqueo. Este valor se almacena como un entero grande que representa el negativo del número de intervalos de 100 nanosegundos desde el momento en que se supera [**el**](a-lockoutthreshold.md) umbral de bloqueo que debe transcurrir antes de que se desbloquee la cuenta.



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Lockout-Duration                     |
| Ldap-Display-Name | lockoutDuration                      |
| Size              | \-                                   |
| Actualizar privilegios  | Administrador de dominio                 |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.60                |
| System-Id-Guid    | bf9679a5-0de6-11d0-a285-00aa003049e2 |
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
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Es de un solo valor       | Verdadero                                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Es de un solo valor       | Verdadero                                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Es de un solo valor       | Verdadero                                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Es de un solo valor       | Verdadero                                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Es de un solo valor       | Verdadero                                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| Es de un solo valor       | Verdadero                                                                                                                                                  |
| Está indexado             | Falso                                                                                                                                                 |
| En el catálogo global      | Falso                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Clases usadas en        | [**Directiva de dominio**](c-domainpolicy.md)<br/> [**Sam-Domain**](c-samdomain.md)<br/> [**Sam-Domain-Base**](c-samdomainbase.md)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Umbral de bloqueo**](a-lockoutthreshold.md)
</dt> </dl>

 

 





