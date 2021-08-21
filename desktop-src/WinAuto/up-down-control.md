---
title: Up-Down control (referencia de elemento de la interfaz de usuario de MSAA)
description: Un control de flechas, también conocido como control de número, combina un par de botones que se muestran como flechas con un control de edición de compañeros. Al hacer clic en las flechas se incrementa o disminuye el valor del control de edición.
ms.assetid: 45e56c0f-4ac6-4731-b9a6-be4613bf40ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b9475d8bbca24d2bf536a4eb9a9decf078297e788a37aa4d8560029a67e50e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118114630"
---
# <a name="up-down-control-msaa-ui-element-reference"></a>Up-Down control (referencia de elemento de la interfaz de usuario de MSAA)

> [!Note]  
> En este tema se **describen los objetos de control de** nivel superior para fines de referencia de elementos de la interfaz de usuario de MSAA. Aquí no se describe cómo crear **objetos de control** de arriba a abajo en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

Un control de flechas, también conocido como control de número, combina un par de botones que se muestran como flechas con un control de edición de compañeros. Al hacer clic en las flechas se incrementa o disminuye el valor del control de edición.

El nombre de clase de ventana de un control de flechas es UPDOWN CLASS, que se define como \_ "msctls \_ updown32" en Commctrl.h.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Un control de arriba a abajo admite los métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) siguientes:

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

Un control de arriba a abajo admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)



| Propiedad                                                                 | Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accChildCount**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | La **propiedad ChildCount** es "2" (los botones de flecha arriba y abajo).                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**get \_ accFocus**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelp**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelp)             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accHelpTopic**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acchelptopic)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | La **propiedad Name** del objeto de control de arriba a abajo se obtiene del texto de la ventana del control (o título). Este texto no se muestra con el control de flechas, por lo que los desarrolladores de servidores deben proporcionar texto significativo en la instrucción de definición de recursos del control para ayudar a los usuarios de utilidades cliente a identificar el control. La **propiedad** Nombre del botón de flecha superior del control de  arriba a abajo es "Más" y la propiedad Nombre del botón de flecha inferior es "Less". |
| [**get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | La **propiedad** Parent del control de arriba a abajo es una ventana [**(ROLE SYSTEM \_ \_ WINDOW)**](object-roles.md) que rodea el control y tiene la misma propiedad **Name** y el mismo nombre de clase de ventana que el control. La **propiedad Parent** de los botones de flecha arriba y abajo es el objeto de control hacia abajo.                                                                                                                                                    |
| [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | La **propiedad Role** para el objeto de control de arriba a abajo es ROLE SYSTEM [**\_ \_ SPINBUTTON**](object-roles.md). La **propiedad Role** de los botones de flecha es ROLE SYSTEM [**\_ \_ PUSHBUTTON**](object-roles.md).                                                                                                                                                                                                                          |
| [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | La propiedad State para el objeto de control de arriba a abajo es uno de los valores [siguientes:](object-state-constants.md)[**STATE SYSTEM \_ \_ FOCUSED**](object-state-constants.md) \| [**STATE SYSTEM \_ \_ FOCUSABLE**](object-state-constants.md)<br/>                                                                                                                                                                                      |
| [**get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

## <a name="notes"></a>Notas

Microsoft Active Accessibility expone el control de edición de compañeros como un objeto independiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





