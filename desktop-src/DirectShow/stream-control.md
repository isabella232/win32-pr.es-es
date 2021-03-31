---
description: Control de flujo
ms.assetid: b529b38c-a25c-42dd-aee1-5d263c94202d
title: Control de flujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c41cee586737e131d4a32508b9ba6dd9ef1bd3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911093"
---
# <a name="stream-control"></a>Control de flujo

La interfaz [**IVMRVideoStreamControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrvideostreamcontrol) en los pin de entrada de la VMR permite a las aplicaciones y a los filtros ascendentes controlar el comportamiento del componente de mezclador, incluido el orden Z y el estado activo de los flujos de entrada de la VMR. Aunque esta interfaz se expone en las clavijas, funciona en el componente de mezclador de VMR, por lo que solo está disponible cuando se carga el mezclador, que es cuando la VMR procesa varios flujos de entrada. Los filtros ascendentes usan los métodos [**SetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setcolorkey) y [**GetColorKey**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getcolorkey) para controlar la clave del color de origen. Estos métodos permiten efectos como la superposición de la animación en vídeo. Solo tiene que establecer la clave de color en el color de fondo de la secuencia de animación y el VMR combinará ese flujo con otro flujo de vídeo. Las aplicaciones deben tener cuidado de no cambiar la clave de color a un valor distinto del valor utilizado por un filtro de nivel superior, como un descodificador.

Los filtros usan los métodos [**GetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-getstreamactivestate) y [**SetStreamActiveState**](/windows/desktop/api/Strmif/nf-strmif-ivmrvideostreamcontrol-setstreamactivestate) para indicar al mezclador si deben esperar datos de entrada de un PIN especificado. Por ejemplo, el descodificador de Line21 usa estos métodos para activar el PIN de entrada de VMR solo para los datos de Line21 cuando esos datos están presentes en la secuencia. Al establecer un PIN en un estado inactivo, se indica al mezclador que no espere por los datos de un PIN especificado antes de componer la imagen.

 

 



