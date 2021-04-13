---
title: Nuevas características de TSF
description: Con el lanzamiento de Microsoft WindowsXP Service Pack1, el marco de trabajo de servicios de texto (TSF) tiene varias características nuevas.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Text Services Framework (TSF), nuevas características
- TSF (marco de trabajo de servicios de texto), nuevas características
- servicios de texto, nuevas características
- Aplicaciones habilitadas para TSF, nuevas características
- Text Services Framework (TSF), soporte técnico avanzado
- TSF (marco de trabajo de servicios de texto), soporte técnico avanzado
- servicios de texto, soporte técnico avanzado
- Aplicaciones habilitadas para TSF, compatibilidad avanzada
- Marco de trabajo de servicios de texto (TSF), edición enriquecida
- TSF (marco de trabajo de servicios de texto), edición enriquecida
- servicios de texto, edición enriquecida
- Aplicaciones habilitadas para TSF, edición enriquecida
- Edición enriquecida
- Marco de trabajo de servicios de texto (TSF), seguridad
- TSF (marco de trabajo de servicios de texto), seguridad
- servicios de texto, seguridad
- Aplicaciones habilitadas para TSF, seguridad
- seguridad para TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420806"
---
# <a name="new-features-in-tsf"></a>Nuevas características de TSF

Con el lanzamiento de Microsoft WindowsXP Service Pack1, el marco de trabajo de servicios de texto (TSF) tiene varias características nuevas.

## <a name="extended-support-of-advanced-text-services"></a>Compatibilidad ampliada con servicios de texto avanzados

Se ha agregado compatibilidad con TSF y Windows para proporcionar una interfaz de usuario coherente para todas las aplicaciones en el escritorio. Esta nueva compatibilidad permite a las aplicaciones heredadas o a los controles que no saben que TSF aproveche algunos servicios de texto avanzados de forma gratuita. Por ejemplo, el dictado de voz y la escritura a mano ahora se pueden usar para escribir texto en un documento de cualquier aplicación.

Esta nueva característica solo está disponible para WindowsXP Service Pack1 o posterior. Está desactivada de forma predeterminada. Para habilitarlo, haga clic en la casilla de la ficha Opciones **avanzadas** de la sección **servicios de texto e idiomas de entrada** del panel de control **configuración regional y de idioma** .

![compatibilidad con aplicaciones deshabilitadas en el panel de control de TSF](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>Compatibilidad con la edición enriquecida

[Edición enriquecida de Microsoft®](../controls/rich-edit-controls.md) La versión 4,1, usada por las aplicaciones para ver y editar texto con formato de caracteres y párrafos especiales, ahora expone la funcionalidad TSF. De forma predeterminada, esta compatibilidad está desactivada. Para habilitar TSF en Rich Edit, una aplicación de hospedaje envía un mensaje de ventana especial al control Rich Edit.

## <a name="security-improvements"></a>Mejoras de seguridad

La seguridad y la solidez de TSF se han mejorado sustancialmente, para reducir la probabilidad de que un programa hostil pueda acceder a la pila, al montón o a otras ubicaciones de memoria seguras. También se ha mejorado la seguridad de las aplicaciones de ejemplo y los servicios de texto del kit de desarrollo de software (SDK).

 

 