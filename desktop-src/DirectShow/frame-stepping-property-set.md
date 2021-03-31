---
description: Conjunto de propiedades de ejecución de fotogramas
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Conjunto de propiedades de ejecución de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806128"
---
# <a name="frame-stepping-property-set"></a>Conjunto de propiedades de ejecución de fotogramas

Los descodificadores que implementan búsquedas con precisión de fotogramas en Microsoft DirectShow deben implementar el \_ conjunto de propiedades AM KSPROPSETID \_ FrameStep, que se usa junto con la interfaz [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) .



|                   |                            |
|-------------------|----------------------------|
| GUID del conjunto de propiedades | \_FrameStep KSPROPSETID \_ AM |



 



| Id. de propiedad                              | Descripción                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FRAMESTEP de la \_ propiedad AM \_ \_ paso            | Indica al descodificador que comience una operación de paso y pasa una [**estructura \_ \_ FRAMESTEP de la propiedad AM**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) que especifica el número de pasos.            |
| \_propiedad AM \_ FRAMESTEP \_ cancelar          | Indica al descodificador que cancele la operación de paso actual. No hay datos de instancia asociados a esta propiedad.                                                                  |
| \_propiedad AM \_ FRAMESTEP \_ CANSTEP         | El descodificador devuelve S \_ OK en esta instrucción para indicar que puede realizar la ejecución paso a paso de fotogramas; de \_ lo contrario, es false. No se pasan datos de instancia cuando se establece esta propiedad.         |
| \_propiedad AM \_ FRAMESTEP \_ CANSTEPMULTIPLE | El descodificador devuelve S \_ OK en esta instrucción para indicar que puede recorrer varios fotogramas a la vez; de \_ lo contrario, es false. No se pasan datos de instancia cuando se establece esta propiedad. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 



