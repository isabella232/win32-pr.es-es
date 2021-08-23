---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cde3597a0922159eb035e94e08691cf9d36a07f8a1c23ec0cb25280ab961faa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118829543"
---
# <a name="elementhasnoname"></a>ElementHasNoName

## <a name="text"></a>Texto

El elemento no tiene nombre

## <a name="type"></a>Tipo

Error

## <a name="description"></a>Descripción

Un elemento no tiene un nombre. Por ejemplo, el elemento no tiene accName implementado y se devuelve una cadena vacía cuando se usa el método [**\_ get accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) para recuperar el nombre MSAA del elemento.

Este problema provoca problemas para las personas que dependen de un lector de pantalla y un teclado para la navegación porque un elemento podría identificarse incorrectamente para el usuario.

## <a name="possible-causes"></a>Causas posibles

-   El elemento o su elemento primario no tienen nombre ni etiqueta.
-   Al elemento se le asigna [**un accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) que sugiere que el elemento tiene un nombre.
-   El elemento que tiene el foco no debe recibir el foco. Por ejemplo, una etiqueta o un control deshabilitado.
-   Un control invisible ha recibido el foco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> </dl>

 

 




