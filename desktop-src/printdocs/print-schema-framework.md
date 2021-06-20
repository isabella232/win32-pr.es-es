---
description: En estos artículos se proporciona información más detallada sobre el significado y el uso de los tipos de elementos Print Schema.
ms.assetid: 05c7fd07-1c32-409d-8ca5-820038af3440
title: Marco de esquema de impresión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570701df700954ad85fb724b9528b7e7912f3174
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407168"
---
# <a name="print-schema-framework"></a>Marco de esquema de impresión

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

En esta sección se proporciona información más detallada sobre el significado y el uso de los tipos de elemento Print Schema. El enfoque principal de la versión inicial de Print Schema Framework es representar las configuraciones y las funcionalidades de los atributos del dispositivo. En un nivel alto, este marco ofrece dos estilos diferentes para describir un atributo de dispositivo: como una construcción feature/option o como una construcción de parámetros. Si un atributo de dispositivo tiene un número pequeño de valores o estados disponibles, el atributo debe caracterizarse como una característica con los valores o estados permitidos denominados elementos Option. Por el contrario, si un atributo de dispositivo tiene un gran número de valores o estados disponibles y el conjunto de todos los valores posibles se define fácilmente sin recurrir a la enumeración explícita, el atributo de dispositivo debe caracterizarse como un parámetro. (Un parámetro se define mediante un elemento ParameterDef y una instancia de parámetro se inicializa mediante un elemento ParameterInit). Los elementos property se usan en las construcciones feature/option y de parámetros para proporcionar un nivel más fino de diferenciación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



