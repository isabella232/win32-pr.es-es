---
description: LOCALE \_ SPARENT
ms.assetid: 3fa0bc36-7577-4b5a-b557-8ac42e8594a8
title: LOCALE_SPARENT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35a774c6a7f8eea631a2d6579b97058b30acdfe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127274287"
---
# <a name="locale_sparent"></a>LOCALE \_ SPARENT

**Windows Vista y versiones posteriores:** Configuración regional de reserva, que usa el cargador de recursos. El número máximo de caracteres permitido para esta cadena es 85, incluido un carácter nulo de terminación.

Las configuraciones regionales tienen una jerarquía en la que el elemento primario de una configuración regional específica es una configuración regional neutra. Una configuración regional específica está asociada a un idioma y a un país o región, mientras que una configuración regional neutra está asociada a un idioma, pero no a ningún país o región. La configuración regional primaria se usa para decidir la primera reserva que se va a intentar cuando un recurso para una configuración regional específica no está disponible. Por ejemplo, la configuración regional primaria para "en-US" (0x0409) es "en" (0x0009). Cuando un recurso no está disponible para la configuración regional "en-US" específica, el cargador de recursos vuelve a usar el recurso que está disponible para la configuración regional "en" neutra. Consulte [Interfaz de usuario Language Management para](user-interface-language-management.md) más información sobre la estrategia de reserva del cargador de recursos.

Este patrón es coherente para las configuraciones regionales predefinidas. Sin embargo, la configuración regional primaria no está determinada por ninguna manipulación del nombre de la configuración regional. Es decir, [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) y [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) no analizan una cadena como "en-US" para obtener el valor "en". En su lugar, observan los datos de configuración regional almacenados. Para las configuraciones regionales predefinidas, el valor sigue el patrón esperado, en el que el elemento primario de una configuración regional específica es la configuración regional neutra correspondiente y el elemento primario de una configuración regional neutra es la configuración regional invariable. Aunque se recomienda que las configuraciones regionales personalizadas sigan una estrategia similar en cuanto a la definición de su configuración regional primaria, esto no se aplica. La aplicación que implementa una configuración regional personalizada puede especificar un elemento primario menos obviamente adecuado.

> [!Note]  
> Puesto que ninguna de las funciones descritas en Llamar a las funciones ["Nombre](calling-the--locale-name--functions.md) de configuración regional" acepta configuraciones regionales neutras como entradas, estos datos SPARENT de LOCALE tienen \_ un uso muy limitado. En concreto, ni [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ni [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) aceptan configuraciones regionales neutras como entradas.

 

 

 



