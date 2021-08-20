---
title: Funciones auxiliares para Direct3D 12
description: Estas funciones auxiliares ayudan especialmente a controlar los subrecursos y se declaran en `d3dx12.h` .
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funciones auxiliares
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9434bf916d7cb92116cdf4f7f6d86363b2eb51
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813187"
---
# <a name="helper-functions-for-direct3d-12"></a>Funciones auxiliares para Direct3D 12

Estas funciones auxiliares ayudan especialmente a controlar los subrecursos y se declaran en `d3dx12.h` .

`d3dx12.h` está disponible por separado de los encabezados de Direct3D 12. Puede descargar desde `d3dx12.h` [la biblioteca auxiliar D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**CommandListCast**](commandlistcast.md) | Esta plantilla de función convierte un puntero constante a cualquier lista de comandos en un puntero const a id3D12CommandList. |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md) | Calcula un índice de subrecurso para una textura. |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md) | Genera el segmento mip, el segmento de matriz y el segmento de plano que corresponden al índice de subrecurso especificado. |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) | Obtiene el número de planos para el formato DXGI especificado para el adaptador virtual especificado **(un ID3D12Device**). |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md) | Indica si el diseño es opaco. |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md) | Devuelve el tipo de subobjeto que corresponde a la clase base del tipo de subobjeto pasado. |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md) | Analiza una descripción de flujo de estado de canalización, llamando a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada. |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md) | Ayuda a habilitar las características de firma raíz 1.1 cuando están disponibles y no requiere mantener dos rutas de acceso de código para crear firmas raíz. Este método auxiliar reconstruye una firma raíz de la versión 1.0 cuando no se admite la versión 1.1. |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md) | Devuelve el tamaño necesario de un búfer que se usará para la carga de datos. |
| [**Memcpysubresource**](memcpysubresource.md) | Copia una fila de subrecurso por fila. |
| [**Updatesubresources**](updatesubresources1.md) | Actualiza los subrecursos, se deben rellenar todas las matrices de subrecursos, normalmente llamando a [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). |
| [**Updatesubresources (asignación de montones)**](updatesubresources2.md) | Actualiza los subrecursos con una implementación de asignación de montón. |
| [**Updatesubresources (asignación de pila)**](updatesubresources3.md) | Actualiza los subrecursos con una implementación de asignación de pila. |

## <a name="related-topics"></a>Temas relacionados

* [Referencia de Direct3D 12](direct3d-12-reference.md)
* [Estructuras y funciones auxiliares de D3D12](helper-structures-and-functions-for-d3d12.md)
