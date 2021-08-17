---
description: Controlador MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Controlador MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23eaf6dd7f0d6713b0db5ba5ed21ba4f7640c1373f23cb0066b0b31f366809cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952214"
---
# <a name="mstape-driver"></a>Controlador MSTape

Este tema se aplica a Windows XP o posterior.

El controlador MSTape admite dispositivos D-VHS y MPEG. Se expone a las aplicaciones como filtro [de captura de vídeo de WDM.](wdm-video-capture-filter.md) Su funcionalidad es similar a la de [MSDV,](msdv-driver.md)el controlador de cámara dv:

-   Aparece en las categorías de filtro "Orígenes de captura de vídeo" (CLSID \_ VideoInputDeviceCategory) y "Dispositivos de representación de streaming de WDM" (AM \_ KSCATEGORY \_ RENDER).
-   Una aplicación puede crear una instancia del filtro mediante la [**interfaz ICreateDevEnum.**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)
-   Tiene un pin de salida para la captura y el transporte desde el dispositivo, y un pin de entrada para el transporte al dispositivo. Solo se puede conectar un pin a la vez.

**Tipos de medios**

El pin de entrada admite un tipo de medio.



| Etiqueta | Value |
|--------------|------------------------------------------------------------|
| Tipo principal   | Secuencia \_ MEDIATYPE                                          |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE                     |
| Tamaño de muestra  | 192 x 256                                                  |
| Bloque de formato | [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md) |



 

El pin de salida admite dos tipos de medios.



| Etiqueta | Value |
|--------------|----------------------------------------|
| Tipo principal   | Secuencia \_ MEDIATYPE                      |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE |
| Tamaño de muestra  | 192 x 256                              |
| Bloque de formato | MPEG2 \_ TRANSPORT \_ STRIDE               |



 



| Etiqueta | Value |
|--------------|----------------------------------------|
| Tipo principal   | Secuencia \_ MEDIATYPE                      |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE |
| Tamaño de muestra  | 188 x 256                              |
| Bloque de formato | **NULL**                               |



 

**Información del dispositivo**

El controlador lee dinámicamente información de la ROM de configuración del dispositivo. La aplicación puede recuperar esta información enlazando el moniker de dispositivo a un bolsa de propiedades y llamando al **método IPropertyBag::Read.**



| Propiedad            | Descripción                                                                                                                                                                         | Tipo de datos           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| UniqueID \_ Low       | Identificador único del dispositivo **(DWORD bajo).**                                                                                                                                            | **long** (VT \_ I4)   |
| UniqueID \_ High      | Identificador único del dispositivo **(DWORD alto)**                                                                                                                                            | **long**            |
| VendorID            | Id. de proveedor.                                                                                                                                                                          | **long**            |
| ModelID             | Identificador del modelo.                                                                                                                                                                           | **long**            |
| VendorText          | Nombre del proveedor.                                                                                                                                                                        | **BSTR** (VT \_ BSTR) |
| ModelText           | Nombre del modelo de dispositivo.                                                                                                                                                                  | **Bstr**            |
| UnitModelText       | Nombre del modelo de unidad; puede ser igual que ModelText.                                                                                                                                      | **Bstr**            |
| DeviceOPcr0Payload  | Carga útil de oPCR (output plug control). Ejemplo: 146 quadlets.                                                                                                                          | **long**            |
| DeviceOPcr0DataRate | Velocidad de datos de oPCR. Ejemplos: 0 (S100), 1 (S200) o 2 (S400).                                                                                                                          | **long**            |
| DeviceClassGUID     | GUID que identifica el controlador del dispositivo. Para MSTape, este valor es `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` . Este GUID se define como MSTapeDeviceGUID en el archivo de encabezado Xprtdefs.h. | **Bstr**            |
| Descripción         | Descripción del dispositivo, tomada del archivo INF. Esta cadena normalmente contiene el nombre de marca del dispositivo.                                                                    | **Bstr**            |



 

El identificador de dispositivo es un entero de 64 bits. El **DWORD bajo se** almacena en la propiedad UniqueID Low y el DWORD alto se almacena \_ en la propiedad UniqueID  \_ High.

Para obtener más información sobre los monikers de dispositivo, [vea Usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Control de una cámara dv](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



