---
title: Instance-Type atributo)
description: Un campo de bits que determina cómo se crea una instancia del objeto en un servidor determinado.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Instance-Type
- instanceType esquema de AD de atributos
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e31eec3c5a7a189f4623e8e77badb3b1e83e0cd4
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804777"
---
# <a name="instance-type-attribute"></a>Instance-Type atributo)

Un campo de bits que determina cómo se crea una instancia del objeto en un servidor determinado. El valor de este atributo puede diferir en las distintas réplicas, incluso si las réplicas están sincronizadas.

Este atributo puede ser cero o una combinación de uno o varios de los valores siguientes.

| Value      | Descripción                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| 0x00000001 | Encabezado del contexto de nomenclatura.                                                                        |
| 0x00000002 | No se crea una instancia de esta réplica.                                                                  |
| 0x00000004 | El objeto es grabable en este directorio.                                                          |
| 0x00000008 | Se mantiene el contexto de nomenclatura por encima de este en este directorio.                                       |
| 0x00000010 | El contexto de nomenclatura está en proceso de construirse por primera vez mediante la replicación. |
| 0x00000020 | El contexto de nomenclatura está en proceso de quitarse del DSA local.                          |



 



| Entrada | Value |
|-------------------|------------------------------------------------|
| CN                | Instance-Type                                  |
| Nombre para mostrar de LDAP | instanceType                                   |
| Tamaño              | 4 bytes.                                       |
| Actualizar privilegio  | El administrador del esquema establece este valor. |
| Frecuencia de actualización  | Cuando se crea el objeto.                    |
| Attribute-Id      | 1.2.840.113556.1.2.1                           |
| System-ID-GUID    | bf96798c-0de6-11d0-a285-00aa003049e2           |
| Sintaxis            | [**Enumeración**](s-enumeration.md)           |



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
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| Tiene un único valor       | True                            |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| Tiene un único valor       | True                            |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| Tiene un único valor       | True                            |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| Tiene un único valor       | True                            |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| Tiene un único valor       | True                            |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| Tiene un único valor       | True                            |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|---------------------------------|
| Identificador de vínculo                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | True                            |
| Tiene un único valor       | True                            |
| Está indexado             | False                           |
| En el catálogo global      | True                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



 

 





