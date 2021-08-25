---
title: AccNameShouldNotContainRole
description: AccNameShouldNotContainRole
ms.assetid: 271461FF-5123-482F-B66D-A323CB3361DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8f09bd9ccdf27c5f52a45466b6b8145cfe23248cc175777f57202aac6530791
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899735"
---
# <a name="accnameshouldnotcontainrole"></a>AccNameShouldNotContainRole

## <a name="text"></a>Texto

El nombre del elemento ( ) no debe contener el texto del rol {0} del elemento ( {1} )

## <a name="type"></a>Tipo

Advertencia

## <a name="description"></a>Descripción

El nombre de un elemento incorpora su rol MSAA o tipo de control UIA. Por ejemplo, esta advertencia puede producirse si el método [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) (que se usa para recuperar el nombre MSAA de un elemento) devuelve "ROLE \_ SYSTEM \_ \_ SCROLLBAR". \*

Este problema provoca problemas para las personas que se basan en un lector de pantalla y un teclado para la navegación porque el rol se leerá dos veces o puede ser poco reconocible o no intuitivo para los usuarios.

## <a name="possible-causes"></a>Causas posibles

-   El elemento o su elemento primario tienen un nombre o etiqueta asignados incorrectamente.
-   El elemento o su elemento primario tiene un nombre predeterminado que no se ha revisado a un nombre descriptivo. Por ejemplo, button1.
-   Un desarrollador no es consciente de que los lectores de pantalla leen nombres.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[Propiedad Name](name-property.md)
</dt> </dl>

 

 




