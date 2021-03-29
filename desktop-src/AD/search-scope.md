---
title: Especificar el ámbito de búsqueda
description: Puede especificar el ámbito de una búsqueda como una búsqueda base, de un nivel o de subárbol.
ms.assetid: b02354c2-7b95-4911-8ae3-4a261d3ca2d3
ms.tgt_platform: multiple
keywords:
- Especificar el ámbito de búsqueda AD
- Active Directory, buscar y especificar el ámbito de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ff076e0410088c69eace25f204241c1c51c6fb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789477"
---
# <a name="specifying-the-search-scope"></a>Especificar el ámbito de búsqueda

Puede especificar el ámbito de una búsqueda como una búsqueda base, de un nivel o de subárbol. Use la marca de **\_ ámbito de \_ búsqueda \_ de ADS SEARCHPREF** con los valores de la enumeración [**ADS \_ SCOPEENUM**](/windows/win32/api/iads/ne-iads-ads_scopeenum) para especificar el ámbito de búsqueda. La lista siguiente incluye descripciones de los tipos de búsqueda:

-   **Base**. Una búsqueda base limita la búsqueda al objeto base. El número máximo de objetos devueltos es siempre uno. Esta búsqueda es útil para comprobar la existencia de un objeto para recuperar la pertenencia a grupos. Por ejemplo, si tiene un nombre distintivo de objeto y debe comprobar la existencia del objeto en función de la ruta de acceso, puede usar una búsqueda de un solo nivel. Si se produce un error en la búsqueda, puede suponer que es posible que el objeto se haya cambiado de nombre o se haya pasado a una ubicación diferente, o que se le haya proporcionado la información incorrecta sobre el objeto. Tenga en cuenta que debe almacenar el identificador único global (GUID) del objeto en lugar del nombre distintivo, si desea volver a visitar un objeto. El GUID siempre hará referencia al mismo objeto, independientemente de dónde se encuentre el objeto dentro de la jerarquía de directorios.
-   **Un nivel**. Una búsqueda de un nivel está restringida a los elementos secundarios inmediatos de un objeto base, pero excluye el propio objeto base. Esta configuración puede realizar una búsqueda de destino para los objetos secundarios inmediatos de un objeto primario. Por ejemplo, considere un objeto primario P1 y sus elementos secundarios inmediatos: C1, C2 y C3. Una búsqueda de un nivel evalúa C1, C2 y C3 con respecto a los criterios de búsqueda, pero no evalúa P1. Use una búsqueda de un solo nivel para enumerar todos los elementos secundarios de un objeto. Una enumeración [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) se traduce en una búsqueda de un solo nivel.
-   **Subárbol**. Una búsqueda de subárbol (o una búsqueda en profundidad) incluye todos los objetos secundarios, así como el objeto base. Puede solicitar al proveedor LDAP que proseguir las referencias a otros servicios de directorio LDAP, incluidos otros bosques o dominios de directorio.

 

 