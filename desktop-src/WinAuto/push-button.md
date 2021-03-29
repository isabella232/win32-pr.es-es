---
title: Botón de reenvío (referencia de elementos de interfaz de usuario de MSAA)
description: Un botón de reenvío es un pequeño objeto rectangular que se utiliza para realizar una acción. Por ejemplo, los botones aceptar y cancelar de un cuadro de diálogo son botones de reenvío.
ms.assetid: 26dbe4a0-4110-4569-bac6-fa0a95c785dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e188b58501509fd934ab6396a21beb209857661
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775492"
---
# <a name="push-button-msaa-ui-element-reference"></a>Botón de reenvío (referencia de elementos de interfaz de usuario de MSAA)

Un botón de reenvío es un pequeño objeto rectangular que se utiliza para realizar una acción. Por ejemplo, los botones **Aceptar** y **Cancelar** de un cuadro de diálogo son botones de reenvío.

El nombre de la clase de ventana para un botón de la tecla de reenvío es "BUTTON".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un botón de método de extracción admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentarios                                                                                                     |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | El método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) hace clic en el botón de presionar. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                              |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                              |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                              |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                              |



 

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un botón de reenvío admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propiedad **ChildCount** es cero o más.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La propiedad **DEFAULTACTION** es "Press".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propiedad **KeyboardShortcut** es la tecla de acceso del botón, que es un carácter subrayado en el texto del texto de la ventana del botón. Por ejemplo, "Alt + o" es la propiedad **KeyboardShortcut** de un botón **Aceptar** .                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** se obtiene del texto (o título) de la ventana del control, que se muestra en el botón de la tecla de control. Por ejemplo, "Aceptar" es la propiedad de **nombre** de un botón **Aceptar** .                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**\_ \_ PUSHBUTTON del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**estado \_ \_ invisible**](object-state-constants.md) del sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) del sistema de estado sistema de estado del sistema de estado \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ presionado**](object-state-constants.md) sistema \| [**\_ \_ predeterminado**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Casilla de verificación**](check-box.md)
</dt> <dt>

[**Cuadro de grupo**](group-box.md)
</dt> <dt>

[**Botón de radio**](radio-button.md)
</dt> </dl>

 

 





