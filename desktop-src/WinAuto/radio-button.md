---
title: Botón de radio (referencia de elementos de interfaz de usuario de MSAA)
description: Los botones de radio se utilizan para seleccionar una de varias opciones, normalmente en un cuadro de diálogo.
ms.assetid: cf4568ff-1bc4-4770-bc54-a5d08ac0a60c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9766e85f530281e4f843c4d39fd41fe35d4fb620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774167"
---
# <a name="radio-button-msaa-ui-element-reference"></a>Botón de radio (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **botón de radio** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **botón de radio** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Los botones de radio se utilizan para seleccionar una de varias opciones, normalmente en un cuadro de diálogo. Un botón de radio contiene un círculo pequeño con texto al lado. Cuando se selecciona, el círculo tiene un círculo más pequeño y relleno dentro de él. Al seleccionar un botón en un conjunto, se anula la selección del botón seleccionado previamente, por lo que solo se selecciona una de las opciones del conjunto cada vez.

El nombre de clase de ventana para un botón de radio es "BUTTON".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un botón de radio admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentarios                                                                                                      |
|---------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | El método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) hace clic en el botón de radio. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                               |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                               |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                               |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                               |



 

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un botón de radio admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                             | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | La propiedad **ChildCount** es cero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)       | La propiedad **DEFAULTACTION** para un botón de radio es "check".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | La propiedad **KeyboardShortcut** es la tecla de acceso del botón de radio, que es un carácter subrayado en el texto de la ventana del control. Esta cadena contiene el carácter de tecla de acceso anexado a la cadena "Alt +".                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | La propiedad **Name** se obtiene del texto (o título) de la ventana del control, que se muestra con el botón de radio.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | La propiedad **role** es [**\_ \_ RADIOBUTTON del sistema de funciones**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_**](object-state-constants.md) \| [**\_ \_ activo**](object-state-constants.md) sistema estado activado sistema estado \| [**\_ \_ activado**](object-state-constants.md) \| [**\_ \_ normal**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[**Casilla de verificación**](check-box.md)
</dt> <dt>

[**Cuadro de grupo**](group-box.md)
</dt> <dt>

[**Botón de reenvío**](push-button.md)
</dt> </dl>

 

 





