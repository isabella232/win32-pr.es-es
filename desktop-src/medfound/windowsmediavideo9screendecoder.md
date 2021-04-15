---
description: El descodificador de pantalla de Windows Media Video 9 descodifica los flujos codificados por el codificador de pantalla de Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Descodificador de pantalla de Windows Media Video 9 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd9dcdce920fa39437edb769fd575a7d7a0d68fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708860"
---
# <a name="windows-media-video-9-screen-decoder"></a>Descodificador de pantalla de Windows Media Video 9

El descodificador de pantalla de Windows Media Video 9 descodifica los flujos codificados por el [**codificador de pantalla de Windows Media Video 9**](windowsmediavideo9screenencoder.md).

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) para el descodificador de pantalla de Windows Media Video 9 se representa mediante la constante **\_ CMSSCDecMediaObject de CLSID**. Puede crear una instancia del descodificador llamando a **CoCreateInstance**.

## <a name="input-types"></a>Tipos de entrada

El código de cuatro caracteres (FOURCC) para el contenido codificado en pantalla de la versión 9 de Windows Media Video es "MSS2".

El descodificador de pantalla de la versión 9 admite los siguientes tipos de entrada.

-   MEDIASUBTYPE \_ MSS2

## <a name="output-types"></a>Tipos de salida

El descodificador de pantalla de la versión 9 admite los siguientes tipos de salida cuando se usa como un objeto multimedia de DirectX (DMO).

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

El descodificador de pantalla de la versión 9 admite los siguientes tipos de salida cuando se utiliza como una transformación de Media Foundation (MFT).

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="remarks"></a>Observaciones

Un objeto de descodificador de pantalla expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como un objeto multimedia de DirectX (DMO) y exponga la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto pueda usarse como una transformación de Media Foundation (MFT).

Un descodificador de pantalla se comporta como un DMO o una MFT en función de las interfaces que se obtienen y de la versión de Windows que se está ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador de pantalla se comporta como un DMO o MFT.



| Sistema operativo            | Comportamiento del descodificador                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un descodificador de pantalla de Windows Media siempre se comporta como DMO.                                                                                                                 |
| Windows Vista y Windows 7 | De forma predeterminada, un descodificador de pantalla de Windows Media se comporta como un DMO. Si obtiene una interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un descodificador de pantalla, se comporta como una MFT. |



 

Puede usar el mismo CLSID (CLSID \_ CMSSCDecMediaObject) para crear el descodificador de pantalla de la versión 7 y el descodificador de pantalla de la versión 9. El FOURCC para el contenido codificado de la versión 7 de la pantalla Windows Media Video es "MSS1". El descodificador de pantalla de la versión 7 admite el \_ tipo de entrada MSS1 de MEDIASUBTYPE.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Remoto<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Encabezado<br/> | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos Codec](codecobjects.md)
</dt> <dt>

[Implementación de códecs](codecimplementation.md)
</dt> <dt>

[Usar el códec de pantalla de Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Codificador de pantalla de Windows Media Video 9](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
