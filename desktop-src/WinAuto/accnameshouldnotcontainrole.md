---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fb91eeeb34d484c1f51cd0b7cd2d2947e86abda
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779729"
---
# <a name="accnameshouldnotcontainrole"></a>AccNameShouldNotContainRole

## <a name="text"></a>Texto

El nombre del elemento ( {0} ) no debe contener el texto del rol del elemento ( {1} )

## <a name="type"></a>Tipo

Advertencia

## <a name="description"></a>Descripción

El nombre de un elemento incorpora su rol de MSAA o el tipo de control UIA. Por ejemplo, esta advertencia puede producirse si el método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) (que se usa para recuperar el nombre de MSAA de un elemento) devuelve \_ " \_ ScrollBar System ScrollBar \_ \* ".

Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque el rol se leerá dos veces, o puede que no sea pronunciable o no intuitivo para los usuarios.

## <a name="possible-causes"></a>Causas posibles

-   El elemento o su elemento primario tiene un nombre o una etiqueta asignados incorrectamente.
-   El elemento o su elemento primario tiene un nombre predeterminado que no se ha revisado en un nombre descriptivo. Por ejemplo, button1.
-   Un desarrollador no es consciente de que los lectores de pantalla leen los nombres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible:: get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> </dl>

 

 




