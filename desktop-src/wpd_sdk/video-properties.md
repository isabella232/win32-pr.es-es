---
description: Windows Dispositivos portátiles admite las siguientes propiedades de vídeo.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Propiedades de vídeo (PortableDevice.h)
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
ms.openlocfilehash: 6e7bbab3416f50a95d2ae29e2be0ef5ecdcad6eed0112f940e5c34b593f2b79a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083389"
---
# <a name="video-properties"></a>Propiedades de vídeo

Windows Dispositivos portátiles admite las siguientes propiedades de vídeo.



| Propiedad                                         | VarType        | Descripción                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ VIDEO \_ AUTHOR**                           | **VT \_ LPWSTR** | Autor del archivo de vídeo.                                                                                                                                                                                                                           |
| **VELOCIDAD DE BITS \_ \_ DE VÍDEO WPD**                          | **VT \_ UI4**    | Velocidad de bits del archivo de vídeo.                                                                                                                                                                                                                         |
| **TAMAÑO DEL BÚFER \_ \_ DE VÍDEO WPD \_**                     | **VT \_ UI4**    | Valor que especifica el tamaño de búfer de vídeo necesario para representar este archivo.                                                                                                                                                                              |
| **CRÉDITOS DE VÍDEO DE WPD \_ \_**                          | **VT \_ LPWSTR** | Créditos que enumeran el elenco y la cuadrilla del vídeo.                                                                                                                                                                                                    |
| **WPD \_ VIDEO \_ FOURCC \_ CODE**                     | **VT \_ DWORD**  | Código FourCC registrado que indica el códec que se usó para el archivo de vídeo. Para obtener una lista de formatos FourCC, consulte el artículo [Códigos FOURCC](https://msdn2.microsoft.com/library/ms867195.aspx) registrados y formatos WAVE en el sitio web de MSDN. |
| **VELOCIDAD DE \_ \_ FOTOGRAMAS DE VÍDEO WPD**                        | **VT \_ UI4**    | Velocidad de fotogramas del archivo de vídeo, en fotogramas/segundo x 1000. Por ejemplo, una velocidad de fotogramas de 29,97 se representa como 29970.                                                                                                                                 |
| **GÉNERO DE \_ VÍDEO WPD \_**                            | **VT \_ LPWSTR** | Género de este archivo de vídeo. No hay definiciones de género estándar.                                                                                                                                                                                  |
| **DISTANCIA ENTRE \_ \_ FOTOGRAMAS CLAVE \_ DE VÍDEO WPD \_**             | **VT \_ UI4**    | Intervalo entre fotogramas clave, en milisegundos.                                                                                                                                                                                                       |
| **CONFIGURACIÓN DE CALIDAD \_ DE \_ VÍDEO WPD \_**                 | **VT \_ UI4**    | La configuración de calidad del archivo de vídeo. Esto depende del códec.                                                                                                                                                                                        |
| **WPD \_ VIDEO \_ RECORDEDTV \_ CHANNEL \_ NUMBER**      | **VT \_ UI4**    | Número de canal de televisión desde el que se registró el vídeo.                                                                                                                                                                                              |
| **DESCRIPCIÓN DEL \_ PROGRAMA \_ WPD VIDEO RECORDEDTV \_ \_** | **VT \_ LPWSTR** | Descripción del programa de televisión grabado.                                                                                                                                                                                                       |
| **WPD \_ VIDEO \_ RECORDEDTV \_ REPEAT**               | **VT \_ BOOL**   | Valor booleano que especifica si el programa de televisión era una repetición.                                                                                                                                                                     |
| **WPD \_ VIDEO \_ RECORDEDTV \_ STATION \_ NAME**        | **VT \_ LPWSTR** | La estación de televisión desde la que se registró el vídeo.                                                                                                                                                                                                |
| **TIPO DE \_ EXAMEN \_ DE VÍDEO \_ WPD**                       | **VT \_ UI4**    | Enumerador [**WPD \_ VIDEO SCAN \_ \_ TYPES**](wpd-video-scan-types.md) que especifica el entrelazado del archivo de vídeo.                                                                                                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




