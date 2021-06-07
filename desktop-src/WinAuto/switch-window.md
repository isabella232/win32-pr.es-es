---
title: Ventana Cambiar (Referencia del elemento de interfaz de usuario de MSAA)
description: La ventana de conmutador se muestra cada vez que un usuario presiona ALT+TAB para cambiar a otra aplicación. La ventana de conmutador contiene un icono para cada aplicación que se está ejecutando actualmente.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443986"
---
# <a name="switch-window-msaa-ui-element-reference"></a>Ventana Cambiar (Referencia del elemento de interfaz de usuario de MSAA)

La ventana de conmutador se muestra cada vez que un usuario presiona ALT+TAB para cambiar a otra aplicación. La ventana de conmutador contiene un icono para cada aplicación que se está ejecutando actualmente.

El nombre de clase de ventana para la ventana del conmutador es \# "32771".

## <a name="iaccessible-methods"></a>Métodos IAccessible

La ventana switch admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Método                                                                    | Comentarios                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | El propio objeto de ventana switch no tiene una **propiedad DefaultAction.** El [**método accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) para cada elemento de la ventana de modificador activa el elemento especificado. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a>Propiedades IAccessible

La ventana switch admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



|      Propiedad                                                                          |      Descripción                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La **propiedad ChildCount** es cero.                                                                                                                                                                                           |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | El propio objeto de ventana switch no tiene una **propiedad DefaultAction.** La **propiedad DefaultAction** para cada elemento de la ventana de modificador es "Switch".                                                                     |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | El objeto primario de la ventana de conmutador no puede recibir el foco; solo los elementos secundarios individuales pueden recibir el foco.                                                                                                                          |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | El propio objeto de ventana de modificador no tiene una **propiedad Name.** La **propiedad** Nombre de cada icono de aplicación de la ventana del conmutador es la misma que el nombre de la aplicación que se muestra.                                         |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | El propio objeto de ventana de modificador tiene **una propiedad Role** de "ventana \[ 32771". \] Además, cada icono de aplicación de la ventana de modificador tiene **la** propiedad Role [**ROLE SYSTEM \_ \_ LISTITEM**](object-roles.md). |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | El propio objeto de ventana de modificador no admite la **propiedad State.** El **valor de** Estado de los elementos de vista de lista es STATE SYSTEM [**\_ \_ FOCUSABLE.**](object-state-constants.md)                     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




