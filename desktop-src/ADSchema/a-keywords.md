---
title: Atributo Keywords
description: Lista de palabras clave que se pueden usar para buscar un punto de conexión determinado.
ms.assetid: 24297ebf-8d32-4b22-9dd9-b26bce675118
ms.tgt_platform: multiple
keywords:
- Esquema de AD del atributo Keywords
- Esquema de AD del atributo keywords
topic_type:
- apiref
api_name:
- Keywords
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2efa6f3b24aae32cdd0501a5474133981f2c9e582997663480814c6d1167e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924825"
---
# <a name="keywords-attribute"></a>Atributo Keywords

Lista de palabras clave que se pueden usar para buscar un punto de conexión determinado.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Palabras clave                                    |
| Ldap-Display-Name | keywords                                    |
| Size              | \-                                          |
| Actualizar privilegios  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.48                       |
| System-Id-Guid    | bf967993-0de6-11d0-a285-00aa003049e2        |
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



| Entrada | Value |
|------------------------|----------------------------------------------------------|
| Id. de vínculo                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | Falso                                                    |
| Es de un solo valor       | Falso                                                    |
| Está indexado             | Verdadero                                                     |
| En el catálogo global      | Verdadero                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 256                                                      |
| Search-Flags           | 0x00000001                                               |
| System-Flags           | 0x00000010                                               |
| Clases usadas en        | [**Punto de conexión**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="adam"></a>Adán



| Entrada | Value |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                       |
| MAPI-Id                | \-                                                                                                                       |
| System-Only            | Falso                                                                                                                    |
| Es de un solo valor       | Falso                                                                                                                    |
| Está indexado             | Verdadero                                                                                                                     |
| En el catálogo global      | Verdadero                                                                                                                     |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                             |
| Range-Lower            | 1                                                                                                                        |
| Range-Upper            | 256                                                                                                                      |
| Search-Flags           | 0x00000001                                                                                                               |
| System-Flags           | 0x00000010                                                                                                               |
| Clases usadas en        | [**ms-DS-Service-Connection-Point-Publication-Service**](c-msds-serviceconnectionpointpublicationservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Id. de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | Falso                                                                                                                                                                                                                                                                                   |
| Es de un solo valor       | Falso                                                                                                                                                                                                                                                                                   |
| Está indexado             | Verdadero                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | Verdadero                                                                                                                                                                                                                                                                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-Dfs**](c-ftdfs.md)<br/> [**ms-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**ms-DS-App-Data**](c-msds-appdata.md)<br/> |



 

 





