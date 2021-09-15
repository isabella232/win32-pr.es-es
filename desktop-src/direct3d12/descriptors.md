---
title: Descriptores de
description: Los descriptores son la unidad principal de enlace para un único recurso en D3D12.
ms.assetid: f35b5776-46b0-4659-9e61-c6ebfdb55f87
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9576a2d40ade89c9c7a342feb6b069ca1321028e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359801"
---
# <a name="descriptors"></a>Descriptores de

Los descriptores son la unidad principal de enlace para un único recurso en D3D12.

## <a name="in-this-section"></a>En esta sección



| Tema                                                       | Descripción                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Información general sobre los descriptores](descriptors-overview.md)<br/> | Los descriptores se crean mediante llamadas API e identifican recursos.<br/>                                                                                                                                                                                                                                                                                                                   |
| [Creación de descriptores](creating-descriptors.md)<br/> | Describe y muestra ejemplos para crear vistas de índice, vértice y búfer constante. recurso de sombreador, destino de representación, acceso desordenado, salida de flujo y vistas de galería de símbolos de profundidad; y muestreadores. Todos los métodos para crear descriptores son subprocesos gratuitos.<br/>                                                                                                                             |
| [Descriptores de copias](copying-descriptors.md)<br/>   | Los [**métodos ID3D12Device::CopyDescriptors**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptors) e [**ID3D12Device::CopyDescriptorsSimple**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-copydescriptorssimple) de la interfaz de dispositivo usan la CPU para copiar inmediatamente los descriptores. Se pueden llamar subprocesos libres siempre y cuando varios subprocesos de la CPU o la GPU no realicen escrituras potencialmente conflictivas.<br/> |



 

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

 

 





