---
title: Domain-Component atributo)
description: Atributo de asignación de nombres para los objetos de dominio y DNS. Normalmente, se muestra como DC DomainName.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Domain-Component
- Esquema de AD de atributo DC
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a97a6958d51c6e0e29f70685b2624fb194d42e05
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "104151442"
---
# <a name="domain-component-attribute"></a>Domain-Component atributo)

Atributo de asignación de nombres para los objetos de dominio y DNS. Normalmente se muestra como DC = DomainName.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Domain-Component                            |
| Nombre para mostrar de LDAP | dc                                          |
| Tamaño              | \-                                          |
| Actualizar privilegio  | Administrador de dominio                        |
| Frecuencia de actualización  | Cuando se crea el dominio.                 |
| Attribute-Id      | 0.9.2342.19200300.100.1.25                  |
| System-ID-GUID    | 19195a55-6da0-11d0-afd3-00c04fd930c9        |
| Sintaxis            | [**String(Unicode)**](s-string-unicode.md) |



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
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Tiene un único valor       | True                                                                                                                    |
| Está indexado             | False                                                                                                                   |
| En el catálogo global      | True                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Tiene un único valor       | True                                                                                                                    |
| Está indexado             | False                                                                                                                   |
| En el catálogo global      | True                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|---------------------------------------|
| Identificador de vínculo                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | False                                 |
| Tiene un único valor       | True                                  |
| Está indexado             | False                                 |
| En el catálogo global      | True                                  |
| Descriptor de NT-Security- | O:BAG: BAD: S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 255                                   |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000012                            |
| Clases usadas en        | [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Tiene un único valor       | True                                                                                                                    |
| Está indexado             | False                                                                                                                   |
| En el catálogo global      | True                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Tiene un único valor       | True                                                                                                                    |
| Está indexado             | False                                                                                                                   |
| En el catálogo global      | True                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Tiene un único valor       | True                                                                                                                    |
| Está indexado             | False                                                                                                                   |
| En el catálogo global      | True                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | False                                                                                                                   |
| Tiene un único valor       | True                                                                                                                    |
| Está indexado             | False                                                                                                                   |
| En el catálogo global      | True                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Nodo DNS**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



 

 





