---
title: Funciones de WIC
description: Esta sección contiene información sobre las funciones Windows Imaging Component (WIC).
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ce53f51f439ab5d0a697c824a1d37db7fd755f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251792"
---
# <a name="wic-functions"></a>Funciones de WIC

Esta sección contiene información sobre las funciones Windows Imaging Component (WIC).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                      | Descripción                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*ProgressNotificationCallback*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | Función de devolución de llamada definida por la aplicación a la que se llama cuando se realiza el progreso del componente de códec.<br/>                                                                                                                        |
| [**WICConvertBitmapSource**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | Obtiene un [**elemento IWICBitmapSource en**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) el formato de píxel deseado de un elemento **IWICBitmapSource determinado.**<br/>                                                                           |
| [**WICCreateBitmapFromSection**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | Devuelve un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que está respaldo por los píxeles de un identificador de Windows Interfaz de dispositivo gráfico (GDI).<br/>                                                |
| [**WICCreateBitmapFromSectionEx**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | Devuelve un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que está respaldo por los píxeles de un identificador de sección GDI.<br/>                                                                                    |
| [**WICGetMetadataContentSize**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | Devuelve el tamaño del contenido de metadatos contenido en el [**objeto IWICMetadataWriter especificado.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) El tamaño devuelto tiene en cuenta el encabezado y la longitud de los metadatos.<br/> |
| [**WICMapGuidToShortName**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | Obtiene el nombre corto asociado a un GUID determinado.<br/>                                                                                                                                                       |
| [**WICMapSchemaToName**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | Obtiene el nombre asociado a un esquema determinado.<br/>                                                                                                                                                           |
| [**WICMapShortNameToGuid**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | Obtiene el GUID asociado al nombre corto especificado.<br/>                                                                                                                                                     |
| [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | Obtiene un GUID de formato de metadatos para un proveedor y un formato de contenedor especificados que mejor coincidan con el contenido de una secuencia determinada.<br/>                                                                            |
| [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | Escribe metadatos en una secuencia determinada.<br/>                                                                                                                                                                       |
| [Funciones de proxy de WIC](wic-proxy-functions.md)<br/>                                  | Esta sección contiene las funciones de proxy de WIC.<br/>                                                                                                                                                             |



 

 

 




