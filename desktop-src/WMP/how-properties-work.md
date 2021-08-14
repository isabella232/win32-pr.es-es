---
title: Cómo funcionan las propiedades
description: Cómo funcionan las propiedades
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Reproductor de Windows Media complementos, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, propiedades de ejemplo de eco
- Complementos de DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdefea3fce39b70d20d2f100d36cc4aeb8770bd15cd5cd0bf0978cd08f2259f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339139"
---
# <a name="how-properties-work"></a>Cómo funcionan las propiedades

Los valores de propiedad se almacenan en variables miembro.

Los pares de métodos hacen que las propiedades sean accesibles. Un método proporciona la implementación para especificar el valor de propiedad; su nombre comienza por put \_ . El otro método proporciona la implementación para recuperar el valor de propiedad; su nombre comienza por get \_ . La definición de interfaz está en Echo.idl. Los prototipos del método de propiedad están en Echo.h. Se implementan en Echo.cpp.

En las tres secciones siguientes se muestra cómo modificar los métodos de propiedad existentes para satisfacer sus necesidades y cómo agregar los métodos para una propiedad adicional.

-   [Variables para almacenar propiedades](variables-to-store-properties.md)
-   [Modificar la propiedad Scale](modifying-the-scale-property.md)
-   [Adición de la propiedad Mezcla mezclada](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedades de ejemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




