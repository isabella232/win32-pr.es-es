---
title: Cuadro de diálogo (Referencia del elemento de interfaz de usuario de MSAA)
description: Un cuadro de diálogo es una ventana temporal que una aplicación crea para recuperar la entrada del usuario.
ms.assetid: 7d132c2c-eab1-4132-b2b6-fa1f8b142f58
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52abc4f08dabb8bfc96c83b5323951135bc4042d87b4e443e29fb1ecd5592852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122235"
---
# <a name="dialog-box-msaa-ui-element-reference"></a>Cuadro de diálogo (Referencia del elemento de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de cuadro** de diálogo para fines de referencia de elementos de interfaz de usuario de MSAA. Cómo crear objetos **de cuadro de diálogo** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un cuadro de diálogo es una ventana temporal que una aplicación crea para recuperar la entrada del usuario. Una aplicación usa cuadros de diálogo para solicitar al usuario información adicional sobre los comandos que el usuario ha elegido en un menú. Un cuadro de diálogo contiene uno o varios controles (ventanas secundarias) con los que el usuario escribe texto, elige opciones o dirige la acción del comando.

El nombre de clase de ventana de los cuadros de diálogo \# es "32770".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un cuadro de diálogo admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Método                                                                    | Comentarios                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Si el cuadro de diálogo contiene un botón de inserción predeterminado, el método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) llama a [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) con el mensaje de botón [**BM \_ CLICK**](/windows/desktop/Controls/bm-click) para hacer clic en el botón de inserción predeterminado. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                                                                        |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                                                                        |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                                                                        |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                                                                        |



 

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un cuadro de diálogo admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)                 | La **propiedad ChildCount** es igual al número de controles de ventana secundarios en el cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction)           | Si el cuadro de diálogo contiene un botón de inserción predeterminado, la **propiedad DefaultAction** es "Press".                                                                                                                                                                                                                                                                                                                                                                             |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accKeyboardShortcut**](/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | Normalmente, los cuadros de diálogo no tienen métodos abreviados de teclado. Si el texto de la ventana del cuadro de diálogo contiene un carácter de yerba (&), Microsoft Active Accessibility devuelve una cadena que no es NULL como la **propiedad KeyboardShortcut.**                                                                                                                                                                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                             | La **propiedad** Nombre es el texto de la ventana, o título, que se muestra en la barra de título del cuadro de diálogo.                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                         | La **propiedad** Parent es una ventana [**(ROLE SYSTEM \_ \_ WINDOW)**](object-roles.md) que rodea el cuadro de diálogo y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el cuadro de diálogo.                                                                                                                                                                                                                                                        |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                             | La **propiedad Role** es ROLE SYSTEM DIALOG [**\_ \_ o**](object-roles.md) [**ROLE SYSTEM \_ \_ PROPERTYPAGE**](object-roles.md).                                                                                                                                                                                                                                                                                                 |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                           | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSED**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="remarks"></a>Comentarios

El objeto dialog no admite el [**método \_ get accChild.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild) Para obtener un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a un control en un cuadro de diálogo, los clientes deben obtener el identificador de ventana del control y, a continuación, llamar a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

