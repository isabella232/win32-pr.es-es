---
title: Documento como instantánea de propiedades
description: Revise el documento PrintCapabilities como una instantánea de las propiedades. Este tema no es actual. Para obtener la información más reciente, vea La especificación del esquema de impresión.
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118650"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a>Documento PrintCapabilities como instantánea de propiedades

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El dispositivo descrito por PrintCapabilities puede tener propiedades que dependen del estado o la configuración del dispositivo. Aunque PrintCapabilities representa el espacio de configuración completo de un dispositivo, el proveedor PrintCapabilities genera una instancia dependiente de la configuración de PrintCapabilities denominada documento PrintCapabilities. Este documento PrintCapabilities dependiente de la configuración evita cargar el esquema PrintCapabilities con la complejidad de representar datos de varios valores. Lo que es más importante, para liberar a un consumidor del documento PrintCapabilities de la carga de extraer el valor adecuado de una representación de datos de varios valores, todas las instancias property y ScoredProperty de un documento PrintCapabilities deben tener un solo valor. En otras palabras, cada instancia de Property y ScoredProperty de un documento PrintCapabilities debe tener un valor fijo, relativo a la configuración de entrada. Cada documento PrintCapabilities se puede pensar en como una instantánea de las propiedades del dispositivo cuando el dispositivo está en un estado determinado. Por lo tanto, antes de que se pueda construir un documento PrintCapabilities, se debe proporcionar la configuración que se va a usar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



