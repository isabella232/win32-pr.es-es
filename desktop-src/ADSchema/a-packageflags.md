---
title: Package-Flags atributo)
description: Un campo de bits que contiene las marcas de estado de implementación de una aplicación.
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- Esquema de AD de atributo de Package-Flags
- packageFlags esquema de AD de atributos
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7202124bdeac22347d727638dc564a145599e9c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/14/2020
ms.locfileid: "103804879"
---
# <a name="package-flags-attribute"></a>Package-Flags atributo)

Un campo de bits que contiene las marcas de estado de implementación de una aplicación.

Este atributo puede ser cero o una combinación de uno o varios de los valores siguientes.

| Value                 | Descripción                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000004<br/> | La versión no administrada de esta aplicación debe desinstalarse antes de la asignación. **Windows XP con SP1 y versiones posteriores:** Esta marca no se admite.<br/> <br/>                                                                                                                                          |
| 0x00000008<br/> | Se trata de una aplicación publicada.<br/>                                                                                                                                                                                                                                                                    |
| 0x00000010<br/> | Este paquete se implementó después de la versión beta 3 de Windows 2000.<br/>                                                                                                                                                                                                                                             |
| 0x00000020<br/> | Esta aplicación se puede instalar con la característica **Agregar o quitar programas** del panel de control.<br/>                                                                                                                                                                                                 |
| 0x00000040<br/> | Esta aplicación se puede instalar automáticamente a petición.<br/>                                                                                                                                                                                                                                                   |
| 0x00000080<br/> | Esta aplicación está huérfana. Una aplicación publicada puede quedar huérfana si el administrador quita la aplicación de la lista de aplicaciones que se pueden implementar.<br/>                                                                                                                                    |
| 0x00000100<br/> | Esta aplicación se debe tratar como desinstalada.<br/>                                                                                                                                                                                                                                                  |
| 0x00000200<br/> | Esta aplicación solo está disponible como prueba piloto.<br/>                                                                                                                                                                                                                                                      |
| 0x00000400<br/> | Se trata de una aplicación asignada. El usuario no puede quitar completamente una aplicación asignada. Si el usuario intenta desinstalar la aplicación con la característica **Agregar o quitar programas** del panel de control, la aplicación se volverá a anunciar en el equipo cuando se complete la eliminación.<br/> |
| 0x00000800<br/> | Esta aplicación está huérfana cuando se quita la Directiva. Si el administrador quita la Directiva relacionada con esta aplicación, el administrador ya no controlará la implementación de la aplicación, pero la aplicación instalada seguirá funcionando.<br/>                          |
| 0x00001000<br/> | Esta aplicación se desinstala cuando se quita la Directiva de implementación.<br/>                                                                                                                                                                                                                              |
| 0x00002000<br/> | Se llevará A cabo una instalación completa de las aplicaciones asignadas por el usuario.<br/>                                                                                                                                                                                                                                |
| 0x00004000<br/> | Las versiones anteriores de esta aplicación se deben actualizar a esta versión.<br/>                                                                                                                                                                                                                                |
| 0x00008000<br/> | Este paquete solo admite una interfaz de usuario mínima con una barra de progreso para el proceso de instalación.<br/>                                                                                                                                                                                               |
| 0x00010000<br/> | Se trata de un paquete para las versiones de 32 bits de Windows que no se deben ejecutar en las versiones de Windows XP Professional x64 Edition o de 64 bits de Windows Server 2003.<br/>                                                                                                                                      |
| 0x00020000<br/> | Este paquete es adecuado para cualquier lenguaje.<br/>                                                                                                                                                                                                                                                          |
| 0x00040000<br/> | Este paquete tiene actualizaciones.<br/>                                                                                                                                                                                                                                                                          |
| 0x00080000<br/> | Este paquete tiene una interfaz de usuario completa para el proceso de instalación.<br/>                                                                                                                                                                                                                                |
| 0x00100000<br/> | Las clases de esta aplicación se conservan durante una operación de volver a implementar si se vuelve a implementar la aplicación en un cambio de nombre de dominio.<br/>                                                                                                                                                                       |



 



| Entrada | Value |
|-------------------|--------------------------------------|
| CN                | Package-Flags                        |
| Nombre para mostrar de LDAP | packageFlags                         |
| Tamaño              | \-                                   |
| Actualizar privilegio  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.327               |
| System-ID-GUID    | 7d6c0e99-7e20-11d0-afd6-00c04fd930c9 |
| Sintaxis            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Value |
|------------------------|------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Tiene un único valor       | True                                                             |
| Está indexado             | True                                                             |
| En el catálogo global      | False                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Paquete-registro**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Value |
|------------------------|------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Tiene un único valor       | True                                                             |
| Está indexado             | True                                                             |
| En el catálogo global      | False                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Paquete-registro**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Tiene un único valor       | True                                                             |
| Está indexado             | True                                                             |
| En el catálogo global      | False                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Paquete-registro**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Value |
|------------------------|------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Tiene un único valor       | True                                                             |
| Está indexado             | True                                                             |
| En el catálogo global      | False                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Paquete-registro**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Value |
|------------------------|------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Tiene un único valor       | True                                                             |
| Está indexado             | True                                                             |
| En el catálogo global      | False                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Paquete-registro**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Value |
|------------------------|------------------------------------------------------------------|
| Identificador de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | False                                                            |
| Tiene un único valor       | True                                                             |
| Está indexado             | True                                                             |
| En el catálogo global      | False                                                            |
| Descriptor de NT-Security- | O:BAG: BAD: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Paquete-registro**](c-packageregistration.md)<br/> |



 

 





