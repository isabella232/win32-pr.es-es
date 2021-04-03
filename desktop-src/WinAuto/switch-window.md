---
title: Ventana conmutador (referencia de elementos de interfaz de usuario de MSAA)
description: La ventana conmutador aparece siempre que un usuario presiona ALT + TAB para cambiar a otra aplicación. La ventana conmutador contiene un icono para cada aplicación que se está ejecutando.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779663"
---
# <a name="switch-window-msaa-ui-element-reference"></a>Ventana conmutador (referencia de elementos de interfaz de usuario de MSAA)

La ventana conmutador aparece siempre que un usuario presiona ALT + TAB para cambiar a otra aplicación. La ventana conmutador contiene un icono para cada aplicación que se está ejecutando.

El nombre de la clase de ventana de la ventana de conmutador es " \# 32771".

## <a name="iaccessible-methods"></a>Métodos IAccessible

La ventana switch admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentarios                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | El propio objeto de ventana modificador no tiene una propiedad **DEFAULTACTION** . El método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) de cada elemento de la ventana switch activa el elemento especificado. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

La ventana switch admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La propiedad **ChildCount** es cero.                                                                                                                                                                                           |
| [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | El propio objeto de ventana modificador no tiene una propiedad **DEFAULTACTION** . La propiedad **DEFAULTACTION** de cada elemento de la ventana switch es "switch".                                                                     |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | El objeto primario de la ventana de conmutador no puede recibir el foco; solo los elementos secundarios individuales pueden recibir el foco.                                                                                                                          |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | El propio objeto de ventana conmutador no tiene una propiedad **nombre** . La propiedad **Name** de cada icono de la aplicación en la ventana de conmutador es igual que el nombre de aplicación mostrado.                                         |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | El propio objeto de ventana conmutador tiene una propiedad **role** de "Window \[ 32771 \] ". Además, cada icono de aplicación de la ventana de conmutador tiene la propiedad de **rol** [**\_ \_ ListItem del sistema de rol**](object-roles.md). |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | El propio objeto de ventana modificador no admite la propiedad **State** . El valor de **Estado** de los elementos de la vista de lista es el [**sistema de estado \_ \_ enfocable**](object-state-constants.md).                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




