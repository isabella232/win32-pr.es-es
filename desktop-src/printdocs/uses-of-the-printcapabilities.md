---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usos de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63dda5b21d1472ec8d4162c8d7229ff47264fb55
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104003467"
---
# <a name="uses-of-the-printcapabilities"></a>Usos de PrintCapabilities

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

La PrintCapabilities está pensada para representar atributos de dispositivo configurables como construcciones de características o de opciones o construcciones de parámetros. Esta información define el espacio de configuración del dispositivo y puede ser utilizado por un cliente de la interfaz de usuario (UI) para construir una interfaz de usuario. Las palabras clave del esquema de impresión definen un conjunto de instancias de características estándar, instancias de opciones para las instancias de características estándar e instancias de ParameterDef.

Las construcciones de características, opciones o parámetros de PrintCapabilities están pensadas para contener instancias de propiedad o ScoredProperty que describen un dispositivo y que son compatibles con el subsistema de cola de impresión. Estas instancias de propiedad y ScoredProperty son de interés general para los clientes del dispositivo y contienen la información proporcionada por las funciones DevCaps de Win32. Las palabras clave de esquema de impresión definen un conjunto de instancias de ScoredProperty y de propiedades estándar.

Se debe resaltar que el documento de PrintCapabilities está diseñado para representar solo datos de valor único: datos que no dependen de una configuración determinada del dispositivo. El documento de PrintCapabilities solo proporciona una instantánea de los datos dependientes de la configuración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



