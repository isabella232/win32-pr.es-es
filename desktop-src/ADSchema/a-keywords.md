---
title: Keywords (atributo)
description: Una lista de palabras clave que se pueden usar para buscar un punto de conexión determinado.
ms.assetid: 24297ebf-8d32-4b22-9dd9-b26bce675118
ms.tgt_platform: multiple
keywords:
- Atributo Keywords esquema de AD
- atributo Keywords esquema de AD
topic_type:
- apiref
api_name:
- Keywords
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5c1fba475505ee03cda4813f90a28d1c91fb69
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804759"
---
# <a name="keywords-attribute"></a>Keywords (atributo)

Una lista de palabras clave que se pueden usar para buscar un punto de conexión determinado.



| Entrada | Value |
|-------------------|---------------------------------------------|
| CN                | Palabras clave                                    |
| Nombre para mostrar de LDAP | keywords                                    |
| Tamaño              | \-                                          |
| Actualizar privilegio  | \-                                          |
| Frecuencia de actualización  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.48                       |
| System-ID-GUID    | bf967993-0de6-11d0-a285-00aa003049e2        |
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
|------------------------|----------------------------------------------------------|
| Identificador de vínculo                | \-                                                       |
| MAPI-Id                | \-                                                       |
| System-Only            | False                                                    |
| Tiene un único valor       | False                                                    |
| Está indexado             | True                                                     |
| En el catálogo global      | True                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                             |
| Range-Lower            | 1                                                        |
| Range-Upper            | 256                                                      |
| Search-Flags           | 0x00000001                                               |
| System-Flags           | 0x00000010                                               |
| Clases usadas en        | [**Punto de conexión**](c-connectionpoint.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                   |
| Está indexado             | True                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-app-data**](c-msds-appdata.md)<br/> |



## <a name="adam"></a>ADAM



| Entrada | Value |
|------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                       |
| MAPI-Id                | \-                                                                                                                       |
| System-Only            | False                                                                                                                    |
| Tiene un único valor       | False                                                                                                                    |
| Está indexado             | True                                                                                                                     |
| En el catálogo global      | True                                                                                                                     |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                             |
| Range-Lower            | 1                                                                                                                        |
| Range-Upper            | 256                                                                                                                      |
| Search-Flags           | 0x00000001                                                                                                               |
| System-Flags           | 0x00000010                                                                                                               |
| Clases usadas en        | [**Servicio MS-DS-Service-Connection-Point-Publication-Service**](c-msds-serviceconnectionpointpublicationservice.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                   |
| Está indexado             | True                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-app-data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                   |
| Está indexado             | True                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-app-data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                   |
| Está indexado             | True                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-app-data**](c-msds-appdata.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                                                                                                                                                                                                                                                      |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                      |
| System-Only            | False                                                                                                                                                                                                                                                                                   |
| Tiene un único valor       | False                                                                                                                                                                                                                                                                                   |
| Está indexado             | True                                                                                                                                                                                                                                                                                    |
| En el catálogo global      | True                                                                                                                                                                                                                                                                                    |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                                                                                                                                                                                                                                            |
| Range-Lower            | 1                                                                                                                                                                                                                                                                                       |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                     |
| Search-Flags           | 0x00000001                                                                                                                                                                                                                                                                              |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                              |
| Clases usadas en        | [**Versión de la aplicación**](c-applicationversion.md)<br/> [**Punto de conexión**](c-connectionpoint.md)<br/> [**FT-DFS**](c-ftdfs.md)<br/> [**MS-DS-App-Configuration**](c-msds-app-configuration.md)<br/> [**MS-DS-app-data**](c-msds-appdata.md)<br/> |



 

 





