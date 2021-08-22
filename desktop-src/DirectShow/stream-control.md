---
description: Stream Control
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Stream Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8da9f317137904a87356bbdcc10dc68357513cf168a0b7b7ea46398ed47a81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072389"
---
# <a name="stream-control"></a>Stream Control

La [**interfaz IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) en los pin de entrada de VMR permite que las aplicaciones y los filtros ascendentes controle el comportamiento del componente mezclador, incluido el orden Z y el estado activo de los flujos de entrada del VMR. Aunque esta interfaz se expone en los pines, funciona en el componente mezclador de VMR, por lo que solo está disponible cuando se carga el mezclador, que es cuando la VMR procesa varios flujos de entrada. Los filtros ascendentes usan [**los métodos SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) y [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) para controlar la clave de color de origen. Estos métodos permiten efectos como la superposición de animación sobre vídeo. Basta con establecer la clave de color en el color de fondo de la secuencia de animación y vmr mezclará esa secuencia con otra secuencia de vídeo. Las aplicaciones deben tener cuidado de no cambiar la clave de color por un valor diferente del que usa un filtro ascendente, como un descodificador.

Los filtros usan [**los métodos GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) y [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) para decir al mezclador si se deben esperar datos de entrada de un pin especificado. Por ejemplo, el descodificador Line21 usa estos métodos para activar el pin de entrada del VMR para los datos line21 solo cuando esos datos están presentes en la secuencia. Al establecer un pin en un estado inactivo, se indica al mezclador que no espere los datos de un pin especificado antes de componer la imagen.

 

 



