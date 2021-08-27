---
title: Caret (Referencia del elemento de interfaz de usuario de MSAA)
description: El elemento de referencia es una línea parpadeante, un bloque o un mapa de bits en el área cliente de una ventana o en un control que acepta la entrada del teclado.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f846940a9180885da84cf8a030672b1473eab
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467302"
---
# <a name="caret-msaa-ui-element-reference"></a>Caret (Referencia del elemento de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los elementos de la interfaz de usuario de MSAA para fines de referencia. Aquí no se describe cómo usar los elementos de interfaz de usuario en varios marcos de interfaz de usuario. Consulte la documentación de referencia de API para el marco de interfaz de usuario que está usando.

 

El elemento de referencia es una línea parpadeante, un bloque o un mapa de bits en el área cliente de una ventana o en un control que acepta la entrada del teclado. Indica el lugar en el que se inserta texto o gráficos. Dado que solo una ventana a la vez tiene el foco del teclado, solo hay un centro de diálogo en el sistema.

## <a name="iaccessible-methods"></a>Métodos IAccessible

El caret admite los siguientes métodos [**IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Propiedades IAccessible

El caret admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)




| Propiedad | Comentarios | 
|----------|----------|
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a> | La <strong>propiedad ChildCount</strong> es cero. | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a> | La <strong>propiedad</strong> Name es "Edit". | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a> | La <strong>propiedad Role</strong> es <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>. | 
| <a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a> | Entre los valores posibles de <strong>la propiedad State</strong> se incluyen:<ul><li>Cero, lo que significa que el signo de referencia está visible</li><li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li></ul> | 




 

## <a name="notes"></a>Notas

-   A diferencia de otros elementos de la interfaz de usuario, el objeto de aviso no tiene un identificador de ventana asociado. Para obtener acceso al objeto de caret, los clientes deben establecer [*winEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y esperar a que el objeto de caret genere eventos.
-   El objeto de cursor del control de edición enriquecido proporcionado por Riched20.dll (que se usa en editores de texto como Microsoft WordPad en Windows 98) no envía [winevents](winevents-infrastructure.md) cuando se cambia su posición durante la selección de texto. Cuando los usuarios presionan MAYÚS y las teclas de dirección para seleccionar texto, el objeto de cursor no desencadena [**EVENT \_ OBJECT \_ LOCATIONCHANGE**](event-constants.md) WinEvent. De forma similar, cuando la selección se establece mediante programación a través de mensajes de edición enriquecidos, el objeto de cursor no envía ningún evento para indicar su nueva posición.

    Todas las aplicaciones que usan Riched20.dll muestran este problema. Las aplicaciones que usan versiones anteriores del control de edición enriquecido envían correctamente eventos en función de la selección.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaz IAccessible](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




