---
title: Funciones de contexto de interacción
description: En los temas de esta sección se proporcionan las especificaciones de referencia para las funciones de contexto de interacción.
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
ms.openlocfilehash: 7f57bf6ac2b5d9bc7f17a43cd84a6e8eb7d828a4
ms.sourcegitcommit: 6b8d5058d02daacad4d2ed7830da63b63a509586
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/07/2020
ms.locfileid: "105720119"
---
# <a name="interaction-context-functions"></a>Funciones de contexto de interacción

En los temas de esta sección se proporcionan las especificaciones de referencia para las funciones de [contexto de interacción](interaction-context-portal.md) .

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|---|---|
| [**AddPointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext)<br/> | Incluye el puntero especificado en el conjunto de punteros procesados por el objeto de [contexto de interacción](interaction-context-portal.md) . <br/> |
| [**BufferPointerPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-bufferpointerpacketsinteractioncontext)<br/> | Agrega el historial de un puntero de entrada único al búfer del objeto de [contexto de interacción](interaction-context-portal.md) .<br/> |
| [**CreateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-createinteractioncontext)<br/> | Crea e inicializa un objeto de [contexto de interacción](interaction-context-portal.md) .<br/> |
| [**DestroyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext)<br/> | Destruye el objeto de [contexto de interacción](interaction-context-portal.md) especificado.<br/> |
| [**GetCrossSlideParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getcrossslideparameterinteractioncontext)<br/> | Obtiene el comportamiento de interacción entre diapositivas. <br/> |
| [**GetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinertiaparameterinteractioncontext)<br/> | Obtiene el comportamiento de inercia de una manipulación (traslación, giro, escala). <br/> |
| [**GetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext)<br/> | Obtiene el estado de configuración de interacción para el objeto de [contexto de interacción](interaction-context-portal.md) .<br/> |
| [**GetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext)<br/> | Obtiene el estado de la rueda del mouse para el objeto de [contexto de interacción](interaction-context-portal.md) . <br/> |
| [**GetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext)<br/> | Obtiene las propiedades del objeto de [contexto de interacción](interaction-context-portal.md) .<br/> |
| [**GetStateInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext)<br/> | Obtiene el estado del [contexto de interacción](interaction-context-portal.md) actual y la hora en que el contexto volverá al estado de inactividad. <br/> |
| [**ProcessBufferedPacketsInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processbufferedpacketsinteractioncontext)<br/> | Procesar los paquetes almacenados en búfer al final de un marco de entrada de puntero.<br/> |
| [**ProcessInertiaInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processinertiainteractioncontext)<br/> | Envía la entrada del temporizador al objeto de [contexto de interacción](interaction-context-portal.md) para el procesamiento de la inercia.<br/> |
| [**ProcessPointerFramesInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-processpointerframesinteractioncontext)<br/> | Procesa un conjunto de marcos de entrada de puntero.<br/> |
| [**RegisterOutputCallbackInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext)<br/> | Registra una devolución de llamada para recibir los eventos de interacción de un objeto de [contexto de interacción](interaction-context-portal.md) .<br/> |
| [**RemovePointerInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext)<br/> | Quitar el puntero especificado del conjunto de punteros procesados por el objeto de [contexto de interacción](interaction-context-portal.md) . <br/> |
| [**ResetInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-resetinteractioncontext)<br/> | Restablece el estado de [**interacción**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state), los valores de configuración de interacción y todos los parámetros a su estado inicial. Las interacciones actuales se cancelan sin notificaciones. <br/> El [contexto de interacción](interaction-context-portal.md) debe volver a configurarse antes del siguiente uso.<br/> |
| [**SetCrossSlideParametersInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setcrossslideparametersinteractioncontext)<br/> | Configura la interacción entre diapositivas. <br/> |
| [**SetInertiaParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext)<br/> | Configura el comportamiento de inercia de una manipulación (traslación, rotación y escalado) una vez que se levanta el contacto. <br/> | [**SetInteractionConfigurationInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext)<br/> | Configura el objeto de [contexto de interacción](interaction-context-portal.md) para procesar las manipulaciones especificadas.<br/> |
| [**SetMouseWheelParameterInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext)<br/> | Establece los valores de parámetro para la entrada de la rueda del mouse. <br/> |
| [**SetPivotInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpivotinteractioncontext)<br/> | Establece el punto central y el radio de pivote desde el punto central, para una manipulación de rotación mediante un puntero de entrada único. <br/> |
| [**SetPropertyInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext)<br/> | Establece las propiedades del objeto de [contexto de interacción](interaction-context-portal.md) .<br/> |
| [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)<br/> | Establece el [**Estado de interacción**](/windows/win32/api/interactioncontext/ne-interactioncontext-interaction_state) en \_ Estado de interacción \_ inactivo y deja intactos todos los parámetros y parámetros de configuración de interacción. Las interacciones actuales se cancelan y las notificaciones se envían según sea necesario.<br/> No es necesario volver a configurar el [contexto de interacción](interaction-context-portal.md) antes del siguiente uso.<br/> |

## <a name="related-topics"></a>Temas relacionados

[Referencia de contexto de interacción](interaction-context-reference.md)
