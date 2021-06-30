---
title: Funciones auxiliares de D3D12
description: Estas funciones auxiliares ayudan especialmente a controlar los subrecursos y se declaran en d3dx12.h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Funciones auxiliares
- d3dx12.h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10736d91da0e2c4efa2a3c981ab5c4f64e2af86d
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102143"
---
# <a name="helper-functions-for-d3d12"></a>Funciones auxiliares de D3D12

Estas funciones auxiliares ayudan especialmente a controlar los subrecursos y se declaran en **d3dx12.h**.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                             | Descripción                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommandListCast**](commandlistcast.md)<br/>                                     | Esta plantilla de función convierte un puntero constante a cualquier lista de comandos en un puntero const a id3D12CommandList.<br/>                                                                                                                               |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md)<br/>                                   | Calcula un índice de subrecurso para una textura. <br/>                                                                                                                                                                                                  |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md)<br/>                         | Genera el segmento mip, el segmento de matriz y el segmento de plano que corresponden al índice de subrecurso especificado. <br/>                                                                                                                                        |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md)<br/>                           | Obtiene el número de planos para el formato DXGI especificado para el adaptador virtual especificado **(id. 3D12Device).** <br/>                                                                                                                               |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md)<br/>                                     | Indica si el diseño es opaco.<br/>                                                                                                                                                                                                         |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md)<br/>                       | Devuelve el tipo de subobjeto que corresponde a la clase base del tipo de subobjeto pasado.<br/>                                                                                                                                                  |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md)<br/>                    | Analiza una descripción de flujo de estado de canalización, llamando a una devolución de llamada definida por el usuario para cada instancia de subobjeto analizada.<br/>                                                                                                                                 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md)<br/> | Ayuda a habilitar las características de firma raíz 1.1 cuando están disponibles y no requiere mantener dos rutas de acceso de código para crear firmas raíz. Este método auxiliar reconstruye una firma raíz de la versión 1.0 cuando no se admite la versión 1.1.<br/> |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md)<br/>                     | Devuelve el tamaño necesario de un búfer que se va a usar para la carga de datos. <br/>                                                                                                                                                                              |
| [**Memcpysubresource**](memcpysubresource.md)<br/>                                         | Copia una fila de subrecurso por fila. <br/>                                                                                                                                                                                                               |
| [**Updatesubresources**](updatesubresources1.md)<br/>                                      | Actualiza los subrecursos, todas las matrices de subrecursos deben rellenarse, normalmente llamando a [**ID3D12Device::GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). <br/>                                                                  |
| [**Updatesubresources (asignación de montones)**](updatesubresources2.md)<br/>                    | Actualiza los subrecursos con una implementación de asignación de montón. <br/>                                                                                                                                                                                    |
| [**Updatesubresources (asignación de pila)**](updatesubresources3.md)<br/>                   | Actualiza los subrecursos con una implementación de asignación de pila. <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Estructuras y funciones auxiliares de D3D12](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





