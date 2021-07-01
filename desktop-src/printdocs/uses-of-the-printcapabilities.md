---
description: Obtenga información sobre los usos de PrintCapabilities. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: ea75a7ac-d4d7-42b6-91e9-e28607fd684c
title: Usos de PrintCapabilities
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f09882d42814930ef5ba08e087f1df87e0d0e9bc
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119430"
---
# <a name="uses-of-the-printcapabilities"></a>Usos de PrintCapabilities

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

PrintCapabilities está diseñado para representar atributos de dispositivo configurables como construcciones de características o opciones o construcciones de parámetros. Esta información define el espacio de configuración del dispositivo y lo puede usar un cliente de interfaz de usuario (UI) para construir una interfaz de usuario. Las palabras clave de esquema de impresión definen un conjunto de instancias de características estándar, instancias de opción para las instancias de feature estándar e instancias parameterdef.

Las construcciones de característica/opción o parámetro de PrintCapabilities están diseñadas para contener instancias de Property o ScoredProperty que describen un dispositivo y que son compatibles con el subsistema de cola. Estas instancias de Property y ScoredProperty son de interés general para los clientes del dispositivo y contienen la información proporcionada por las funciones DevCaps de Win32. Las palabras clave de esquema de impresión definen un conjunto de instancias de Property y ScoredProperty estándar.

Debe destacarse que el documento PrintCapabilities está pensado para representar solo datos de un solo valor: datos que no dependen de una configuración determinada del dispositivo. El documento PrintCapabilities proporciona solo una instantánea de los datos dependientes de la configuración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



