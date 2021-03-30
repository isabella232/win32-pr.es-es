---
title: Interfaz ID3DX11EffectUnorderedAccessViewVariable (D3dx11effect. h)
description: Obtiene acceso a una vista de acceso desordenado.
ms.assetid: f78dc8c5-c85a-48cf-b579-f2937aa5ce2a
keywords:
- Interfaz ID3DX11EffectUnorderedAccessViewVariable Direct3D 11
- Interfaz ID3DX11EffectUnorderedAccessViewVariable Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectUnorderedAccessViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d48161ad4d9fc1773889fab0e8a0fd9a21ec793e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998317"
---
# <a name="id3dx11effectunorderedaccessviewvariable-interface"></a>Interfaz ID3DX11EffectUnorderedAccessViewVariable

Obtiene acceso a una vista de acceso desordenado.

## <a name="members"></a>Miembros

La interfaz **ID3DX11EffectUnorderedAccessViewVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectUnorderedAccessViewVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11EffectUnorderedAccessViewVariable** tiene estos métodos.



| Método                                                                                                      | Descripción                                        |
|:------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| [**GetUnorderedAccessView**](id3dx11effectunorderedaccessviewvariable-getunorderedaccessview.md)           | Obtiene una vista de acceso sin ordenar.<br/>           |
| [**GetUnorderedAccessViewArray**](id3dx11effectunorderedaccessviewvariable-getunorderedaccessviewarray.md) | Obtiene una matriz de vistas de acceso desordenados.<br/> |
| [**SetUnorderedAccessView**](id3dx11effectunorderedaccessviewvariable-setunorderedaccessview.md)           | Establecer una vista de acceso sin ordenar.<br/>           |
| [**SetUnorderedAccessViewArray**](id3dx11effectunorderedaccessviewvariable-setunorderedaccessviewarray.md) | Establezca una matriz de vistas de acceso desordenados.<br/> |



 

## <a name="remarks"></a>Observaciones

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen de Effects 11 para compilar la aplicación de tipo Effects. Para obtener más información sobre el uso de los efectos 11 de origen, vea [diferencias entre los efectos 10 y 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca de Effects 11 está disponible en línea como código fuente compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





