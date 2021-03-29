---
title: Cómo funcionan las propiedades
description: Cómo funcionan las propiedades
ms.assetid: 469af852-593c-4b54-8dc3-b76ad460fa77
keywords:
- Complementos de Media Player de Windows, propiedades de ejemplo de eco
- complementos, propiedades de ejemplo de eco
- Complementos de procesamiento de señal digital, eco de propiedades de ejemplo
- Complementos DSP, propiedades de ejemplo de eco
- Ejemplo de complemento DSP de eco, propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad37b71ddc6a097dd43e1ac41147c571f81a67a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777100"
---
# <a name="how-properties-work"></a>Cómo funcionan las propiedades

Los valores de propiedad se almacenan en variables de miembro.

Las propiedades se hacen accesibles mediante pares de métodos. Un método proporciona la implementación para especificar el valor de la propiedad; su nombre comienza por Put \_ . El otro método proporciona la implementación para recuperar el valor de la propiedad; su nombre comienza con get \_ . La definición de la interfaz está en echo. idl. Los prototipos de método de propiedad están en echo. h. Se implementan en echo. cpp.

En las tres secciones siguientes se muestra cómo modificar los métodos de propiedad existentes para adaptarlos a sus necesidades y cómo agregar los métodos para una propiedad adicional.

-   [Variables para almacenar propiedades](variables-to-store-properties.md)
-   [Modificar la propiedad Scale](modifying-the-scale-property.md)
-   [Agregar la propiedad de combinación húmeda](adding-the-wet-mix-property.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Eco de propiedades de ejemplo**](echo-sample-properties.md)
</dt> </dl>

 

 




