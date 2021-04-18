---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de vídeo.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Propiedades de vídeo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718708"
---
# <a name="video-properties"></a>Propiedades de vídeo

Los dispositivos portátiles de Windows admiten las siguientes propiedades de vídeo.



| Propiedad                                         | VarType        | Descripción                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_autor de vídeo de WPD \_**                           | **VT \_ LPWStr** | Autor del archivo de vídeo.                                                                                                                                                                                                                           |
| **velocidad de bits de \_ vídeo WPD \_**                          | **VT \_ UI4**    | La velocidad de bits del archivo de vídeo.                                                                                                                                                                                                                         |
| **\_tamaño del \_ búfer de vídeo de WPD \_**                     | **VT \_ UI4**    | Valor que especifica el tamaño de búfer de vídeo necesario para representar este archivo.                                                                                                                                                                              |
| **\_créditos de vídeo de WPD \_**                          | **VT \_ LPWStr** | Los créditos que enumeran la conversión y el tripulante para el vídeo.                                                                                                                                                                                                    |
| **\_ \_ código FourCC de vídeo de WPD \_**                     | **VT \_ DWORD**  | Código de FourCC registrado que indica el códec que se usó para el archivo de vídeo. Para obtener una lista de formatos FourCC, vea el artículo [registro de códigos FourCC y formatos de onda](https://msdn2.microsoft.com/library/ms867195.aspx) en el sitio web de MSDN. |
| **fotogramas de vídeo de WPD \_ \_**                        | **VT \_ UI4**    | La velocidad de fotogramas del archivo de vídeo, en fotogramas/segundo x 1.000. Por ejemplo, una velocidad de fotogramas de 29,97 se representa como 29970.                                                                                                                                 |
| **\_género de vídeo de WPD \_**                            | **VT \_ LPWStr** | Género de este archivo de vídeo. No hay ninguna definición de género estándar.                                                                                                                                                                                  |
| **\_distancia de \_ \_ fotogramas de clave de vídeo de WPD \_**             | **VT \_ UI4**    | Intervalo entre fotogramas clave, en milisegundos.                                                                                                                                                                                                       |
| **\_configuración de \_ calidad de vídeo de WPD \_**                 | **VT \_ UI4**    | La configuración de calidad para el archivo de vídeo. Esto depende del códec.                                                                                                                                                                                        |
| **\_número de \_ canal de RECORDEDTV de vídeo de WPD \_ \_**      | **VT \_ UI4**    | El número de canal de televisión desde el que se grabó el vídeo.                                                                                                                                                                                              |
| **\_Descripción del \_ \_ programa RECORDEDTV de vídeo \_ de WPD** | **VT \_ LPWStr** | Descripción del programa de televisión grabado.                                                                                                                                                                                                       |
| **RECORDEDTV de vídeo de WPD \_ \_ \_ repite**               | **VT \_ bool**   | Valor booleano que especifica si el programa de televisión era una repetición que se muestra.                                                                                                                                                                     |
| **\_nombre de \_ la \_ estación \_ RECORDEDTV de vídeo de WPD**        | **VT \_ LPWStr** | La estación de televisión desde la que se grabó el vídeo.                                                                                                                                                                                                |
| **\_tipo de \_ examen de vídeo de WPD \_**                       | **VT \_ UI4**    | Un enumerador de tipos de análisis de vídeo de WPD que especifica el entrelazado del archivo de vídeo. [**\_ \_ \_**](wpd-video-scan-types.md)                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




