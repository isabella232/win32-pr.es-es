---
description: El descodificador MPEG4 v1/v2 de Windows Media descodifica transmisiones de vídeo MPEG4 v1/v2.
ms.assetid: 63b32972-1003-4291-bfdd-cc0cb8d65430
title: Descodificador MPEG4 v1/v2 de Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b14cf22e29c1266ac9bb3593375ee4485d79df2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717343"
---
# <a name="windows-media-mpeg4-v1v2-decoder"></a>Descodificador MPEG4 v1/v2 de Windows Media

El descodificador MPEG4 v1/v2 de Windows Media descodifica transmisiones de vídeo MPEG4 v1/v2.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador MPEG4 v1/v2 de Windows Media se representa mediante la constante **\_ CMpeg4DecMediaObject de CLSID**. Puede crear una instancia del descodificador MPEG4 v1/v2 llamando a **CoCreateInstance**.

## <a name="formats"></a>Formatos

El descodificador MPEG4 v1/v2 de Windows Media admite los siguientes tipos de medios de entrada.

-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ MPG4
-   MEDIASUBTYPE \_ mp42
-   MEDIASUBTYPE \_ mp42

El descodificador MPEG4 v1/v2 de Windows Media admite los siguientes subtipos de medios de salida cuando actúa como un objeto multimedia de DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

El descodificador MPEG4 v1/v2 de Windows Media admite los siguientes subtipos de medios de salida cuando actúa como una transformación de Media Foundation (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Observaciones

El objeto descodificador MPEG4 v1/v2 de Windows Media expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT). El objeto tiene el mismo identificador de clase (CLSID) independientemente de si actúa como un DMO o MFT.

Un descodificador MPEG4 v1/v2 se comporta como un DMO o una MFT en función de las interfaces que se obtengan y de la versión de Windows que se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador MPEG4 v1/v2 se comporta como DMO o MFT.



| Sistema operativo            | Comportamiento del descodificador                                                                                                                                                                |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un descodificador MPEG4 v1/v2 siempre se comporta como DMO.                                                                                                                                 |
| Windows Vista y Windows 7 | De forma predeterminada, un descodificador MPEG4 v1/v2 se comporta como un DMO. Si obtiene una interfaz de [GUID de subtipo de vídeo](video-subtype-guids.md) en un descodificador MPEG4 v1/v2, se comporta como una MFT. |



 

Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un descodificador actúa como un DMO o una MFT. Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un descodificador actúa como un DMO o una MFT. Para obtener información sobre los GUID que representan subtipos de vídeo, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MPG4DECD.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
