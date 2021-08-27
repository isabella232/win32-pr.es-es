---
title: Funciones de contexto de interacción
description: Los temas de esta sección proporcionan las especificaciones de referencia para las funciones de contexto de interacción.
ms.assetid: 0F34F181-D92C-4B08-9F1D-62379D4A2B15
keywords:
- interacción con el usuario
- input
- puntero
- Función táctil
- mouse
- Lápiz
- lápiz
ms.topic: article
ms.date: 02/06/2020
ms.openlocfilehash: 5f0769aa5b9b097b23206c0515bd32552a59969404e72bbfcf26973d5d4f3de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118758341"
---
# <a name="interaction-context-functions"></a>Funciones de contexto de interacción

Los temas de esta sección proporcionan las especificaciones de referencia para las [funciones de contexto de](interaction-context-portal.md) interacción.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|---|---|
| [**AddPointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | Incluya el puntero especificado en el conjunto de punteros procesados por el objeto [Contexto de](interaction-context-portal.md) interacción. <br/> |
| [**BufferPointerPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | Agrega el historial de un solo puntero de entrada al búfer del objeto [Contexto de](interaction-context-portal.md) interacción.<br/> |
| [**CreateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | Crea e inicializa un objeto [de contexto de](interaction-context-portal.md) interacción.<br/> |
| [**DestroyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | Destruye el objeto de [contexto de interacción](interaction-context-portal.md) especificado.<br/> |
| [**GetCrossSlideParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | Obtiene el comportamiento de interacción entre diapositivas. <br/> |
| [**GetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | Obtiene el comportamiento de inercia de una manipulación (traducción, rotación, escalado). <br/> |
| [**GetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | Obtiene el estado de configuración de interacción para el [objeto Contexto de](interaction-context-portal.md) interacción.<br/> |
| [**GetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | Obtiene el estado de la rueda del mouse para el [objeto Contexto de](interaction-context-portal.md) interacción. <br/> |
| [**GetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | Obtiene las [propiedades del objeto de contexto](interaction-context-portal.md) de interacción.<br/> |
| [**GetStateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | Obtiene el estado [actual del contexto de](interaction-context-portal.md) interacción y la hora en que el contexto volverá al estado inactivo. <br/> |
| [**ProcessBufferedPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | Procesar paquetes almacenados en búfer al final de un marco de entrada de puntero.<br/> |
| [**ProcessInertiaInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | Envía la entrada del temporizador al [objeto Contexto de](interaction-context-portal.md) interacción para el procesamiento de la inercia.<br/> |
| [**ProcessPointerFramesInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | Procesa un conjunto de marcos de entrada de puntero.<br/> |
| [**RegisterOutputCallbackInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | Registra una devolución de llamada para recibir eventos de interacción de un [objeto de contexto de](interaction-context-portal.md) interacción.<br/> |
| [**RemovePointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | Quite el puntero especificado del conjunto de punteros procesados por el objeto [Contexto de](interaction-context-portal.md) interacción. <br/> |
| [**ResetInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | Restablece el estado [**de interacción,**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state)las opciones de configuración de interacción y todos los parámetros a su estado inicial. Las interacciones actuales se cancelan sin notificaciones. <br/> [El contexto de](interaction-context-portal.md) interacción debe volver a configurarse antes del siguiente uso.<br/> |
| [**SetCrossSlideParametersInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | Configura la interacción entre diapositivas. <br/> |
| [**SetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | Configura el comportamiento de inercia de una manipulación (traducción, rotación, escalado) después de que se eleva el contacto. <br/> | [**SetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | Configura el objeto [Contexto de](interaction-context-portal.md) interacción para procesar las manipulaciones especificadas.<br/> |
| [**SetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | Establece los valores de parámetro para la entrada de rueda del mouse. <br/> |
| [**SetPivotInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | Establece el punto central y el radio de pivote desde el punto central para una manipulación de rotación mediante un solo puntero de entrada. <br/> |
| [**SetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | Establece las [propiedades del objeto de contexto](interaction-context-portal.md) de interacción.<br/> |
| [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | Establece el estado [**de interacción en**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) ESTADO DE INTERACCIÓN INACTIVO y deja intactos todos los parámetros y valores de configuración de \_ \_ interacción. Las interacciones actuales se cancelan y las notificaciones se envían según sea necesario.<br/> [El contexto](interaction-context-portal.md) de interacción no tiene que volver a configurarse antes del siguiente uso.<br/> |

## <a name="related-topics"></a>Temas relacionados

[Referencia de contexto de interacción](interaction-context-reference.md)
