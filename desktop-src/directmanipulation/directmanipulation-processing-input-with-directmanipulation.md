---
description: En esta sección se proporciona información general sobre el modelo de subprocesos de manipulación directa, cómo se procesan los mensajes de ventana mediante la manipulación directa y cómo cambia el estado de una ventanilla a medida que la entrada se asigna a los movimientos de salida.
ms.assetid: 0818E34E-990E-4C36-9954-EF87EB226AF6
title: Procesamiento de entradas con DirectManipulation
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 49b72f88da8978192af402c8b810655c102395d5aad273f34340ed57e2703008
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094664"
---
# <a name="processing-input-with-directmanipulation"></a>Procesamiento de entradas con DirectManipulation

En esta sección se [](direct-manipulation-portal.md) proporciona información general sobre el modelo de subprocesos de manipulación directa, cómo se procesan los mensajes de ventana mediante la manipulación directa y cómo cambia el estado de una ventanilla a medida que la entrada se asigna a los movimientos de salida.

- [Flujo de entrada](#input-flow)
- [Comentarios:](#remarks)

[La manipulación](direct-manipulation-portal.md) directa usa dos subprocesos para coordinar las operaciones asincrónicas:

*Subproceso de interfaz* de usuario: el subproceso que posee el **HWND** asociado a la entrada. Este subproceso posee la inicialización de [la manipulación directa.](direct-manipulation-portal.md) El procesamiento de entrada del mouse y el teclado también se produce en el subproceso de la interfaz de usuario.

*Subproceso delegado:* el subproceso creado y propiedad de [la manipulación directa.](direct-manipulation-portal.md) El procesamiento de entrada táctil se produce en el subproceso de delegado.

## <a name="input-flow"></a>Flujo de entrada

En una configuración típica en la que las pruebas de acceso se realizan en el subproceso de la interfaz de usuario, la manipulación directa procesa los mensajes de ventana [en](direct-manipulation-portal.md) el orden siguiente:

![diagrama que muestra el orden en el que se procesan los mensajes.](images/inputprocessing.png)

Para una ventanilla en reposo:

1. Una serie de mensajes de ventana llegan al subproceso delegado.
2. [WM_POINTERDOWN](../inputmsg/wm-pointerdown.md) y [DM_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) los envía el subproceso delegado al subproceso de prueba de acceso independiente (IHT).
3. Si se llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) desde el subproceso IHT, el subproceso delegado podría enviar mensajes al subproceso de interfaz de usuario, en función del valor de [**DIRECTMANIPULATION \_ HITTEST \_ TYPE**](/windows/win32/api/directmanipulation/ne-directmanipulation-directmanipulation_hittest_type) cuando se llamó a [**RegisterHitTestTarget.**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)
4. Si no se llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) desde el subproceso IHT, el subproceso delegado siempre envía mensajes al subproceso de interfaz de usuario.
5. El cliente puede llamar a [**SetContact desde**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) el subproceso de la interfaz de usuario para permitir [que la manipulación directa](direct-manipulation-portal.md) detecte una manipulación.
6. Si se detecta una manipulación, [la](direct-manipulation-portal.md) manipulación directa envía un mensaje [wm/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) para notificar al cliente que la entrada se controla mediante la manipulación directa. El estado de la ventanilla se establece **en RUNNING y** la transformación de salida se actualizará.
7. Si se detecta una interacción que no sea una manipulación, [la manipulación directa](direct-manipulation-portal.md) envía los mensajes restantes al subproceso de interfaz de usuario.

Para una ventanilla en movimiento (con el estado RUNNING o INERTIA), el mensaje de la ventana llega primero al subproceso delegado, donde [la](direct-manipulation-portal.md) manipulación directa hace pruebas con todas las ventanillas en ejecución. La manipulación directa asigna automáticamente el contacto a las ventanillas adecuadas identificadas por las pruebas de acceso. El estado de la ventanilla es RUNNING y se actualizará la transformación de salida.

En algunos casos, un subproceso de interfaz de usuario de la aplicación puede ser demasiado lento para responder a las pruebas de acceso. Se puede usar un subproceso de prueba de acceso [**(RegisterHitTestTarget**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget)) para permitir que el cliente mueva mensajes [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) y [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md) a un subproceso específico para permitir las pruebas de acceso.

## <a name="remarks"></a>Comentarios

Normalmente, [la manipulación](direct-manipulation-portal.md) directa solo envía mensajes [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) [y DM/_POINTERHITTEST al](../inputmsg/dm-pointerhittest.md) subproceso de interfaz de usuario, reteniendo los mensajes posteriores mientras se espera una respuesta del cliente. Si el cliente llama a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact), los únicos mensajes que recibe el subproceso de interfaz de usuario cuando se detecta una manipulación son [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) y [DM/_POINTERHITTEST](../inputmsg/dm-pointerhittest.md)y el mensaje [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md).

Es posible que el cliente no llame [**a SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) al procesar [mensajes WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) [y DM/_POINTERHITTEST.](../inputmsg/dm-pointerhittest.md) En este caso, [la manipulación directa](direct-manipulation-portal.md) envía todos los mensajes al subproceso de la interfaz de usuario sin analizar los mensajes para ver si hay una manipulación. A continuación, el cliente puede elegir cualquier punto para llamar a **SetContact** y hacer que la manipulación directa empiece a detectar manipulaciones y envíe mensajes de mensaje [WM/_POINTERCAPTURECHANGED](../inputmsg/wm-pointercapturechanged.md) cuando se detecte uno.

**Windows 10 y versiones posteriores:** Puede decidir qué manipulaciones desea controlar llamando a [**DeferContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact) antes de llamar a [**SetContact**](/windows/win32/api/DirectManipulation/nf-directmanipulation-idirectmanipulationviewport-setcontact) en un mensaje [WM/_POINTERDOWN](../inputmsg/wm-pointerdown.md) [o DM/_POINTERHITTEST.](../inputmsg/dm-pointerhittest.md) **DeferContact** garantiza que todos los mensajes posteriores se envíen al subproceso de la interfaz de usuario durante el período de tiempo especificado.
