---
title: Control Barra de estado (Referencia del elemento de la interfaz de usuario de MSAA)
description: Las barras de estado muestran información de estado en una ventana horizontal en la parte inferior de una ventana de aplicación.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6c4955bfe10bc7eb224213a8e2e262179d2b122ca4eae210d0d1e72e4635b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119998065"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a>Control Barra de estado (Referencia del elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de control de barra** de estado para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos **de control de barra de** estado en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Las barras de estado muestran información de estado en una ventana horizontal en la parte inferior de una ventana de aplicación. Las barras de estado a menudo se dividen en partes, denominadas paneles, y cada panel muestra información de estado diferente. Además, las barras de estado pueden contener objetos de diferentes tipos, incluidos botones y barras de progreso. El nombre de clase de ventana para un control de barra de estado es STATUSCLASSNAME, que se define como "msctls \_ statusbar32" en Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Las barras de estado admiten los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Las barras de estado admiten las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **propiedad ChildCount** es el número de paneles de la barra de estado.                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | El propio objeto de barra de estado no tiene una **propiedad Name.** La **propiedad** Nombre de cada panel de la barra de estado es la misma que la del texto mostrado.                                                                                                                                                                                                                                                                                                                   |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **propiedad Parent** del objeto de barra de estado es una ventana [**(ROLE SYSTEM \_ \_ WINDOW)**](object-roles.md) que rodea el control y tiene el mismo nombre de clase de ventana que el control. La **propiedad Parent** de los paneles de la barra de estado es el objeto de la barra de estado.                                                                                                                                                                           |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **propiedad Role** del propio objeto de barra de estado es ROLE SYSTEM [**\_ \_ STATUSBAR**](object-roles.md). El texto mostrado en una barra de estado tiene [**ROLE \_ SYSTEM \_ STATICTEXT**](object-roles.md) como su **propiedad Role.**                                                                                                                                                                                                 |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSED**](object-state-constants.md) STATE SYSTEM \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="notes"></a>Notas

Dado que no se admiten métodos abreviados de teclado para controles de barra de estado o áreas de texto en barras de estado, no se [**\_ admite get accKeyboardShortcut.**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





