---
title: Funciones de WIC
description: Esta sección contiene información acerca de las funciones de Windows Imaging Component (WIC).
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ce53f51f439ab5d0a697c824a1d37db7fd755f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907905"
---
# <a name="wic-functions"></a>Funciones de WIC

Esta sección contiene información acerca de las funciones de Windows Imaging Component (WIC).

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                      | Descripción                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*ProgressNotificationCallback*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | Función de devolución de llamada definida por la aplicación llamada cuando se realiza el progreso del componente Codec.<br/>                                                                                                                        |
| [**WICConvertBitmapSource**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | Obtiene un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) en el formato de píxel deseado de un **IWICBitmapSource** determinado.<br/>                                                                           |
| [**WICCreateBitmapFromSection**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | Devuelve un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que está respaldado por los píxeles de un identificador de sección de Windows interfaz de dispositivo gráfico (GDI).<br/>                                                |
| [**WICCreateBitmapFromSectionEx**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | Devuelve un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) que está respaldado por los píxeles de un identificador de sección de GDI.<br/>                                                                                    |
| [**WICGetMetadataContentSize**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | Devuelve el tamaño del contenido de los metadatos que contiene el [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)especificado. Las cuentas de tamaño devueltas para el encabezado y la longitud de los metadatos.<br/> |
| [**WICMapGuidToShortName**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | Obtiene el nombre corto asociado a un GUID determinado.<br/>                                                                                                                                                       |
| [**WICMapSchemaToName**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | Obtiene el nombre asociado a un esquema determinado.<br/>                                                                                                                                                           |
| [**WICMapShortNameToGuid**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | Obtiene el GUID asociado al nombre corto especificado.<br/>                                                                                                                                                     |
| [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | Obtiene un GUID de formato de metadatos para un formato de contenedor especificado y un proveedor que mejor coincida con el contenido de una secuencia determinada.<br/>                                                                            |
| [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | Escribe los metadatos en una secuencia determinada.<br/>                                                                                                                                                                       |
| [Funciones de proxy WIC](wic-proxy-functions.md)<br/>                                  | Esta sección contiene las funciones de proxy de WIC.<br/>                                                                                                                                                             |



 

 

 




