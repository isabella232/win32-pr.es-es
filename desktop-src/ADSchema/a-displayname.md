---
title: Display-Name atributo
description: Nombre para mostrar de un objeto.
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- Display-Name esquema de AD del atributo
- Esquema de AD del atributo displayName
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d4be2c6823fa068f07a14ab478a797c0db92e4f91b25656439319da5a25db1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049595"
---
# <a name="display-name-attribute"></a>Display-Name atributo

Nombre para mostrar de un objeto. Esta suele ser la combinación del nombre de los usuarios, la inicial intermedia y el apellido.



| Entrada | Value |
|-------------------|------------------------------------------------------------------------------|
| CN                | Display-Name                                                                 |
| Ldap-Display-Name | DisplayName                                                                  |
| Size              | \-                                                                           |
| Privilegio actualizar  | Administrador de dominio o propietario de la cuenta.                                       |
| Frecuencia de actualización  | Cuando se crea el registro del usuario y cuando es necesario cambiar el nombre para mostrar. |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| System-Id-Guid    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Syntax            | [**String(Unicode)**](s-string-unicode.md)                                  |



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
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                            |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                             |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                             |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Plantilla de dirección**](c-addresstemplate.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Plantilla de dirección**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|---------------------------------|
| Id. de vínculo                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Es de un solo valor       | Verdadero                            |
| Está indexado             | Verdadero                            |
| En el catálogo global      | Verdadero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 256                             |
| Search-Flags           | 0x00000005                      |
| System-Flags           | 0x00000010                      |
| Clases usadas en        | [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Plantilla de dirección**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Plantilla de dirección**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Plantilla de dirección**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Es de un solo valor       | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Clases usadas en        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Plantilla de dirección**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Clase de servicio**](c-serviceclass.md)<br/> [**Instancia de servicio**](c-serviceinstance.md)<br/> [**Arriba**](c-top.md)<br/> |



 

 





