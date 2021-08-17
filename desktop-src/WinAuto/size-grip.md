---
title: Control de tamaño (referencia del elemento de la interfaz de usuario de MSAA)
description: El control de tamaño es un puntero especial del mouse en la esquina inferior derecha de una ventana que permite al usuario hacer clic y arrastrar el control de tamaño para cambiar el tamaño de la ventana.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7315425720ddee8beaf0f7c1f1b2ecbd8ba0fada51e64dc70453f3bb477e1f6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795654"
---
# <a name="size-grip-msaa-ui-element-reference"></a>Control de tamaño (referencia del elemento de la interfaz de usuario de MSAA)

El control de tamaño es un puntero especial del mouse en la esquina inferior derecha de una ventana que permite al usuario hacer clic y arrastrar el control de tamaño para cambiar el tamaño de la ventana.

## <a name="iaccessible-methods"></a>Métodos IAccessible

El control de tamaño admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

El control de tamaño admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                   | Comentarios                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accDescription**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | La **propiedad Description** es "Se puede usar para cambiar el ancho y el alto de una ventana".                                                                                   |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | La **propiedad Name** es "Size box".                                                                                                                                   |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | Ventana que contiene el control de tamaño.                                                                                                                                |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | La **propiedad Role** es ROLE SYSTEM [**\_ \_ GRIP.**](object-roles.md)                                                                                  |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | El valor de la **propiedad State** es cero, lo que significa que el objeto está visible o STATE [**SYSTEM \_ \_ INVISIBLE.**](object-state-constants.md) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




