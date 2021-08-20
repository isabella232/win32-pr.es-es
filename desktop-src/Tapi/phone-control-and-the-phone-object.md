---
description: TAPI 3.1 presenta controles de teléfono basados en COM. Se supone que está familiarizado con COM, OLE Automation y scripting, al igual que el conocimiento del modelo de objetos TAPI 3. El conocimiento de las funciones de control telefónico tapi 2 también es útil.
ms.assetid: e56aef54-e358-429b-9f0f-c8776507d95f
title: Teléfono Control y el objeto Teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc00131b37b46a9a275b3463f1eac19e057818c4311a1be54cc45a331983134
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117944484"
---
# <a name="phone-control-and-the-phone-object"></a>Teléfono Control y el objeto Teléfono

TAPI 3.1 presenta controles de teléfono basados en COM. Se supone que está familiarizado con COM, OLE Automation y scripting, al igual que el conocimiento del modelo de objetos TAPI 3. El conocimiento de las funciones de control telefónico tapi 2 también es útil.

Teléfono control se implementa en tres niveles de características, cada una de las cuales se basa en la anterior:

-   Teléfono objeto . El primer nivel define cómo se exponen los dispositivos de teléfono de TAPI 2.x (API, constantes y mensajes que comienzan por "teléfono") en el modelo de objetos TAPI 3.1. Esto implica un nuevo objeto de teléfono expuesto desde TAPI 3.1, con [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) como interfaz predeterminada en el nuevo objeto. La interfaz de **ITPhone,** junto con sus constantes, tipos enumerados y eventos asociados, suele exponer el mismo nivel de detalle y funcionalidad que las funciones, constantes, estructuras y mensajes de TAPI 2.x que comienzan por la palabra "phone". Este nivel también implica nuevas interfaces en varios objetos TAPI 3.x existentes para facilitar la creación de objetos de teléfono y la asociación de objetos de teléfono con otros objetos con los que están relacionados.
-   Control telefónico automatizado y control de llamadas. El segundo nivel consta de una interfaz adicional denominada [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) y sus constantes, tipos enumerados y eventos asociados. Se trata de una interfaz secundaria en el objeto de teléfono. Si el dispositivo telefónico se abrió con privilegios de propietario, use el método **QueryInterface** en la interfaz [**de ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) para obtener un puntero de interfaz **ITAutomatedPhoneControl.**
-   Windows 2000 Teléfono Dialer. El tercer nivel consta de cambios en la Windows 2000 Teléfono Dialer para implementar interacciones de usuario específicas.

Microsoft o desarrolladores de terceros pueden usar el modelo de objetos TAPI 3.1 para implementar aplicaciones o servicios más avanzados que impliquen teléfonos, incluido un servicio que permite que los teléfonos de bus serie universal (USB), por ejemplo, se usen para llamadas telefónicas incluso si ningún usuario ha iniciado sesión y no se ha iniciado explícitamente ninguna otra aplicación TAPI.

En TAPI 3.0, un msp Teléfono intentó mejorar los dispositivos telefónicos asociados a las líneas usadas para las llamadas TAPI 3.0. Este desarrollo está pensado para admitir módems con altavoz conmutables por software. Las aplicaciones TAPI 3.1 que usan este tipo de módem deben usar los objetos de teléfono TAPI 3.1 para manipular el estado del conmutador de enlace del módem.

Para obtener más información y una lista de todas las interfaces asociadas al objeto Teléfono, vea [Teléfono Interfaces de objeto](phone-object-interfaces.md). Las interfaces de control telefónico exponen métodos que permiten el control sobre los conjuntos de teléfonos mediante COM.

 

 



