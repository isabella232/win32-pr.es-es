---
UID: NE:directml.DML_RANDOM_GENERATOR_TYPE
title: DML_RANDOM_GENERATOR_TYPE
description: Define constantes que especifican tipos de generador de números aleatorios.
helpviewer_keywords:
- DML_RANDOM_GENERATOR_TYPE
- DML_RANDOM_GENERATOR_TYPE structure
- direct3d12.dml_graph_node_type
- directml/DML_RANDOM_GENERATOR_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_RANDOM_GENERATOR_TYPE, DML_RANDOM_GENERATOR_TYPE structure, direct3d12.dml_graph_node_type, directml/DML_RANDOM_GENERATOR_TYPE
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_RANDOM_GENERATOR_TYPE
- directml/DML_RANDOM_GENERATOR_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_RANDOM_GENERATOR_TYPE
ms.openlocfilehash: c08b5cdc07280a2851636a555415ecce515fa79b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803757"
---
# <a name="dml_random_generator_type-enumeration-directmlh"></a>DML_RANDOM_GENERATOR_TYPE enumeración (directml.h)

Define constantes que especifican tipos de generador de números aleatorios.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
enum DML_RANDOM_GENERATOR_TYPE
{
  DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10
};
```

## <a name="constants"></a>Constantes

| Nombre | Descripción |
| ---- |:---- |
| DML_RANDOM_GENERATOR_TYPE_PHILOX_4X32_10 | Especifica un generador para números pseudo aleatorios según el algoritmo [de Filaox 4x32-10](http://www.thesalmons.org/john/random123/papers/random123sc11.pdf). |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |