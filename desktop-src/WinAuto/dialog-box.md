---
title: Cuadro de diálogo (referencia de elementos de interfaz de usuario de MSAA)
description: Un cuadro de diálogo es una ventana temporal que crea una aplicación para recuperar los datos proporcionados por el usuario.
ms.assetid: 7d132c2c-eab1-4132-b2b6-fa1f8b142f58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75214998ac54659196bd64100b806e5768df176e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791800"
---
# <a name="dialog-box-msaa-ui-element-reference"></a>Cuadro de diálogo (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **cuadro de diálogo** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **cuadro de diálogo** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un cuadro de diálogo es una ventana temporal que crea una aplicación para recuperar los datos proporcionados por el usuario. Una aplicación usa cuadros de diálogo para solicitar al usuario información adicional sobre los comandos que el usuario ha elegido en un menú. Un cuadro de diálogo contiene uno o más controles (ventanas secundarias) con los que el usuario escribe texto, elige opciones o dirige la acción del comando.

El nombre de la clase de ventana para los cuadros de diálogo es " \# 32770".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un cuadro de diálogo admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentarios                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Si el cuadro de diálogo contiene un botón de opción predeterminado, el método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) llama a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con el mensaje del botón [**\_ click de BM**](/windows/desktop/Controls/bm-click) para hacer clic en el botón de opción predeterminado. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                        |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                        |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                        |



 

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un cuadro de diálogo admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)                 | La propiedad **ChildCount** es igual al número de controles de ventana secundarios en el cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)           | Si el cuadro de diálogo contiene un botón de opción predeterminado, la propiedad **DEFAULTACTION** es "Press".                                                                                                                                                                                                                                                                                                                                                                             |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accKeyboardShortcut**](/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Normalmente, los cuadros de diálogo no tienen métodos abreviados de teclado. Si el texto de la ventana para el cuadro de diálogo contiene un carácter de y comercial (&), Microsoft Active Accessibility devuelve una cadena que no es NULL como la propiedad **KeyboardShortcut** .                                                                                                                                                                                                                                        |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                             | La propiedad **nombre** es el texto de la ventana, o título, que se muestra en la barra de título del cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                              |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                         | La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el cuadro de diálogo y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el cuadro de diálogo.                                                                                                                                                                                                                                                        |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                             | La propiedad **role** es el [**cuadro de \_ \_ diálogo de sistema de roles**](object-roles.md) o el sistema de [**roles \_ \_ PROPERTYPAGE**](object-roles.md).                                                                                                                                                                                                                                                                                                 |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                           | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md):[**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable<br/> |



 

## <a name="remarks"></a>Observaciones

El objeto de cuadro de diálogo no admite el método [**Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) . Para obtener un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a un control en un cuadro de diálogo, los clientes deben obtener el identificador de ventana del control y, a continuación, llamar a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

