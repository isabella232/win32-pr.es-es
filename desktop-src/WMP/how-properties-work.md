---
title: Cómo funcionan las propiedades
description: Cómo funcionan las propiedades
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Reproductor de Windows Media complementos, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- complementos de procesamiento de señales digitales, propiedades de ejemplo de eco
- Complementos DE DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476238"
---
# <a name="how-properties-work"></a>Cómo funcionan las propiedades

Los valores de propiedad se almacenan en variables miembro.

Los pares de métodos hacen que las propiedades sean accesibles. Un método proporciona la implementación para especificar el valor de propiedad; su nombre comienza por put \_ . El otro método proporciona la implementación para recuperar el valor de propiedad; su nombre comienza por get \_ . La definición de interfaz está en Echo.idl. Los prototipos del método de propiedad están en Echo.h. Se implementan en Echo.cpp.

En las tres secciones siguientes se muestra cómo modificar los métodos de propiedad existentes para satisfacer sus necesidades y cómo agregar los métodos para una propiedad adicional.

-   [Variables para almacenar propiedades](variables-to-store-properties.md)
-   [Modificar la propiedad Scale](modifying-the-scale-property.md)
-   [Agregar la propiedad Mezcla mezclada](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Propiedades de ejemplo de eco**](echo-sample-properties.md)
</dt> </dl>

 

 




