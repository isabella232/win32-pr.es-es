---
description: Conjunto de propiedades paso a paso de marco
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Conjunto de propiedades paso a paso de marco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ccddab4cd7f302dc850a4581ce8e70dcffc9cb6a4943c8f768a74c890edfb9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565005"
---
# <a name="frame-stepping-property-set"></a>Conjunto de propiedades paso a paso de marco

Los descodificadores que implementan búsquedas precisas de fotogramas en Microsoft DirectShow deben implementar el conjunto de propiedades FrameStep KSPROPSETID de AM, que se usa junto con la \_ \_ interfaz [**IVideoFrameStep.**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)



| Etiqueta | Valor |
|-------------------|----------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ FrameStep |



 



| Id. de propiedad                              | Descripción                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PASO \_ \_ FRAMESTEP DE LA \_ PROPIEDAD AM            | Indica al descodificador que inicie una operación de paso y pasa una estructura [**\_ \_ FRAMESTEP de AM PROPERTY**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) que especifica el número de pasos.            |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANCEL          | Indica al descodificador que cancele la operación de paso actual. No hay datos de instancia asociados a esta propiedad.                                                                  |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEP         | El descodificador devuelve S OK en esta instrucción para indicar que puede realizar la ejecución paso a \_ paso del marco; en caso contrario, S \_ FALSE. No se pasa ningún dato de instancia cuando se establece esta propiedad.         |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEPMULTIPLE | El descodificador devuelve S OK en esta instrucción para indicar que puede ir varios fotogramas a la vez; en caso \_ contrario, S \_ FALSE. No se pasa ningún dato de instancia cuando se establece esta propiedad. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 



