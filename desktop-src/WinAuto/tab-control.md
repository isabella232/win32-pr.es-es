---
title: Control de pestaña (referencia de elementos de interfaz de usuario de MSAA)
description: Un control de ficha define varias páginas para la misma área de una ventana o un cuadro de diálogo.
ms.assetid: 664dd109-3c4a-4106-9b92-e10ec5a33463
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cc8381a668701446e06df81694941ece9f5f259
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714152"
---
# <a name="tab-control-msaa-ui-element-reference"></a>Control de pestaña (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **control de pestaña** para la referencia de elementos de interfaz de usuario de MSAA. Cómo crear objetos de **control de pestaña** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un control de ficha define varias páginas para la misma área de una ventana o un cuadro de diálogo. Cada página está formada por un conjunto de información o un grupo de controles que una aplicación muestra cuando el usuario selecciona la pestaña correspondiente. El sistema operativo Windows usa controles de ficha para mostrar los botones de la barra de tareas, con la excepción del botón **iniciar** .

El nombre de clase de ventana de un control de ficha es WC \_ TABCONTROL, que se define como "SysTabControl" en commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un control de pestaña admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentarios                                                                                                  |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | El método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) hace clic en la pestaña de la página. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                           |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                           |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                           |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                           |



 

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un control de pestaña admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La propiedad **DEFAULTACTION** es "switch".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propiedad **KeyboardShortcut** es la tecla de acceso del control de pestaña, que es un carácter subrayado en el texto de la ventana del control. Esta cadena contiene el carácter de tecla de acceso anexado a la cadena "Alt +".                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** se obtiene del texto (o título) de la ventana del control, que se muestra en el control de pestaña.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propiedad **primaria** es una ventana ( [**sistema \_ de \_ PAGETABLIST de rol**](object-roles.md) ) que rodea el control y tiene el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**\_ \_ PAGETAB del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**obtener \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad de **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): sistema de estado [**\_ \_ invisible**](object-state-constants.md) sistema de estado seleccionado sistema de estado \| [**\_ \_ selección**](object-state-constants.md) del sistema de estado de sistema \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ activo**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) de estado activado<br/> |



 

## <a name="notes"></a>Notas

Los controles de ficha devuelven correctamente los elementos correctos \_ desde el método [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect) cuando se llama con la marca [**\_ TAKEFOCUS de SELFLAG**](selflag.md) . Los controles de ficha no pueden tomar el foco del teclado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





