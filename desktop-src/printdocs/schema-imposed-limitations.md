---
description: Obtenga información sobre las limitaciones impuestas por el esquema PrintCapabilities. El proveedor PrintCapabilities debe detectar configuraciones no válidas y resolverlas.
ms.assetid: 420c5c84-abb8-495a-9b74-dc19a16034fb
title: Schema-Imposed limitaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85470d8f2e86b357e28633a4cf1df8f4eff00079d0e7303d380dd4a3084591fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119947385"
---
# <a name="schema-imposed-limitations"></a>Schema-Imposed limitaciones

Este tema no es actual. Para obtener la información más reciente, vea [La especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).

El esquema PrintCapabilities proporciona a los autores de PrintCapabilities una gran cantidad de flexibilidad y expresividad que se pueden usar en las descripciones del dispositivo. Sin embargo, las dependencias de configuración imponen una limitación en esta flexibilidad y expresividad. Las instancias de ParameterDef, la lista de elementos Feature, la lista de instancias option dentro de cada característica y las instancias ScoredProperty dentro de cada opción no deben contener dependencias de configuración. El proveedor de documentos PrintCapabilities debe detectar combinaciones de configuraciones no válidas y debe resolverlas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Especificación de esquema de impresión](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



