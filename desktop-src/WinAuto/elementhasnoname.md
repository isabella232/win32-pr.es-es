---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357768"
---
# <a name="elementhasnoname"></a>ElementHasNoName

## <a name="text"></a>Texto

El elemento no tiene nombre

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento no tiene un nombre. Por ejemplo, el elemento no tiene accName implementado y se devuelve una cadena vacía cuando se usa el método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) para recuperar el nombre de MSAA del elemento.

Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque un elemento podría identificarse incorrectamente al usuario.

## <a name="possible-causes"></a>Causas posibles

-   El elemento o su elemento primario no tiene nombre o etiqueta.
-   Al elemento se le asigna un [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) que sugiere que el elemento tiene un nombre.
-   El elemento que tiene el foco no debe recibir el foco. Por ejemplo, una etiqueta o un control deshabilitado.
-   Un control invisible ha recibido el foco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> </dl>

 

 




