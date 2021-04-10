---
description: Controlador MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Controlador MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906335"
---
# <a name="mstape-driver"></a>Controlador MSTape

Este tema se aplica a Windows XP o posterior.

El controlador MSTape admite dispositivos de vídeo D-VHS y MPEG camcorder. Se expone a las aplicaciones como el filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) . Su funcionalidad es similar a la de [MSDV](msdv-driver.md), el controlador de videocámara DV:

-   Aparece en las categorías de filtro "orígenes de captura de vídeo" (CLSID \_ VideoInputDeviceCategory) y "dispositivos de representación de transmisión por secuencias WDM" ( \_ KSCATEGORY \_ representar).
-   Una aplicación puede crear una instancia del filtro mediante la interfaz [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .
-   Tiene un PIN de salida para la captura y el transporte desde el dispositivo y un PIN de entrada para el transporte al dispositivo. Solo se puede conectar un PIN a la vez.

**Tipos de medios**

El PIN de entrada admite un tipo de medio.



|              |                                                            |
|--------------|------------------------------------------------------------|
| Tipo principal   | \_Secuencia MEDIATYPE                                          |
| Subtype      | \_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_                     |
| Tamaño de muestra  | 192 x 256                                                  |
| Bloque de formato | [**\_Intervalo de transporte de MPEG2 \_**](mpeg2-transport-stride.md) |



 

El PIN de salida admite dos tipos de medios.



|              |                                        |
|--------------|----------------------------------------|
| Tipo principal   | \_Secuencia MEDIATYPE                      |
| Subtype      | \_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_ |
| Tamaño de muestra  | 192 x 256                              |
| Bloque de formato | \_Intervalo de transporte de MPEG2 \_               |



 



|              |                                        |
|--------------|----------------------------------------|
| Tipo principal   | \_Secuencia MEDIATYPE                      |
| Subtype      | \_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_ |
| Tamaño de muestra  | 188 x 256                              |
| Bloque de formato | **NULL**                               |



 

**Información del dispositivo**

El controlador Lee dinámicamente la información del ROM de configuración del dispositivo. La aplicación puede recuperar esta información enlazando el moniker del dispositivo a un contenedor de propiedades y llamando al método **IPropertyBag:: Read** .



| Propiedad            | Descripción                                                                                                                                                                         | Tipo de datos           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| UniqueID \_ bajo       | IDENTIFICADOR único del dispositivo ( **DWORD** inferior).                                                                                                                                            | **Long** (VT \_ I4)   |
| UniqueID \_ alto      | IDENTIFICADOR único del dispositivo ( **DWORD** alto)                                                                                                                                            | **long**            |
| VendorID            | IDENTIFICADOR del proveedor.                                                                                                                                                                          | **long**            |
| ModelID             | Identificador del modelo.                                                                                                                                                                           | **long**            |
| VendorText          | Nombre del proveedor.                                                                                                                                                                        | **BSTR** (VT \_ BSTR) |
| ModelText           | Nombre del modelo de dispositivo.                                                                                                                                                                  | **UTILICEN**            |
| UnitModelText       | Nombre del modelo de unidad; puede ser igual que ModelText.                                                                                                                                      | **UTILICEN**            |
| DeviceOPcr0Payload  | carga de oPCR (control de conector de salida). Ejemplo: 146 quadlets.                                                                                                                          | **long**            |
| DeviceOPcr0DataRate | velocidad de datos oPCR. Ejemplos: 0 (S100), 1 (S200) o 2 (S400).                                                                                                                          | **long**            |
| DeviceClassGUID     | GUID que identifica el controlador de dispositivo. En el caso de MSTape, este valor es `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` . Este GUID se define como MSTapeDeviceGUID en el archivo de encabezado Xprtdefs. h. | **UTILICEN**            |
| Descripción         | Descripción del dispositivo, tomada del archivo INF. Esta cadena normalmente contiene el nombre de marca del dispositivo.                                                                    | **UTILICEN**            |



 

El identificador de dispositivo es un entero de 64 bits. El **valor DWORD** inferior se almacena en la \_ propiedad UniqueID Low y el **valor DWORD** superior se almacena en la \_ propiedad UniqueID High.

Para obtener más información acerca de los monikers de dispositivo, consulte [usar el enumerador de dispositivos del sistema](using-the-system-device-enumerator.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Control de una videocámara DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



