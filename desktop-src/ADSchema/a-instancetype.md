---
title: Instance-Type atributo
description: Campo de bits que determina cómo se crea una instancia del objeto en un servidor determinado.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Instance-Type esquema de AD del atributo
- Esquema de AD del atributo instanceType
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb087afedfb6570c2d25858ca99a53749607f2260f3a6f7a24ae766e22ea3e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925285"
---
# <a name="instance-type-attribute"></a>Instance-Type atributo

Campo de bits que determina cómo se crea una instancia del objeto en un servidor determinado. El valor de este atributo puede diferir en diferentes réplicas incluso si las réplicas están sincronizadas.

Este atributo puede ser cero o una combinación de uno o varios de los valores siguientes.

| Value      | Descripción                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| 0x00000001 | El responsable del contexto de nomenclatura.                                                                        |
| 0x00000002 | No se crea una instancia de esta réplica.                                                                  |
| 0x00000004 | El objeto se puede escribir en este directorio.                                                          |
| 0x00000008 | Se mantiene el contexto de nomenclatura por encima de este en este directorio.                                       |
| 0x00000010 | El contexto de nomenclatura está en proceso de construirse por primera vez mediante la replicación. |
| 0x00000020 | El contexto de nomenclatura está en proceso de quitarse de la DSA local.                          |



 



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | Instance-Type                                  |
| Ldap-Display-Name | instanceType                                   |
| Size              | 4 bytes.                                       |
| Privilegio actualizar  | El administrador del esquema establece este valor. |
| Frecuencia de actualización  | Cuando se crea el objeto .                    |
| Attribute-Id      | 1.2.840.113556.1.2.1                           |
| System-Id-Guid    | bf96798c-0de6-11d0-a285-00aa003049e2           |
| Syntax            | [**Enumeración**](s-enumeration.md)           |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Verdadero                            |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Falso                           |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



 

 





