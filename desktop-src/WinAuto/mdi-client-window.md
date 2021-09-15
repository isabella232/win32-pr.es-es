---
title: Ventana cliente de MDI (Referencia del elemento de interfaz de usuario de MSAA)
description: La interfaz de múltiples documentos (MDI) es una especificación que define la interfaz de usuario estándar para las aplicaciones escritas para Windows. Una aplicación MDI permite a un usuario trabajar con más de un documento a la vez.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567416"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>Ventana cliente de MDI (Referencia del elemento de interfaz de usuario de MSAA)

La interfaz de múltiples documentos (MDI) es una especificación que define la interfaz de usuario estándar para las aplicaciones escritas para Windows. Una aplicación MDI permite a un usuario trabajar con más de un documento a la vez.

Una aplicación MDI tiene tres tipos de ventanas: una ventana de marco, una ventana de cliente y varias ventanas secundarias. La ventana marco es como la ventana principal de una aplicación y rodea la ventana de cliente. La ventana de cliente es un elemento secundario de la ventana de marco y actúa como fondo para las ventanas secundarias. La ventana de cliente también proporciona compatibilidad para crear y manipular las ventanas secundarias en las que se muestran los documentos.

El nombre de clase de ventana para una ventana de cliente MDI es "MDIClient".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Una ventana de cliente MDI admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Una ventana de cliente MDI admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **propiedad ChildCount** es el número de ventanas secundarias en las que se muestran los documentos.                                                                                                                                                                                                                                                                                                                                                                              |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La **propiedad Name** es "Workspace".                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **propiedad Parent** es la ventana de marco MDI.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **propiedad Role** es ROLE SYSTEM [**\_ \_ CLIENT**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                  |
| [**get \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La **propiedad State** es una combinación de uno o varios de los valores siguientes: STATE SYSTEM [**\_ \_ INVISIBLE**](object-state-constants.md) STATE SYSTEM [](object-state-constants.md) \| [**\_ \_ UNAVAILABLE**](object-state-constants.md) STATE SYSTEM \| FOCUSED STATE SYSTEM [**\_ \_**](object-state-constants.md) \| [**\_ \_ FOCUSABLE**](object-state-constants.md)<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (Interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





