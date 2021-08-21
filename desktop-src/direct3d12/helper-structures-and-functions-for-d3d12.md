---
title: Estructuras y funciones auxiliares para Direct3D 12
description: Estas estructuras auxiliares y funciones auxiliares se declaran en `d3dx12.h` .
ms.assetid: 095958A9-345B-45AE-8363-B353534044B2
keywords:
- Funciones auxiliares
- Estructuras auxiliares
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b42bc9ae73f3537cc786a465feba596b3392401
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812178"
---
# <a name="helper-structures-and-functions-for-direct3d-12"></a>Estructuras y funciones auxiliares para Direct3D 12

Estas estructuras auxiliares y funciones auxiliares se declaran en `d3dx12.h` .

`d3dx12.h` está disponible por separado de los encabezados de Direct3D 12. Puede descargar desde `d3dx12.h` [la biblioteca auxiliar D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

Puede usar estas estructuras auxiliares para crear e inicializar estructuras de Direct3D. Estas estructuras auxiliares se comportan como clases de C++. Cada estructura auxiliar normalmente tiene un constructor predeterminado, un constructor explícito, un destructor y un operador de conversión para la estructura D3D12 asociada. Cada estructura auxiliar tiene un prefijo "C" y está asociada a una estructura D3D12 que carece del prefijo "C". La mayoría de las estructuras auxiliares contienen métodos de miembro de inicialización, algunos contienen funciones de comparación.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Interfaces auxiliares para D3D12](helper-interfaces-for-d3d12.md) | Estas interfaces auxiliares ayudan especialmente a controlar los subrecursos y se declaran en `d3dx12.h` .  |
| [Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md) | Estas estructuras auxiliares ayudan a inicializar muchas de las estructuras de Direct3D 12 y se declaran en `d3dx12.h` . |
| [Funciones auxiliares de D3D12](helper-functions-for-d3d12.md) | Estas funciones auxiliares ayudan especialmente a controlar los subrecursos y se declaran en `d3dx12.h` .  |

## <a name="related-topics"></a>Temas relacionados

* [Referencia de Direct3D 12](direct3d-12-reference.md)
