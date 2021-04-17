---
description: Este tema no está actualizado. Para obtener la información más reciente, consulte la especificación del esquema de impresión.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Limitaciones de Schema-Imposed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dc283704ea96e3303de6755a217e454b506bdc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105698028"
---
# <a name="schema-imposed-limitations"></a>Limitaciones de Schema-Imposed

Este tema no está actualizado. Para obtener la información más reciente, consulte la [especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema de PrintCapabilities proporciona a los autores de PrintCapabilities una cantidad considerable de flexibilidad y expresividad que se puede usar en las descripciones de los dispositivos. Sin embargo, las dependencias de configuración imponen una limitación en esta flexibilidad y expresividad. Las instancias de ParameterDef, la lista de elementos de característica, la lista de instancias de opción dentro de cada característica y las instancias de ScoredProperty dentro de cada opción no deben contener dependencias de configuración. El proveedor de documentos de PrintCapabilities debe detectar combinaciones no válidas de configuraciones y debe resolverlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



