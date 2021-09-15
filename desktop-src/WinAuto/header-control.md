---
title: Control de encabezado (referencia de elemento de la interfaz de usuario de MSAA)
description: Un control de encabezado muestra encabezados en la parte superior de las columnas de información y permite al usuario ordenar la información haciendo clic en los encabezados. Windows El Explorador usa un control de encabezado cuando se selecciona la vista Detalles.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465707"
---
# <a name="header-control-msaa-ui-element-reference"></a>Control de encabezado (referencia de elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen **los objetos de control** de encabezado para fines de referencia de elementos de la interfaz de usuario de MSAA. Cómo crear objetos **de control de** encabezado en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un control de encabezado muestra encabezados en la parte superior de las columnas de información y permite al usuario ordenar la información haciendo clic en los encabezados. Windows El Explorador usa un control de encabezado cuando se selecciona la vista Detalles.

El nombre de clase de ventana de un control de encabezado es WC HEADER, que se define como \_ "SysHeader32" en Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un control de encabezado admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Método                                                                    | Comentarios                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | Este método realiza la acción predeterminada haciendo clic en el encabezado . |
| [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un control de encabezado admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                       | Comentarios                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | La **propiedad ChildCount** es cero.                                                                                                                                                                                                   |
| [**get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | La **propiedad DefaultAction** es "Click".                                                                                                                                                                                             |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | La **propiedad Name** es la misma que el nombre del encabezado de columna.                                                                                                                                                                    |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | La **propiedad Parent** es una ventana [**(ROLE SYSTEM \_ \_ LIST)**](object-roles.md) que rodea el control y tiene el mismo nombre de clase de ventana que el control.                                                      |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | La **propiedad Role** es ROLE SYSTEM [**\_ \_ COLUMNHEADER.**](object-roles.md)                                                                                                                                  |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | El valor de la **propiedad State** siempre es STATE [**SYSTEM \_ \_ READONLY**](object-state-constants.md) y también puede incluir [**STATE SYSTEM \_ \_ INVISIBLE**](object-state-constants.md). |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




