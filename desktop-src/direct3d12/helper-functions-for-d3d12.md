---
title: Funciones auxiliares de D3D12
description: Estas funciones auxiliares ayudan especialmente en el control de Subrecursos y se declaran en d3dx12. h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funciones auxiliares
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704697"
---
# <a name="helper-functions-for-d3d12"></a>Funciones auxiliares de D3D12

Estas funciones auxiliares ayudan especialmente en el control de Subrecursos y se declaran en **d3dx12. h**.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommandListCast**](cd3dx12-shader-bytecode.md)<br/>                                     | Esta plantilla de función convierte un puntero constante en cualquier lista de comandos en un puntero const a un ID3D12CommandList.<br/>                                                                                                                               |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md)<br/>                                   | Calcula un índice de subrecurso para una textura. <br/>                                                                                                                                                                                                  |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md)<br/>                         | Genera el segmento MIP, el segmento de matriz y el segmento de plano que se corresponden con el índice del subrecurso especificado. <br/>                                                                                                                                        |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md)<br/>                           | Obtiene el número de planos para el formato de DXGI especificado para el adaptador virtual especificado (un **ID3D12Device**). <br/>                                                                                                                               |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md)<br/>                                     | Indica si el diseño es opaco.<br/>                                                                                                                                                                                                         |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md)<br/>                       | Devuelve el tipo de subobjeto que corresponde a la clase base del tipo de subobjeto pasado.<br/>                                                                                                                                                  |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md)<br/>                    | Analiza una descripción de flujo de estado de canalización, que llama a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.<br/>                                                                                                                                 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md)<br/> | Ayuda a habilitar las características de la firma raíz 1,1 cuando están disponibles y no requiere mantener dos rutas de acceso de código para generar firmas raíz. Este método auxiliar reconstruye una firma raíz de la versión 1,0 cuando no se admite la versión 1,1.<br/> |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md)<br/>                     | Devuelve el tamaño necesario de un búfer que se va a utilizar para la carga de datos. <br/>                                                                                                                                                                              |
| [**Memcpysubresource**](memcpysubresource.md)<br/>                                         | Copia un subrecurso fila por fila. <br/>                                                                                                                                                                                                               |
| [**Updatesubresources**](updatesubresources1.md)<br/>                                      | Actualiza los Subrecursos, se deben rellenar todas las matrices de Subrecursos, normalmente mediante una llamada a [**ID3D12Device:: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). <br/>                                                                  |
| [**Updatesubresources (asignación de montones)**](updatesubresources2.md)<br/>                    | Actualiza Subrecursos con una implementación de asignación de montón. <br/>                                                                                                                                                                                    |
| [**Updatesubresources (asignación de pila)**](updatesubresources3.md)<br/>                   | Actualiza Subrecursos con una implementación de asignación de pila. <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Estructuras y funciones auxiliares de D3D12](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





