---
title: Documento como una instantánea de propiedades
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73fc190ed8c259e64fdd60cc291c6ae5b58f80
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "104424151"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>Documento de PrintCapabilities como una instantánea de propiedades

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El dispositivo descrito por la PrintCapabilities puede tener propiedades que dependen del estado o la configuración del dispositivo. Mientras que la PrintCapabilities representa el espacio de configuración completo de un dispositivo, el proveedor de PrintCapabilities genera una instancia dependiente de la configuración de la PrintCapabilities denominada documento de PrintCapabilities. Este documento de PrintCapabilities dependiente de la configuración evita sobrecargar el esquema de PrintCapabilities con la complejidad de representar datos de varios valores. Lo que es más importante, para liberar a un consumidor del documento de PrintCapabilities de la carga de extraer el valor adecuado de una representación de datos con varios valores, todas las instancias de Property y ScoredProperty de un documento de PrintCapabilities deben ser de un solo valor. En otras palabras, cada propiedad y la instancia de ScoredProperty de un documento de PrintCapabilities deben tener un valor fijo, con respecto a la configuración de entrada. Cada documento de PrintCapabilities se puede considerar como una instantánea de las propiedades del dispositivo cuando el dispositivo se encuentra en un estado determinado. Por consiguiente, antes de que se pueda construir un documento de PrintCapabilities, se debe proporcionar la configuración que se va a usar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



