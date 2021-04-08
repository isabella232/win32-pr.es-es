---
title: Ventana de cliente MDI (referencia de elementos de interfaz de usuario de MSAA)
description: La interfaz de múltiples documentos (MDI) es una especificación que define la interfaz de usuario estándar para las aplicaciones escritas para Windows. Una aplicación MDI permite a un usuario trabajar con más de un documento a la vez.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994184"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a>Ventana de cliente MDI (referencia de elementos de interfaz de usuario de MSAA)

La interfaz de múltiples documentos (MDI) es una especificación que define la interfaz de usuario estándar para las aplicaciones escritas para Windows. Una aplicación MDI permite a un usuario trabajar con más de un documento a la vez.

Una aplicación MDI tiene tres tipos de ventanas: una ventana de marco, una ventana de cliente y un número de ventanas secundarias. La ventana de marco es similar a la ventana principal de una aplicación y se rodea a la ventana de cliente. La ventana de cliente es un elemento secundario de la ventana de marco y sirve de fondo para las ventanas secundarias. La ventana de cliente también proporciona compatibilidad para crear y manipular las ventanas secundarias en las que se muestran los documentos.

El nombre de la clase de ventana de una ventana de cliente MDI es "MDIClient".

## <a name="iaccessible-methods"></a>Métodos IAccessible

Una ventana de cliente MDI admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Una ventana de cliente MDI admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La propiedad **ChildCount** es el número de ventanas secundarias en las que se muestran los documentos.                                                                                                                                                                                                                                                                                                                                                                              |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propiedad **Name** es "Workspace".                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La propiedad **primaria** es la ventana de marco MDI.                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propiedad **role** es [**el \_ \_ cliente del sistema de roles**](object-roles.md)                                                                                                                                                                                                                                                                                                                                                                                  |
| [**obtener \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





