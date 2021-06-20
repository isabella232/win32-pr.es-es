---
description: Obtenga información sobre las limitaciones impuestas por el esquema PrintCapabilities. El proveedor PrintCapabilities debe detectar configuraciones no válidas y resolverlas.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Schema-Imposed limitaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2911d4b90ebc194aa245f398f71575496c877
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404928"
---
# <a name="schema-imposed-limitations"></a>Schema-Imposed limitaciones

Este tema no es actual. Para obtener la información más reciente, vea [La especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema PrintCapabilities proporciona a los autores de PrintCapabilities una gran cantidad de flexibilidad y expresividad que se pueden usar en las descripciones de dispositivos. Sin embargo, las dependencias de configuración imponen una limitación a esta flexibilidad y expresividad. Las instancias de ParameterDef, la lista de elementos Feature, la lista de instancias option dentro de cada característica y las instancias scoredProperty dentro de cada opción no deben contener dependencias de configuración. El proveedor de documentos PrintCapabilities debe detectar combinaciones de configuraciones no válidas y debe resolverlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación del esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



