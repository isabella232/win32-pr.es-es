---
title: Domain-Component atributo
description: Atributo de nomenclatura para los objetos De dominio y DNS. Normalmente se muestra como dc DomainName.
ms.assetid: 1d674af1-ed2f-4266-9704-8c6ed5a9bdd8
ms.tgt_platform: multiple
keywords:
- Domain-Component esquema de AD del atributo
- Esquema de AD del atributo dc
topic_type:
- apiref
api_name:
- Domain-Component
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe93b6629ac176452edbe5cdf13bf35afa955890cde369273f87990034bcd3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118177781"
---
# <a name="domain-component-attribute"></a>Domain-Component atributo

Atributo de nomenclatura para los objetos De dominio y DNS. Normalmente se muestra como dc=DomainName.



| Entrada | Valor |
|-------------------|---------------------------------------------|
| CN                | Domain-Component                            |
| Ldap-Display-Name | dc                                          |
| Size              | \-                                          |
| Privilegio actualizar  | Administrador de dominio                        |
| Frecuencia de actualización  | Cuando se crea el dominio.                 |
| Attribute-Id      | 0.9.2342.19200300.100.1.25                  |
| System-Id-Guid    | 19195a55-6da0-11d0-afd3-00c04fd930c9        |
| Syntax            | [**String(Unicode)**](s-string-unicode.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adán**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                    |
| Está indexado             | Falso                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Dns-Node**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                    |
| Está indexado             | Falso                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Dns-Node**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Valor |
|------------------------|---------------------------------------|
| Id. de vínculo                | \-                                    |
| MAPI-Id                | \-                                    |
| System-Only            | Falso                                 |
| Es de un solo valor       | Verdadero                                  |
| Está indexado             | Falso                                 |
| En el catálogo global      | Verdadero                                  |
| NT-Security-Descriptor | O:BAG:BAD:S:                          |
| Range-Lower            | 1                                     |
| Range-Upper            | 255                                   |
| Search-Flags           | 0x00000000                            |
| System-Flags           | 0x00000012                            |
| Clases usadas en        | [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                    |
| Está indexado             | Falso                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Dns-Node**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                    |
| Está indexado             | Falso                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Dns-Node**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                    |
| Está indexado             | Falso                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Dns-Node**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                      |
| MAPI-Id                | \-                                                                                                                      |
| System-Only            | Falso                                                                                                                   |
| Es de un solo valor       | Verdadero                                                                                                                    |
| Está indexado             | Falso                                                                                                                   |
| En el catálogo global      | Verdadero                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                            |
| Range-Lower            | 1                                                                                                                       |
| Range-Upper            | 255                                                                                                                     |
| Search-Flags           | 0x00000000                                                                                                              |
| System-Flags           | 0x00000012                                                                                                              |
| Clases usadas en        | [**Dns-Node**](c-dnsnode.md)<br/> [**Zona DNS**](c-dnszone.md)<br/> [**Domain**](c-domain.md)<br/> |



 

 





