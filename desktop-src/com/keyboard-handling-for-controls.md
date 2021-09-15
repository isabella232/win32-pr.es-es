---
title: Control de teclado para controles
description: Un control responde a los aceleradores de teclado para que el usuario final pueda iniciar acciones realizadas por el control.
ms.assetid: 59aca5cb-f109-49ee-897d-43610501f7f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbe03058fdb0192a0f8f7b13032612288045775b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359838"
---
# <a name="keyboard-handling-for-controls"></a>Control de teclado para controles

Un control responde a los aceleradores de teclado para que el usuario final pueda iniciar acciones realizadas por el control. El contenedor administra la actividad de teclado para todos sus controles incrustados. Con los documentos compuestos, los aceleradores de teclado solo se aplican al objeto activo actualmente. Con los controles, se ha agregado un mecanismo para que un control pueda responder a su tecla mnemotécnica aunque no esté activo actualmente en la interfaz de usuario.

Los [**métodos IOleControl::GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo) e [**IOleControl::OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic) y el método [**IOleControlSite::OnControlInfoChanged**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-oncontrolinfochanged) controlan los métodos de teclado de un control. Una [**estructura CONTROLINFO**](/windows/win32/api/ocidl/ns-ocidl-controlinfo) describe los aceleradores mnemotécnicos de un control y las marcas que se le pasan a través del método **GetControlInfo** describen el comportamiento de los controles con las teclas Enter y Esc. Cuando un control cambia sus elementos mnemotécnicos, llama a **OnControlInfoChanged** para que el contenedor pueda volver a cargar la estructura si es necesario.

Cuando un control está activo en la interfaz de usuario, también es el control con el foco. A medida que los controles se activan y desactivan entre el activo en contexto y los estados activos de la interfaz de usuario, el control llama a [**IOleControlSite::OnFocus**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-onfocus) para que informe al contenedor de estos cambios.

Además, cuando un control está activo en la interfaz de usuario, tendrá la primera oportunidad de procesar las pulsaciones de tecla. Para dar a un contenedor la oportunidad de procesar la pulsación de tecla antes del control, el control llama a [**IOleControlSite::TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator). Si el contenedor no controla la pulsación de tecla, el control lo procesa.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Controles ActiveX](activex-controls.md)
</dt> </dl>

 

 




