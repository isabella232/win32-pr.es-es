---
title: Package-Flags atributo
description: Campo de bits que contiene las marcas de estado de implementación de una aplicación.
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- Package-Flags esquema de AD de atributo
- PackageFlags attribute AD Schema
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd6965b5c39603032bdb673df10026b0eed2a5d5ae838aeb094013d9a5e95dff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923945"
---
# <a name="package-flags-attribute"></a>Package-Flags atributo

Campo de bits que contiene las marcas de estado de implementación de una aplicación.

Este atributo puede ser cero o una combinación de uno o varios de los valores siguientes.

| Valor                 | Descripción                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000004<br/> | La versión no administrada de esta aplicación debe desinstalarse antes de asignarla. **Windows XP con SP1 y versiones posteriores:** Esta marca no se admite.<br/> <br/>                                                                                                                                          |
| 0x00000008<br/> | Se trata de una aplicación publicada.<br/>                                                                                                                                                                                                                                                                    |
| 0x00000010<br/> | Este paquete se implementó después de la versión beta 3 Windows 2000.<br/>                                                                                                                                                                                                                                             |
| 0x00000020<br/> | Esta aplicación se puede instalar con la **característica Agregar** o quitar programas del Panel de control.<br/>                                                                                                                                                                                                 |
| 0x00000040<br/> | Esta aplicación se puede instalar automáticamente a petición.<br/>                                                                                                                                                                                                                                                   |
| 0x00000080<br/> | Esta aplicación está huérfana. Una aplicación publicada puede quedar huérfana si el administrador quita la aplicación de la lista de aplicaciones implementables.<br/>                                                                                                                                    |
| 0x00000100<br/> | Esta aplicación debe tratarse como desinstalada.<br/>                                                                                                                                                                                                                                                  |
| 0x00000200<br/> | Esta aplicación solo está disponible como piloto.<br/>                                                                                                                                                                                                                                                      |
| 0x00000400<br/> | Se trata de una aplicación asignada. El usuario no puede quitar completamente una aplicación asignada. Si el usuario intenta desinstalar  la aplicación con la característica Agregar o quitar programas del Panel de control, la aplicación se volverá a anunciar al equipo cuando se complete la eliminación.<br/> |
| 0x00000800<br/> | Esta aplicación se queda huérfana cuando se quita la directiva. Si el administrador quita la directiva relacionada con esta aplicación, el administrador ya no controlará la implementación de la aplicación, pero la aplicación instalada seguirá funcionando.<br/>                          |
| 0x00001000<br/> | Esta aplicación se desinstala cuando se quita la directiva de implementación.<br/>                                                                                                                                                                                                                              |
| 0x00002000<br/> | Se realizará una instalación completa de las aplicaciones asignadas por el usuario.<br/>                                                                                                                                                                                                                                |
| 0x00004000<br/> | Las versiones anteriores de esta aplicación deben actualizarse a esta versión.<br/>                                                                                                                                                                                                                                |
| 0x00008000<br/> | Este paquete solo admite una interfaz de usuario mínima con una barra de progreso para el proceso de instalación.<br/>                                                                                                                                                                                               |
| 0x00010000<br/> | Se trata de un paquete para versiones de 32 bits de Windows que no se deben ejecutar en Windows XP Professional x64 Edition o versiones de 64 bits de Windows Server 2003.<br/>                                                                                                                                      |
| 0x00020000<br/> | Este paquete es adecuado para cualquier lenguaje.<br/>                                                                                                                                                                                                                                                          |
| 0x00040000<br/> | Este paquete tiene actualizaciones.<br/>                                                                                                                                                                                                                                                                          |
| 0x00080000<br/> | Este paquete tiene una interfaz de usuario completa para el proceso de instalación.<br/>                                                                                                                                                                                                                                |
| 0x00100000<br/> | Las clases de esta aplicación se conservan durante una operación de reimplementación si la aplicación se vuelve a implementar en un cambio de nombre de dominio.<br/>                                                                                                                                                                       |



 



| Entrada | Valor |
|-------------------|--------------------------------------|
| CN                | Package-Flags                        |
| Ldap-Display-Name | packageFlags                         |
| Size              | \-                                   |
| Actualizar privilegios  | \-                                   |
| Frecuencia de actualización  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.327               |
| System-Id-Guid    | 7d6c0e99-7e20-11d0-afd6-00c04fd930c9 |
| Syntax            | [**Enumeración**](s-enumeration.md) |



## <a name="implementations"></a>Implementaciones

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| Id. de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Es de un solo valor       | Verdadero                                                             |
| Está indexado             | Verdadero                                                             |
| En el catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Registro de paquetes**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| Id. de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Es de un solo valor       | Verdadero                                                             |
| Está indexado             | Verdadero                                                             |
| En el catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Registro de paquetes**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| Id. de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Es de un solo valor       | Verdadero                                                             |
| Está indexado             | Verdadero                                                             |
| En el catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Registro de paquetes**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| Id. de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Es de un solo valor       | Verdadero                                                             |
| Está indexado             | Verdadero                                                             |
| En el catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Registro de paquetes**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| Id. de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Es de un solo valor       | Verdadero                                                             |
| Está indexado             | Verdadero                                                             |
| En el catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Registro de paquetes**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Entrada | Valor |
|------------------------|------------------------------------------------------------------|
| Id. de vínculo                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| Es de un solo valor       | Verdadero                                                             |
| Está indexado             | Verdadero                                                             |
| En el catálogo global      | Falso                                                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Clases usadas en        | [**Registro de paquetes**](c-packageregistration.md)<br/> |



 

 





