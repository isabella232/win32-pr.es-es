---
title: Barra de título (Referencia de elementos de la interfaz de usuario de MSAA)
description: La barra de título de la parte superior de una ventana muestra un icono definido por la aplicación y una línea de texto.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 620fa8716cb498857cdf12c652b99f409e6e4214
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070601"
---
# <a name="title-bar-msaa-ui-element-reference"></a>Barra de título (Referencia de elementos de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de barra** de título para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos de **barra de** título en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

La barra de título de la parte superior de una ventana muestra un icono definido por la aplicación y una línea de texto. El texto especifica el nombre de la aplicación e indica el propósito de la ventana. La barra de título también permite al usuario mover la ventana mediante un mouse u otro dispositivo que señala.

Las barras de título contienen al menos tres botones pequeños que minimizan, maximizan o restauran, y cierran la ventana asociada a la barra de título. Las barras de título también contienen un botón ayuda contextual. Las aplicaciones que se ejecutan en Far-East versión del Windows operativo también pueden contener botones del Editor de métodos de entrada (IME). Microsoft Active Accessibility expone estos botones como elementos secundarios de la barra de título.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Las barras de título admiten los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) siguientes:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Las barras de título admiten las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)




| Propiedad | Comentarios | 
|----------|----------|
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a> | La <strong>propiedad ChildCount</strong> es cinco. La <strong>propiedad ChildCount</strong> incluye el IME y los botones de Ayuda contextual incluso cuando no se muestran. Los botones que no se muestran tienen la <strong>propiedad State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>. | 
| <strong>get_accDescription</strong> | La <strong>propiedad Description</strong> de la propia barra de título es: "Muestra el nombre de la ventana y contiene controles para manipularla". Los botones secundarios de la barra de título tienen las descripciones siguientes:<br /><ul><li>"Mueve la ventana fuera de</li><li>"Hace que la ventana se llena</li><li>"Coloca un minimizado o</li><li>"Cierra la ventana"</li><li>"Entra o sale del contexto:</li><li>"Abre el teclado cuando se presiona"</li></ul> | 
| <strong>get_accName</strong> | La propia barra de título no admite la <strong>propiedad Name.</strong> Los botones secundarios de la barra de título tienen los nombres siguientes:<ul><li>"Minimizar"</li><li>"Maximizar" o "Restaurar",</li><li>"Cerrar"</li><li>"Ayuda de contexto"</li><li>"IME"</li></ul> | 
| <strong>get_accParent</strong> | La <strong>propiedad Parent</strong> de la barra de título es la ventana principal de la aplicación <a href="object-roles.md"><strong>(ROLE_SYSTEM_WINDOW</strong></a> ) que tiene el mismo nombre de clase de ventana definido por la aplicación que la barra de título. | 
| <strong>get_accRole</strong> | La <strong>propiedad Role</strong> es <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>. Los botones secundarios de la barra de título tienen la <strong>propiedad Role</strong> <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>. | 
| <strong>get_accState</strong> | La <strong>propiedad State</strong> de la barra de título y los botones secundarios puede ser una combinación de uno o varios de los valores <a href="object-state-constants.md">siguientes:</a> <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a> | <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br /> | 
| <strong>get_accValue</strong> | La <strong>propiedad Value</strong> es una cadena que es la misma que el texto mostrado en la barra de título. | 




 

## <a name="notes"></a>Notas

-   Aunque la barra de título  de una aplicación tiene la marca de propiedad [**State STATE \_ SYSTEM \_ FOCUSABLE**](object-state-constants.md), nunca tiene la marca **de** estado STATE [**SYSTEM \_ \_ FOCUSED**](object-state-constants.md). Al establecer el foco en un objeto de barra de título, se centra la ventana de la aplicación.
-   Dado que el objeto de barra de título no admite [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), los botones de la barra de título son elementos simples. No admiten la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) por sí mismos. El objeto de barra de título proporciona información sobre estos botones secundarios.
-   Dado que las barras de título no obtienen el foco y no tienen ninguna acción predeterminada, los métodos [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) y [**\_ get accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) no se admiten para este control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





