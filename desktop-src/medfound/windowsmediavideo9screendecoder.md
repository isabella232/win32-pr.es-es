---
description: El descodificador Windows Media Video 9 Screen descodifica secuencias codificadas por el codificador de pantalla Windows Media Video 9.
ms.assetid: 6688a830-7a54-4f58-947e-26013e191b5f
title: Windows Descodificador de pantalla de Vídeo multimedia 9 (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c2e081423c4c5efc2d44fdf78c7c6a94a00dae86d40d761a06ab0de07fa5d1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462395"
---
# <a name="windows-media-video-9-screen-decoder"></a>Windows Descodificador de pantalla de Vídeo multimedia 9

El descodificador Windows Media Video 9 Screen descodifica las secuencias codificadas por el codificador de pantalla Windows [**Media Video 9.**](windowsmediavideo9screenencoder.md)

## <a name="class-identifier"></a>Identificador de clase

El identificador de clase (CLSID) del descodificador Windows Media Video 9 Screen se representa mediante la constante **\_ CLSID CMSSCDecMediaObject**. Puede crear una instancia del descodificador llamando a **CoCreateInstance**.

## <a name="input-types"></a>Tipos de entrada

El código de cuatro caracteres (FOURCC) para Windows contenido codificado de media video screen versión 9 es "MSS2".

El descodificador de pantalla de la versión 9 admite los siguientes tipos de entrada.

-   MEDIASUBTYPE \_ MSS2

## <a name="output-types"></a>Tipos de salida

Los siguientes tipos de salida son compatibles con el descodificador de pantalla de la versión 9 cuando se usa como objeto multimedia directX (DMO).

-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ ARGB32
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ RGB8

Los siguientes tipos de salida son compatibles con el descodificador de pantalla de la versión 9 cuando se usa como Media Foundation transform (MFT).

-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ ARGB32
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ RGB8

## <a name="remarks"></a>Observaciones

Un objeto descodificador de pantalla expone la interfaz [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) para que el objeto se pueda usar como objeto multimedia DirectX (DMO) y expone la interfaz [**DEFTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) para que el objeto se pueda usar como una transformación de Media Foundation (MFT).

Un descodificador de pantalla se comporta como un DMO o MFT en función de las interfaces que se obtengan y la versión de Windows se esté ejecutando. En la tabla siguiente se muestran las condiciones en las que un descodificador de pantalla se comporta DMO o MFT.



| Sistema operativo            | Comportamiento del descodificador                                                                                                                                                        |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows XP                  | Un Windows de Media Screen siempre se comporta como un DMO.                                                                                                                 |
| Windows Vista y Windows 7 | De forma predeterminada, un descodificador Windows Media Screen se comporta como un DMO. Si obtiene una interfaz [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) en un descodificador de pantalla, se comporta como un MFT. |



 

Puede usar el mismo CLSID (CLSID CMSSCDecMediaObject) para crear el descodificador de pantalla de la versión 7 y el descodificador de pantalla de \_ la versión 9. El contenido codificado fourcc Windows media video screen versión 7 es "MSS1". El descodificador de pantalla de la versión 7 admite el tipo de entrada MEDIASUBTYPE \_ MSS1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-----------------------------------------------------------------------------------------|
| Cliente<br/> | Windows XP, Windows Vista o Windows 7<br/>                                       |
| Header<br/> | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>Wmvsdecd.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Objetos de códec](codecobjects.md)
</dt> <dt>

[Implementación de códecs](codecimplementation.md)
</dt> <dt>

[Uso del códec de pantalla Windows Media Video 9](usingthewindowsmediavideo9screencodec.md)
</dt> <dt>

[Windows Codificador de pantalla de Vídeo multimedia 9](windowsmediavideo9screenencoder.md)
</dt> </dl>

 

 
