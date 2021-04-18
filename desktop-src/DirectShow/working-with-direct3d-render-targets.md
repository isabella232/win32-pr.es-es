---
description: Trabajar con destinos de representación de Direct3D
ms.assetid: 271b919c-421b-4484-8e60-afbf3cbdca44
title: Trabajar con destinos de representación de Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8aca19082c5db9521cfc1c7341fd74c98270cbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666763"
---
# <a name="working-with-direct3d-render-targets"></a>Trabajar con destinos de representación de Direct3D

Se definen varios subtipos de medios para los destinos de representación de Direct3D para su uso con VMR-7 y VMR-9. Cuando un filtro de nivel superior propone una conexión con uno de estos subtipos, indica al VMR que la representación se va a realizar en un destino de representación de Direct3D. En el caso de VMR-7, será un destino de representación de Direct3D 7 Direct3D y para VMR-9, que será un destino de representación de Direct3D 9 Direct3D. Si el VMR está en modo de mezcla, la superficie también será una superficie de textura de Direct3D. Si VMR no está en modo de mezcla, la superficie será una superficie de Direct3D normal. Los formatos de píxel ARGB solo se admiten cuando el VMR está en modo de mezcla. Los subtipos de destino de representación son:



| VMR-7                                | VMR-9                                |
|--------------------------------------|--------------------------------------|
| MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB32 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX7 \_ RT    | MEDIASUBTYPE \_ RGB16 \_ D3D \_ DX9 \_ RT    |
| MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX7 \_ RT   | MEDIASUBTYPE \_ ARGB32 \_ D3D \_ DX9 \_ RT   |
| MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB4444 \_ D3D \_ DX9 \_ RT |
| MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX7 \_ RT | MEDIASUBTYPE \_ ARGB1555 \_ D3D \_ DX9 \_ RT |



 

Estos tipos se definen en el archivo de encabezado UUID. h. Los tipos de medios de RGB32 de MEDIASUBTYPE \_ son un formato RGBx888 y los \_ tipos de medios MEDIASUBTYPE RGB16 son un formato RGB565. Para obtener más información sobre estos formatos de píxeles, consulte la documentación sobre gráficos de DirectX.

**Solicitud de una superficie desbloqueada**

El bloqueo y el desbloqueo de las superficies de DirectDraw son operaciones costosamente costosas. Al usar los subtipos de medios de destino de representación de Direct3D, el filtro de nivel superior necesita que las superficies se desbloqueen para que pueda trabajar en ellas con el hardware de gráficos. Para evitar una operación innecesaria de desbloqueo de bloqueo, VMR admite una nueva marca en el método [**IMemAllocator:: getBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , AM \_ GBF \_ NODDSURFACELOCK, que indica a la VMR que no bloquee la superficie DirectDraw antes de pasar una muestra al filtro de nivel superior. Cuando se usa esta marca, se producirá un error en las llamadas a [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) porque no hay ningún puntero bloqueado. Para obtener acceso a la superficie de DirectDraw, el filtro debe llamar a **QueryInterface** en el objeto [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) devuelto y solicitar la interfaz [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) . Obviamente, el filtro de nivel superior debe asegurarse de que la superficie no esté bloqueada cuando vuelva a liberar el ejemplo en la lista de disponibilidad.

 

 



