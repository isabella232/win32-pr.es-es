---
description: El Windows descodificador MPEG-4 V3 de Media descodifica secuencias de vídeo MPEG-4 V3.
ms.assetid: 5143b0cc-c171-46af-8d7f-4d029af71fb4
title: Windows Descodificador MPEG-4 V3 multimedia (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 975351d04b0876b5f1793d442e41d54a585062bd1fed778902fee5c4c83dcd6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119100926"
---
# <a name="windows-media-mpeg-4-v3-decoder"></a>Windows Descodificador MPEG-4 V3 multimedia

El Windows descodificador MPEG-4 V3 de Media descodifica secuencias de vídeo MPEG-4 V3.

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del Windows descodificador MPEG-4 V3 se representa mediante la constante **CLSID \_ CMpeg43DecMediaObject**. Puede crear una instancia del descodificador MPEG-4 V3 llamando a **CoCreateInstance**.

## <a name="formats"></a>Formatos

El Windows media MPEG-4 V3 admite los siguientes tipos de medios de entrada.

-   MEDIASUBTYPE \_ MP43
-   MEDIASUBTYPE \_ mp43

El descodificador Windows Media MPEG-4 V3 admite los siguientes subtipos de medios de salida cuando actúa como objeto multimedia DirectX (DMO).

-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555

El descodificador Windows Media MPEG-4 V3 admite los siguientes subtipos de medios de salida cuando actúa como una transformación de Media Foundation (MFT).

-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555

## <a name="remarks"></a>Comentarios

El objeto descodificador Windows Media MPEG-4 V3 expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como objeto multimedia DirectX (DMO) y exponga la interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT). El objeto tiene el mismo identificador de clase (CLSID) independientemente de si actúa como DMO o MFT.

El descodificador MPEG-4 V3 se comporta como DMO o MFT en función de las interfaces que obtenga y la versión de Windows se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador MPEG-4 V3 se comporta como DMO o MFT.



| Sistema operativo            | Comportamiento del descodificador                                                                                                                                                    |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | El descodificador MPEG-4 V3 siempre se comporta como un DMO.                                                                                                                      |
| Windows Vista y Windows 7 | De forma predeterminada, el descodificador MPEG-4 V3 se comporta como un DMO. Si obtiene una interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en el descodificador MPEG-4 V3, se comporta como un MFT. |



 

Los identificadores únicos globales (GUID) de los subtipos de medios RGB difieren en función de si un descodificador actúa como DMO o MFT. Los GUID de los subtipos multimedia no RGB son los mismos, independientemente de si un descodificador actúa como DMO o MFT. Para obtener información sobre los GUID que representan subtipos multimedia, vea [GUID de subtipo de vídeo.](video-subtype-guids.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MP43DECD.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> </dl>

 

 
