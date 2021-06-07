---
title: Compilación de los archivos IDL proporcionados con el SDK
description: Compilación de los archivos IDL proporcionados con el SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Archivos IDL Administrador de dispositivos Windows Media
- Administrador de dispositivos,archivos IDL
- aplicaciones de escritorio, archivos IDL
- proveedores de servicios, archivos IDL
- guía de programación, archivos IDL
- IDL (archivos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19e3d4ecd7f4f9df7b884cf70de3ba3ad62c7939
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444016"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>Compilación de los archivos IDL proporcionados con el SDK

Windows Media Administrador de dispositivos SDK incluye los archivos de encabezado y los archivos IDL de origen para la mayoría de estos archivos de encabezado. Los archivos de encabezado se encuentran en la \\ carpeta inc en la ruta de instalación del \\ SDK. Los archivos IDL se encuentran en la \\ carpeta \\ idl.

Los encabezados precompilados son mucho más sencillos de usar y varios de los archivos IDL se combinan en un único encabezado proporcionado. Sin embargo, si decide procesar sus propios archivos de encabezado a partir de los archivos IDL proporcionados, en este tema se describen qué archivos IDL crean qué archivos de encabezado y también se describen las dependencias de cada archivo IDL.

**Archivos de encabezado IDL y proporcionados equivalentes**



| **Idl**                                                                                            | **Encabezado proporcionado equivalente**               | **Descripción**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM.idl<br/> WMSP.idl<br/> WMSCP.idl<br/> icomponentauthenticate.idl<br/> | Mswmdm.h                                     | Los cuatro archivos IDL se incluyen en este encabezado proporcionado.<br/> **WMDM.idl** Define todas las interfaces de aplicación y las estructuras, constantes y códigos de error necesarios.<br/> **WMSP.idl** Define todas las interfaces del proveedor de servicios.<br/> **WMSCP.idl** Define todas las interfaces, valores GUID y constantes que requieren los proveedores de contenido seguro.<br/> **icomponentauthenticate.idl Define** la [**interfaz IComponentAuthenticate.**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)<br/> |
| Wmdmlog.idl                                                                                        | Wmdmlog.h<br/> wmdmlog \_ i.c<br/> | Define las interfaces de registro.<br/> Ambos archivos de encabezado proporcionados deben usarse, en lugar de solo el archivo .h, debido a un problema con el archivo IDL.<br/>                                                                                                                                                                                                                                                                                                                                                |
| WMDRMDeviceApp.idl                                                                                 | Wmdrmdeviceapp.h                             | Define las [**interfaces IWMDRMDeviceApp**](iwmdrmdeviceapp.md) e [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) que usan las aplicaciones que actualizan DRM en dispositivos o recuentos de reproducción de medidores en dispositivos.                                                                                                                                                                                                                                                                                                                 |



 

**Dependencias de IDL**

Varios de los archivos IDL proporcionados tienen dependencias de compilación. Si planea compilar los archivos IDL usted mismo, debe procesar estas dependencias externas en el orden que se muestra en la tabla siguiente.



|   Idl                      |   Dependencias                                                                   |
|----------------------------|----------------------------------------------------------------------------------|
| icomponentauthenticate.idl | import "oaidl.idl";<br/> \#include "icomponentauthenticate.idl"<br/> |
| WMDM.idl                   | Sin dependencias externas                                                         |
| WmdmLog.idl                | Sin dependencias externas                                                         |
| WMDRMDeviceApp.idl         | Sin dependencias externas                                                         |
| WMSCP.idl                  | \#incluir "WMDRMDeviceApp.idl"<br/> \#incluir "WMSP.idl"<br/>        |
| WMSP.idl                   | \#incluir "WMDM.idl"                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas comunes para aplicaciones y proveedores de servicios**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





