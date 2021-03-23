---
title: Descriptores de
description: Los descriptores son la unidad principal de enlace para un único recurso de D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104093"
---
# <a name="descriptors"></a>Descriptores de

Los descriptores son la unidad principal de enlace para un único recurso de D3D12.

## <a name="in-this-section"></a>En esta sección



| Tema                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre descriptores](descriptors-overview.md)<br/> | Los descriptores se crean mediante llamadas API e identifican recursos.<br/>                                                                                                                                                                                                                                                                                                                   |
| [Crear descriptores](creating-descriptors.md)<br/> | Describe y muestra ejemplos para crear vistas de búfer de índice, vértices y constantes; recursos del sombreador, destino de representación, acceso desordenado, salida de secuencia y vistas de la galería de símbolos de profundidad; y muestreadores. Todos los métodos para crear descriptores son de subprocesamiento libre.<br/>                                                                                                                             |
| [Descriptores de copias](copying-descriptors.md)<br/>   | Los métodos [**ID3D12Device:: CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) y [**ID3D12Device:: CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) de la interfaz de dispositivo usan la CPU para copiar descriptores inmediatamente. Se puede llamar subprocesamiento libre siempre que varios subprocesos de la CPU o GPU no realicen ninguna escritura en conflicto.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> <dt>

[Tablas de descriptores](descriptor-tables.md)
</dt> <dt>

[Enlace de recursos](resource-binding.md)
</dt> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 





