---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Marco de esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 617f747b950676f2359645684c9e672fb5c87ee3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104279848"
---
# <a name="print-schema-framework"></a>Marco de esquema de impresión

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En esta sección se proporciona información más detallada sobre el significado y el uso de los tipos de elemento de esquema de impresión. El enfoque principal de la versión inicial del marco de trabajo del esquema de impresión es representar las configuraciones y las capacidades de los atributos del dispositivo. En un nivel alto, este marco de trabajo ofrece dos estilos diferentes para describir un atributo de dispositivo: como una construcción de característica/opción o como una construcción de parámetro. Si un atributo de dispositivo tiene un pequeño número de valores o Estados disponibles, el atributo debe caracterizarse como una característica con los valores permitidos o los Estados a los que se hace referencia como elementos de opción. Por el contrario, si un atributo de dispositivo tiene un gran número de valores o Estados disponibles y el conjunto de todos los valores posibles se define fácilmente sin recurrir a la enumeración explícita, el atributo de dispositivo se debe caracterizar como un parámetro. (Un parámetro se define por medio de un elemento ParameterDef, y una instancia de parámetro se inicializa mediante un elemento ParameterInit). Los elementos de propiedad se utilizan en las construcciones de características, opciones y parámetros para proporcionar un nivel de diferenciación más preciso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



