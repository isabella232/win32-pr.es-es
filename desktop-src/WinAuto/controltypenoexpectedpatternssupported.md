---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12d7c6500652c10d9ca3228237d215d1428358d2eff10cc6ea935e6974850001
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830095"
---
# <a name="controltypenoexpectedpatternssupported"></a>ControlTypeNoExpectedPatternsSupported

## <a name="text"></a>Texto

El elemento con controlType de debe admitir al menos uno {0} de estos patrones: {1} pero este elemento no

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

La compatibilidad con Automatización de la interfaz de usuario del elemento no cumple con la especificación Automatización de la interfaz de usuario porque el elemento debe admitir al menos uno de los patrones de control proporcionados, pero no lo hace. Como resultado, es posible que este elemento no se exponga correctamente a las tecnologías de asistencia, lo que podría afectar gravemente a la experiencia del usuario.

## <a name="possible-causes"></a>Causas posibles

-   Implementación Automatización de la interfaz de usuario incompleta.
-   La propiedad ControlType no está establecida correctamente.

## <a name="remarks"></a>Comentarios

AccChecker registra este mensaje de error para una barra de progreso indeterminada. Puede omitir este mensaje o agregarlo a la lista de supresiones.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**ControlTypePropertyId de UIA \_**](uiauto-automation-element-propids.md)
</dt> <dt>

[Información general sobre tipos de control de UI Automation](uiauto-controltypesoverview.md)
</dt> <dt>

[Información general acerca de los patrones de control de UI Automation](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




