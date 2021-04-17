---
description: TAPI 3,1 presenta controles telefónicos basados en COM. Se supone que está familiarizado con COM, la automatización OLE y el scripting, así como el conocimiento del modelo de objetos de TAPI 3. También es útil conocer las funciones de control de teléfono TAPI 2.
ms.assetid: e56aef54-e358-429b-9f0f-c8776507d95f
title: Control telefónico y el objeto teléfono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e9344d54a63efcf1692af361a5f8e88121981e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687360"
---
# <a name="phone-control-and-the-phone-object"></a>Control telefónico y el objeto teléfono

TAPI 3,1 presenta controles telefónicos basados en COM. Se supone que está familiarizado con COM, la automatización OLE y el scripting, así como el conocimiento del modelo de objetos de TAPI 3. También es útil conocer las funciones de control de teléfono TAPI 2.

El control de teléfono se implementa en tres niveles de características, cada uno de los cuales se basa en el anterior:

-   Objeto de teléfono. En el primer nivel se define cómo se exponen los dispositivos telefónicos de TAPI 2. x (API, constantes y mensajes que empiezan por "Phone") en el modelo de objetos de TAPI 3,1. Esto implica un nuevo objeto de teléfono expuesto desde TAPI 3,1, con [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) como la interfaz predeterminada en el nuevo objeto. La interfaz **ITPhone** , junto con sus constantes asociadas, los tipos enumerados y los eventos, generalmente expone el mismo nivel de detalle y funcionalidad que las funciones, constantes, estructuras y mensajes TAPI 2. x que comienzan con la palabra "Phone". Este nivel también implica nuevas interfaces en varios objetos TAPI 3. x existentes para facilitar la creación de objetos de teléfono y la Asociación de objetos de teléfono con otros objetos con los que están relacionados.
-   Control automático del teléfono y control de llamadas. El segundo nivel consta de una interfaz adicional denominada [**ITAutomatedPhoneControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol) y sus constantes, tipos enumerados y eventos asociados. Se trata de una interfaz secundaria en el objeto de teléfono. Si el dispositivo telefónico se abrió con privilegios de propietario, use el método **QueryInterface** en la interfaz [**ITPhone**](/windows/desktop/api/tapi3if/nn-tapi3if-itphone) para obtener un puntero de la interfaz **ITAutomatedPhoneControl** .
-   Windows 2000 Phone Dialer. El tercer nivel consta de cambios en la aplicación de marcado telefónico de Windows 2000 para implementar interacciones de usuario específicas.

Los programadores de Microsoft o de terceros pueden usar el modelo de objetos de TAPI 3,1 para implementar aplicaciones o servicios más avanzados que impliquen teléfonos, incluido un servicio que permita el uso de microteléfonos de bus serie universal (USB), por ejemplo, para las llamadas telefónicas, incluso si ningún usuario ha iniciado sesión y no se ha iniciado explícitamente ninguna otra aplicación TAPI.

En TAPI 3,0, un teléfono MSP intentó mejorar los dispositivos telefónicos asociados a las líneas utilizadas para las llamadas a TAPI 3,0. Este desarrollo se ha diseñado para admitir módems con altavozs mutables por software. Las aplicaciones TAPI 3,1 que usan este tipo de módem deben usar los objetos de teléfono de TAPI 3,1 para manipular el estado conmutador del módem.

Para obtener más información y una lista de todas las interfaces asociadas al objeto de teléfono, consulte [interfaces de objetos de teléfono](phone-object-interfaces.md). Las interfaces de control de teléfono exponen métodos que permiten controlar los conjuntos de teléfonos mediante COM.

 

 



