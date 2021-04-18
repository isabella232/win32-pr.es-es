---
description: En esta sección se proporciona información general sobre el modelo de subprocesos de manipulación directa, cómo se procesan los mensajes de ventana mediante la manipulación directa y cómo cambia el estado de una ventanilla a medida que la entrada está asignada a los movimientos de salida.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Procesar la entrada con DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 284a0a1866a2082e2c34c65de347b0dcdfab3a64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105720258"
---
# <a name="processing-input-with-directmanipulation"></a>Procesar la entrada con DirectManipulation

En esta sección se proporciona información general sobre el modelo de subprocesos de [manipulación directa](direct-manipulation-portal.md) , cómo se procesan los mensajes de ventana mediante la manipulación directa y cómo cambia el estado de una ventanilla a medida que la entrada está asignada a los movimientos de salida.

- [Flujo de entrada](#input-flow)
- [Comentarios:](#remarks)

La [manipulación directa](direct-manipulation-portal.md) usa dos subprocesos para coordinar las operaciones asincrónicas:

*Subproceso de interfaz de usuario* : el subproceso que posee el **hWnd** asociado a la entrada. Este subproceso es propietario de la inicialización de la [manipulación directa](direct-manipulation-portal.md). El procesamiento de entradas de mouse y teclado también se produce en el subproceso de la interfaz de usuario.

*Delegate Thread* : el subproceso creado y propiedad de la [manipulación directa](direct-manipulation-portal.md). El procesamiento de la entrada táctil se produce en el subproceso delegado.

## <a name="input-flow"></a>Flujo de entrada

En una configuración típica en la que se realiza la prueba de posicionamiento en el subproceso de la interfaz de usuario, la [manipulación directa](direct-manipulation-portal.md) procesa los mensajes de ventana en el orden siguiente:

![diagrama que muestra el orden en el que se procesan los mensajes.](images/inputprocessing.png)

Para una ventanilla en reposo:

1. Una serie de mensajes de ventana alcanza el subproceso delegado.
2. El subproceso delegado envía los mensajes de [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) y [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) al subproceso de prueba de posicionamiento independiente (IHT).
3. Si se llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) desde el subproceso IHT, el subproceso delegado podría enviar mensajes al subproceso de la interfaz de usuario, dependiendo del valor de [**DIRECTMANIPULATION \_ HITTEST \_ Type**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) cuando se llamó a [**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget) .
4. Si no se llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) desde el subproceso IHT, el subproceso delegado siempre envía los mensajes al subproceso de la interfaz de usuario.
5. El cliente puede llamar a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) desde el subproceso de interfaz de usuario para permitir que la [manipulación directa](direct-manipulation-portal.md) detecte una manipulación.
6. Si se detecta una manipulación, la [manipulación directa](direct-manipulation-portal.md) envía un mensaje de [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) para notificar al cliente que la entrada se administra mediante la manipulación directa. El estado de la ventanilla se establece en Running (en **ejecución** ) y se actualizará la transformación de salida.
7. Si se detecta una interacción distinta de una manipulación, la [manipulación directa](direct-manipulation-portal.md) envía los mensajes restantes al subproceso de la interfaz de usuario.

En el caso de una ventanilla en movimiento (con el estado de en ejecución o inercia), el mensaje de ventana llega primero al subproceso delegado, donde las pruebas de posicionamiento de [manipulación directa](direct-manipulation-portal.md) en todas las ventanillas en ejecución. La manipulación directa asigna automáticamente el contacto a las ventanillas adecuadas identificadas por la prueba de posicionamiento. El estado de la ventanilla se está ejecutando y se actualizará la transformación de salida.

En algunos casos, es posible que un subproceso de interfaz de usuario de la aplicación sea demasiado lento para responder a las pruebas de posicionamiento. Se puede usar un subproceso de prueba de posicionamiento ([**RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)) para permitir que el cliente mueva los mensajes de [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) y [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) a un subproceso específico para permitir la realización de pruebas de posicionamiento.

## <a name="remarks"></a>Observaciones

Normalmente, la [manipulación directa](direct-manipulation-portal.md) solo envía mensajes [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) y [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) al subproceso de la interfaz de usuario, retrasando los mensajes posteriores mientras se espera una respuesta del cliente. Si el cliente llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact), los únicos mensajes que recibe el subproceso de interfaz de usuario cuando se detecta una manipulación son [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) y [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md), y el [mensaje de WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md).

Es posible que el cliente no llame a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) al procesar los mensajes de [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) y [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . En este caso, la [manipulación directa](direct-manipulation-portal.md) envía todos los mensajes al subproceso de interfaz de usuario sin analizar los mensajes para ver si hay una manipulación. A continuación, el cliente puede elegir cualquier punto para llamar a **SetContact** y hacer que la manipulación directa empiece a detectar manipulaciones, y enviar mensajes de [WM/_POINTERCAPTURECHANGED mensaje](../inputmsg/wm-pointercapturechanged.md) cuando se detecte uno.

**Windows 10 y versiones posteriores:** Puede decidir qué manipulaciones desea controlar llamando a [**DeferContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) antes de llamar a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) en un mensaje de [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) o [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) . **DeferContact** garantiza que todos los mensajes subsiguientes se envíen al subproceso de interfaz de usuario durante el período de tiempo especificado.
