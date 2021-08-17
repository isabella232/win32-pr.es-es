---
title: Nuevas características de TSF
description: Con el lanzamiento de Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) tiene varias características nuevas.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Text Services Framework (TSF),nuevas características
- TSF (Text Services Framework),nuevas características
- servicios de texto, nuevas características
- Aplicaciones habilitadas para TSF, nuevas características
- Text Services Framework (TSF), soporte técnico avanzado
- TSF (Text Services Framework), compatibilidad avanzada
- servicios de texto, soporte técnico avanzado
- Aplicaciones habilitadas para TSF, compatibilidad avanzada
- Text Services Framework (TSF),Edición enriquecida
- TSF (Text Services Framework),Edición enriquecida
- text services,Rich Edit
- Aplicaciones habilitadas para TSF, edición enriquecida
- Edición enriquección
- Text Services Framework (TSF),seguridad
- TSF (Text Services Framework),seguridad
- servicios de texto, seguridad
- Aplicaciones habilitadas para TSF, seguridad
- seguridad de TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be73494d4538b25dfa0b004c8691391fb1c572c7ce6d82247cacae4fb9e0a838
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117952031"
---
# <a name="new-features-in-tsf"></a>Nuevas características de TSF

Con el lanzamiento de Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) tiene varias características nuevas.

## <a name="extended-support-of-advanced-text-services"></a>Compatibilidad ampliada con Advanced Text Services

Se ha agregado compatibilidad con TSF y Windows para proporcionar una interfaz de usuario coherente para todas las aplicaciones del escritorio. Esta nueva compatibilidad permite que las aplicaciones o controles heredados que no son conscientes de TSF aprovechen algunos servicios de texto avanzados de forma gratuita. Por ejemplo, ahora se puede usar el dictado de voz y la escritura a mano para escribir texto en un documento en cualquier aplicación.

Esta nueva característica solo está disponible para WindowsXP Service Pack1 o posterior. Está desactivada de forma predeterminada. Para habilitarlo, haga clic en  la casilla de la nueva pestaña Opciones avanzadas en la parte Servicios de texto e **Idiomas** de entrada del panel de control **Opciones regionales** e idiomas.

![compatibilidad con aplicaciones no conscientes en el panel de control de tsf](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a>Compatibilidad con edición enriquecte

[Edición ® de Microsoft](../controls/rich-edit-controls.md) La versión 4.1, usada por las aplicaciones para ver y editar texto con formato de párrafo y carácter especial, ahora expone la funcionalidad de TSF. De forma predeterminada, esta compatibilidad está desactivada. Para habilitar TSF en Rich Edit, una aplicación de hospedaje envía un mensaje de ventana especial al control Rich Edit.

## <a name="security-improvements"></a>Mejoras de seguridad

La seguridad y solidez de TSF se han mejorado considerablemente para reducir la probabilidad de que un programa remoto pueda acceder a la pila, el montón u otras ubicaciones de memoria seguras. También se ha mejorado la seguridad de las aplicaciones de ejemplo y los servicios de texto del Kit de desarrollo de software (SDK).

 

 