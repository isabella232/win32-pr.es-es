---
title: Control header (referencia de elementos de interfaz de usuario de MSAA)
description: Un control de encabezado muestra los encabezados en la parte superior de las columnas de información y permite que el usuario ordene la información haciendo clic en los encabezados. El explorador de Windows utiliza un control de encabezado cuando se selecciona la vista de detalles.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357463"
---
# <a name="header-control-msaa-ui-element-reference"></a>Control header (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **control de encabezado** para la referencia de elementos de interfaz de usuario de MSAA. Cómo crear objetos de **control de encabezado** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

Un control de encabezado muestra los encabezados en la parte superior de las columnas de información y permite que el usuario ordene la información haciendo clic en los encabezados. El explorador de Windows utiliza un control de encabezado cuando se selecciona la vista de detalles.

El nombre de clase de ventana de un control de encabezado es WC \_ header, que se define como "SysHeader32" en commctrl. h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un control de encabezado admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Método                                                                    | Comentarios                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Este método realiza la acción predeterminada haciendo clic en el encabezado. |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Un control de encabezado admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



| Propiedad                                                                       | Comentarios                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La propiedad **ChildCount** es cero.                                                                                                                                                                                                   |
| [**obtener \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | La propiedad **DEFAULTACTION** es "click".                                                                                                                                                                                             |
| [**obtener \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**obtener \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | La propiedad **Name** es igual que el nombre del encabezado de columna.                                                                                                                                                                    |
| [**obtener \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | La propiedad **primaria** es una ventana ( [**\_ \_ lista de sistema de roles**](object-roles.md) ) que rodea el control y tiene el mismo nombre de clase de ventana que el control.                                                      |
| [**obtener \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | La propiedad **role** es el [**sistema de rol \_ \_ COLUMNHEADER**](object-roles.md).                                                                                                                                  |
| [**obtener \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | El valor de la propiedad **State** es siempre [**el \_ estado \_ ReadOnly del sistema**](object-state-constants.md) y también puede incluir el [**sistema de estado \_ \_ invisible**](object-state-constants.md). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




