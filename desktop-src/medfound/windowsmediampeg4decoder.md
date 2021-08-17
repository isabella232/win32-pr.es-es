---
description: El Windows de vídeo MPEG4 V1/V2 de Media descodifica secuencias de vídeo MPEG4 V1/V2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Windows Descodificador MPEG4 V1/V2 multimedia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c55d5c64cec2a0ad08978064d40c26267d7729adeee9a9f148c8e682ba168509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100937"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Windows Descodificador MPEG4 V1/V2 multimedia

El Windows de vídeo MPEG4 V1/V2 de Media descodifica secuencias de vídeo MPEG4 V1/V2.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador Windows Media MPEG4 V1/V2 se representa mediante la constante **CLSID \_ CMpeg4DecMediaObject**. Puede crear una instancia del descodificador MPEG4 V1/V2 llamando a **CoCreateInstance**.

## <a name="formats"></a>Formatos

El Windows media MPEG4 V1/V2 admite los siguientes tipos de medios de entrada.

-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ mpg4
-   MEDIASUBTYPE \_ MP42
-   MEDIASUBTYPE \_ mp42

El descodificador Windows Media MPEG4 V1/V2 admite los siguientes subtipos de medios de salida cuando actúa como objeto multimedia DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

El descodificador Windows Media MPEG4 V1/V2 admite los siguientes subtipos de medios de salida cuando actúa como una transformación de Media Foundation (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Comentarios

El objeto descodificador Windows Media MPEG4 V1/V2 expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como objeto multimedia DirectX (DMO) y exponga la interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT). El objeto tiene el mismo identificador de clase (CLSID) independientemente de si actúa como DMO o MFT.

Un descodificador MPEG4 V1/V2 se comporta como un DMO o MFT en función de las interfaces que obtenga y la versión de Windows se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador MPEG4 V1/V2 se comporta como DMO o MFT.



| Sistema operativo            | Comportamiento del descodificador                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un descodificador MPEG4 V1/V2 siempre se comporta como un DMO.                                                                                                                                 |
| Windows Vista y Windows 7 | De forma predeterminada, un descodificador MPEG4 V1/V2 se comporta como un DMO. Si obtiene una interfaz DE GUID [de subtipo de](video-subtype-guids.md) vídeo en un descodificador MPEG4 V1/V2, se comporta como MFT. |



 

Los identificadores únicos globales (GUID) de los subtipos de medios RGB difieren en función de si un descodificador actúa como DMO o MFT. Los GUID de los subtipos multimedia no RGB son los mismos, independientemente de si un descodificador actúa como DMO o MFT. Para obtener información sobre los GUID que representan subtipos de vídeo, vea [GUID de subtipo de vídeo.](video-subtype-guids.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
