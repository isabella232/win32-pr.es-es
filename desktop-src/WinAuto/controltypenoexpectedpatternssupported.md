---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357163"
---
# <a name="controltypenoexpectedpatternssupported"></a>ControlTypeNoExpectedPatternsSupported

## <a name="text"></a>Texto

El elemento con un ControlType de {0} debe admitir al menos uno de estos patrones: {1} pero este elemento no

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

La compatibilidad de automatización de la interfaz de usuario del elemento no cumple con la especificación de automatización de la interfaz de usuario porque el elemento debe admitir al menos una de las listas de patrones de control proporcionadas, pero no. Como resultado, es posible que este elemento no esté expuesto correctamente a las tecnologías de asistencia, lo que podría tener un impacto serio en la experiencia del usuario.

## <a name="possible-causes"></a>Causas posibles

-   Implementación de automatización de la interfaz de usuario incompleta.
-   La propiedad ControlType no se ha establecido correctamente.

## <a name="remarks"></a>Observaciones

AccChecker registra este mensaje de error para una barra de progreso indeterminada. Puede omitir este mensaje o agregarlo a la lista de supresiones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




