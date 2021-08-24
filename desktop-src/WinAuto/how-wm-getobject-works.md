---
title: Cómo funciona WM_GETOBJECT
description: Microsoft Active Accessibility el mensaje GETOBJECT de WM a la aplicación de servidor adecuada cuando un cliente \_ llama a una de las funciones AccessibleObjectFromX.
ms.assetid: 53f7b3db-97e4-4ff2-9f7a-4555ec7956ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24309b304baede0c7b93c9e609b469991e737ca819e8014effa03a4f39b8772c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795765"
---
# <a name="how-wm_getobject-works"></a>Funcionamiento de WM \_ GETOBJECT

Microsoft Active Accessibility el mensaje [**\_ GETOBJECT**](wm-getobject.md) de WM a la aplicación de servidor adecuada cuando un cliente llama a una de las **funciones AccessibleObjectFrom**_X._ En la lista siguiente se describen los distintos escenarios que se producen:

-   Si la ventana o el control que recibe [**WM \_ GETOBJECT**](wm-getobject.md) implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), la ventana devuelve una referencia a la **interfaz IAccessible** mediante [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject). Microsoft Active Accessibility, junto con la biblioteca del modelo de objetos componentes (COM), realiza la serialización adecuada y pasa el puntero de interfaz del servidor al cliente.
-   Si la ventana que recibe el mensaje no implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible), debe devolver cero.
-   Si la ventana no controla el mensaje [**\_ GETOBJECT de WM,**](wm-getobject.md) la [función DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) devuelve cero.

Incluso si el servidor devuelve cero, Microsoft Active Accessibility proporciona al cliente información sobre el objeto . Para la mayoría de los objetos proporcionados por el sistema, como los botones y cuadros de lista, Microsoft Active Accessibility proporciona información completa; para otros objetos, la información es limitada. Por ejemplo, Microsoft Active Accessibility no proporciona información para los controles que no tienen un identificador de ventana. Microsoft Active Accessibility devuelve un puntero de [**interfaz IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con proxy que el cliente usa para obtener información sobre el objeto.

Para obtener más información, [vea The WM \_ GETOBJECT Message](the-wm-getobject-message.md).

 

 