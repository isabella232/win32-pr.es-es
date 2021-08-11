---
description: Obtenga información sobre los usos de PrintCapabilities. Este tema no está al día. Para obtener la información más reciente, vea Especificación de esquema de impresión.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usos de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96aec2d21a2751305ae1f2e191a37adb584a0209542a78a0bf53253ea66faa20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233533"
---
# <a name="uses-of-the-printcapabilities"></a>Usos de PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

PrintCapabilities está diseñado para representar atributos de dispositivo configurables como construcciones de característica/opción o construcciones de parámetros. Esta información define el espacio de configuración del dispositivo y lo puede usar un cliente de interfaz de usuario (UI) para construir una interfaz de usuario. Las palabras clave de esquema de impresión definen un conjunto de instancias de características estándar, instancias de opción para las instancias de características estándar e instancias parameterdef.

Las construcciones de característica,opción o parámetro de PrintCapabilities están diseñadas para contener instancias de Property o ScoredProperty que describen un dispositivo y que son compatibles con el subsistema spooler. Estas instancias property y ScoredProperty son de interés general para los clientes del dispositivo y contienen la información proporcionada por las funciones DevCaps de Win32. Las palabras clave de esquema de impresión definen un conjunto de instancias de Property y ScoredProperty estándar.

Debe destacarse que el documento PrintCapabilities está pensado para representar solo datos de un solo valor: datos que no dependen de una configuración determinada del dispositivo. El documento PrintCapabilities proporciona solo una instantánea de los datos dependientes de la configuración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



