---
description: Trabajar con destinos de representación de Direct3D
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: Trabajar con destinos de representación de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f7bacf36402b071d60989e225cdcd9533500494a0593bcf9753ddc06bb93ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650345"
---
# <a name="working-with-direct3d-render-targets"></a>Trabajar con destinos de representación de Direct3D

Se definen varios subtipos de medios para destinos de representación de Direct3D para su uso con VMR-7 y VMR-9. Cuando un filtro ascendente propone una conexión con uno de estos subtipos, indica al VMR que la representación se va a realizar en un destino de representación de Direct3D. Para VMR-7, será un destino de representación directX 7 Direct3D y para VMR-9 será un destino de representación directX 9 Direct3D. Si vmr está en modo de combinación, la superficie también será una superficie de textura de Direct3D. Si el VMR no está en modo de combinación, la superficie será una superficie direct3D normal. Los formatos de píxel ARGB solo se admiten cuando vmr está en modo de combinación. Los subtipos de destino de representación son:



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT   | MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX9 \_ RT   |
| MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX9 \_ RT |
| MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX9 \_ RT |



 

Estos tipos se definen en el archivo de encabezado uuids.h. Los tipos de medios MEDIASUBTYPE RGB32 tienen un formato RGBx888 y los tipos de medios \_ MEDIASUBTYPE RGB16 tienen un \_ formato RGB565. Para obtener más información sobre estos formatos de píxel, consulte la documentación de gráficos de DirectX.

**Solicitud de una superficie desbloqueada**

Bloquear y desbloquear superficies de DirectDraw son operaciones costosas desde el punto de vista computacional. Al usar los subtipos multimedia de destino de representación de Direct3D, el filtro ascendente necesita que se desbloqueen las superficies para que pueda operar en ellas con el hardware gráfico. Para evitar una operación de desbloqueo de bloqueo innecesaria, el VMR admite una nueva marca en el método [**IMemAllocator::GetBuffer,**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) AM \_ GBF NODDSURFACELOCK, que indica al VMR que no bloquee la superficie de DirectDraw antes de pasar una muestra al filtro \_ ascendente. Cuando se usa esta marca, se producirá un error en las llamadas a [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) porque no hay ningún puntero bloqueado. Para obtener acceso a la superficie de DirectDraw, el filtro debe llamar a **QueryInterface** en el objeto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) devuelto y solicitar la [**interfaz IVMRSurface.**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) Obviamente, el filtro ascendente debe asegurarse de que la superficie no está bloqueada cuando vuelve a liberar el ejemplo en la lista libre.

 

 



