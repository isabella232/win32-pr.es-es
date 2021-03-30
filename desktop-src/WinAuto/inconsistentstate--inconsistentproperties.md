---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774263"
---
# <a name="inconsistentstate-inconsistentproperties"></a>InconsistentState, InconsistentProperties

## <a name="text"></a>Texto

Un control tiene Estados/propiedades incoherentes {0} y {1}

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento informa de los Estados de MSAA incoherentes o en conflicto o de las propiedades de automatización de la interfaz de usuario. Por ejemplo, cuando el método [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) devuelve cualquiera de las siguientes combinaciones.

-   Sistema \_ \_ de estado expandido y sistema de estado \_ \_ contraído
-   \_Sistema \_ de estado seleccionado y no \_ seleccionable del sistema de estado \_
-   \_Sistema \_ de estado centrado y sin \_ sistema de estado \_ enfocable

Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque es posible que se notifique al usuario un estado incorrecto del elemento.

## <a name="possible-causes"></a>Causas posibles

El elemento o su elemento primario tiene un estado de MSAA establecido incorrectamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[**Constantes de estado de objeto**](object-state-constants.md)
</dt> <dt>

[Estados y propiedades](uiauto-msaa.md)
</dt> </dl>

 

 




