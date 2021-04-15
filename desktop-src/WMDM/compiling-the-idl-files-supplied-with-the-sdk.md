---
title: Compilar los archivos IDL suministrados con el SDK
description: Compilar los archivos IDL suministrados con el SDK
ms.assetid: 718528eb-6ac4-466d-8dfd-d6f2b6c30303
keywords:
- Administrador de dispositivos de Windows Media, archivos IDL
- Administrador de dispositivos, archivos IDL
- aplicaciones de escritorio, archivos IDL
- proveedores de servicios, archivos IDL
- Guía de programación, archivos IDL
- IDL (archivos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e24eec21a481de4603392942b40013ec55086c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695380"
---
# <a name="compiling-the-idl-files-supplied-with-the-sdk"></a>Compilar los archivos IDL suministrados con el SDK

El SDK de Administrador de dispositivos de Windows Media incluye tanto archivos de encabezado como archivos IDL de origen para la mayoría de estos archivos de encabezado. Los archivos de encabezado se encuentran en \\ la \\ carpeta Inc de la ruta de instalación del SDK. Los archivos IDL se encuentran en la \\ \\ carpeta IDL.

Los encabezados precompilados son mucho más fáciles de usar y varios de los archivos IDL se combinan en un único encabezado proporcionado. Sin embargo, si decide procesar sus propios archivos de encabezado a partir de los archivos IDL proporcionados, en este tema se describen los archivos IDL que crean los archivos de encabezado y también se describen las dependencias de cada archivo IDL.

**Archivos de encabezado IDL y proporcionados equivalentes**



| **IDL**                                                                                            | **Encabezado proporcionado equivalente**               | **Descripción**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------------|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WMDM. idl<br/> WMSP. idl<br/> WMSCP. idl<br/> icomponentauthenticate. idl<br/> | Mswmdm. h                                     | Los cuatro archivos IDL se incluyen en este único encabezado proporcionado.<br/> **WMDM. idl** define todas las interfaces de aplicación y las estructuras, constantes y códigos de error necesarios.<br/> **WMSP. idl** define todas las interfaces del proveedor de servicios.<br/> **WMSCP. idl** define todas las interfaces, los valores de GUID y las constantes que requieren los proveedores de contenido seguro.<br/> **icomponentauthenticate. idl** define la interfaz [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) .<br/> |
| Wmdmlog. idl                                                                                        | Wmdmlog. h<br/> wmdmlog \_ c<br/> | Define las interfaces de registro.<br/> Se deben usar ambos archivos de encabezado suministrados, en lugar de solo el archivo. h, debido a un problema con el archivo IDL.<br/>                                                                                                                                                                                                                                                                                                                                                |
| WMDRMDeviceApp. idl                                                                                 | Wmdrmdeviceapp. h                             | Define las interfaces [**IWMDRMDeviceApp**](iwmdrmdeviceapp.md) y [**IWMDRMDeviceApp2**](iwmdrmdeviceapp2.md) que usan las aplicaciones que actualizan DRM en dispositivos o recuentos de las métricas en los dispositivos.                                                                                                                                                                                                                                                                                                                 |



 

**Dependencias IDL**

Varios de los archivos IDL proporcionados tienen dependencias de compilación. Si tiene previsto compilar los archivos IDL personalmente, debe procesar estas dependencias externas en el orden que se muestra en la tabla siguiente.



|                            |                                                                                  |
|----------------------------|----------------------------------------------------------------------------------|
| **IDL**                    | **Dependencias**                                                                 |
| icomponentauthenticate. idl | importar "oaidl. idl";<br/> \#incluir "icomponentauthenticate. idl"<br/> |
| WMDM. idl                   | No hay dependencias externas                                                         |
| WmdmLog. idl                | No hay dependencias externas                                                         |
| WMDRMDeviceApp. idl         | No hay dependencias externas                                                         |
| WMSCP. idl                  | \#incluir "WMDRMDeviceApp. idl"<br/> \#incluir "WMSP. idl"<br/>        |
| WMSP. idl                   | \#incluir "WMDM. idl"                                                             |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas comunes a las aplicaciones y proveedores de servicios**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 





