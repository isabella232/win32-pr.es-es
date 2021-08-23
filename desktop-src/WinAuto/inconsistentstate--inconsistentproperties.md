---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30533125c342bd80134c9eab45f14917a3b3ad04af9d969140c49502cbfd192a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644845"
---
# <a name="inconsistentstate-inconsistentproperties"></a>InconsistentState, InconsistentProperties

## <a name="text"></a>Texto

Un control tiene estados o propiedades que son incoherentes {0} y {1}

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento informa de estados MSAA incoherentes o en conflicto Automatización de la interfaz de usuario propiedades. Por ejemplo, cuando el [**método get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) devuelve cualquiera de las combinaciones siguientes.

-   SISTEMA \_ DE \_ ESTADO EXPANDIDO Y SISTEMA DE ESTADO \_ \_ CONTRAÍDO
-   SISTEMA \_ DE ESTADO SELECCIONADO Y NO SISTEMA DE ESTADO \_ \_ \_ SELECCIONABLE
-   SISTEMA \_ DE ESTADO CENTRADO Y NO SISTEMA DE ESTADO \_ \_ \_ FOCUSABLE

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación, ya que es posible que se notifica al usuario un estado de elemento incorrecto.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tienen un estado MSAA establecido de forma inapropiada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Constantes de estado de objeto**](object-state-constants.md)
</dt> <dt>

[Estados y propiedades](uiauto-msaa.md)
</dt> </dl>

 

 




