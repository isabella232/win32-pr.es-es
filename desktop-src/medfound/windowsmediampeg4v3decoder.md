---
description: El descodificador MPEG-4 V3 de Windows Media descodifica secuencias de vídeo MPEG-4 V3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Descodificador MPEG-4 V3 de Windows Media (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ee98a0a3c4b221da6f2000e32d4c75bc3e3a93b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105717359"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Descodificador MPEG-4 V3 de Windows Media

El descodificador MPEG-4 V3 de Windows Media descodifica secuencias de vídeo MPEG-4 V3.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador MPEG-4 V3 de Windows se representa mediante la constante **\_ CMpeg43DecMediaObject de CLSID**. Puede crear una instancia del descodificador MPEG-4 V3 llamando a **CoCreateInstance**.

## <a name="formats"></a>Formatos

El descodificador MPEG-4 V3 de Windows Media admite los siguientes tipos de medios de entrada.

-   MEDIASUBTYPE \_ mp43
-   MEDIASUBTYPE \_ mp43

El descodificador MPEG-4 V3 de Windows Media admite los siguientes subtipos de medios de salida cuando actúa como un objeto multimedia de DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

El descodificador MPEG-4 V3 de Windows Media admite los siguientes subtipos de medios de salida cuando actúa como una transformación de Media Foundation (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Observaciones

El objeto descodificador MPEG-4 V3 de Windows Media expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT). El objeto tiene el mismo identificador de clase (CLSID) independientemente de si actúa como un DMO o MFT.

El descodificador MPEG-4 V3 se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador MPEG-4 V3 se comporta como DMO o MFT.



| Sistema operativo            | Comportamiento del descodificador                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | El descodificador MPEG-4 V3 siempre se comporta como DMO.                                                                                                                      |
| Windows Vista y Windows 7 | De forma predeterminada, el descodificador MPEG-4 V3 se comporta como un DMO. Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en el descodificador MPEG-4 V3, se comporta como una MFT. |



 

Los identificadores únicos globales (GUID) para los subtipos multimedia RGB difieren en función de si un descodificador actúa como un DMO o una MFT. Los GUID para los subtipos de medios que no son RGB son los mismos, independientemente de si un descodificador actúa como un DMO o una MFT. Para obtener información sobre los GUID que representan subtipos de medios, consulte [GUID de subtipo de vídeo](video-subtype-guids.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> </dl>

 

 
