---
description: Conjunto de propiedades paso a paso de fotogramas
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Conjunto de propiedades paso a paso de fotogramas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061668"
---
# <a name="frame-stepping-property-set"></a>Conjunto de propiedades paso a paso de fotogramas

Los descodificadores que implementan búsquedas precisas de fotogramas en Microsoft DirectShow deben implementar el conjunto de propiedades FrameStep de AM KSPROPSETID, que se usa junto con la \_ \_ interfaz [**IVideoFrameStep.**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)



| Etiqueta | Value |
|-------------------|----------------------------|
| GUID del conjunto de propiedades | AM \_ KSPROPSETID \_ FrameStep |



 



| Id. de propiedad                              | Descripción                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PASO DE \_ \_ FRAMESTEP DE LA \_ PROPIEDAD AM            | Indica al descodificador que inicie una operación de paso y pasa una estructura [**\_ \_ FRAMESTEP de AM PROPERTY**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) que especifica el número de pasos.            |
| CANCELACIÓN \_ DE \_ FRAMESTEP DE LA PROPIEDAD \_ AM          | Indica al descodificador que cancele la operación de paso actual. No hay datos de instancia asociados a esta propiedad.                                                                  |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEP         | El descodificador devuelve S OK en esta instrucción para indicar que puede ejecutar la ejecución paso a paso del marco; en caso \_ contrario, S \_ FALSE. Cuando se establece esta propiedad, no se pasan datos de instancia.         |
| AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEPMULTIPLE | El descodificador devuelve S OK en esta instrucción para indicar que puede ir varios \_ fotogramas a la vez; en caso contrario, S \_ FALSE. Cuando se establece esta propiedad, no se pasan datos de instancia. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conjuntos de propiedades](property-sets.md)
</dt> </dl>

 

 



