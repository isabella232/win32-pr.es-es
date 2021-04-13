---
title: Ventana de escritorio (referencia de elementos de interfaz de usuario de MSAA)
description: La ventana escritorio muestra la vista de lista de escritorio (que contiene iconos como Mi PC) y la barra de tareas que contiene el botón Inicio.
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418456"
---
# <a name="desktop-window-msaa-ui-element-reference"></a>Ventana de escritorio (referencia de elementos de interfaz de usuario de MSAA)

La ventana escritorio muestra la vista de lista de escritorio (que contiene iconos como Mi PC) y la barra de tareas que contiene el botón **Inicio** .

Los clientes raramente consultan este objeto porque la vista de lista y la barra de tareas cubren todo el escritorio. El objeto de escritorio se recupera al iniciar sesión, antes de que el Shell del sistema operativo muestre la vista de lista y la barra de tareas. En algunos casos, el escritorio se obtiene al navegar desde otros objetos.

El nombre de la clase de ventana de la ventana de escritorio es " \# 32769".

## <a name="iaccessible-methods"></a>Métodos IAccessible

La ventana de escritorio admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

La ventana de escritorio admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La propiedad de nombre es "escritorio".                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La propiedad **role** es [**el \_ \_ cliente del sistema de roles**](object-roles.md).                                                                                                                                                                                                                                                                                                                                                                                |
| [**obtener \_ accSelection**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md):[**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





