---
title: Interfaz ID3DX11EffectSamplerVariable (D3dx11effect.h)
description: Una interfaz de sampler accede al estado del sampler.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Interfaz ID3DX11EffectSamplerVariable direct3D 11
- Interfaz ID3DX11EffectSamplerVariable Direct3D 11 , descrita
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0865df924fb3a01e3c10ae015f13b4ec6e06e900dad32ff966d9bdbfed0c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952825"
---
# <a name="id3dx11effectsamplervariable-interface"></a>Interfaz ID3DX11EffectSamplerVariable

Una interfaz de sampler accede al estado del sampler.

## <a name="members"></a>Miembros

La **interfaz ID3DX11EffectSamplerVariable** hereda de [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectSamplerVariable** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ID3DX11EffectSamplerVariable** tiene estos métodos.



| Método                                                                  | Descripción                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetBackingStore**](id3dx11effectsamplervariable-getbackingstore.md) | Obtiene un puntero a una variable que contiene el estado del muestreador.<br/> |
| [**GetSampler**](id3dx11effectsamplervariable-getsampler.md)           | Obtenga un puntero a una interfaz sampler.<br/>                    |
| [**SetSampler**](id3dx11effectsamplervariable-setsampler.md)           | Establezca el estado del sampler.<br/>                                       |
| [**UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)   | Revierta un estado de sampler establecido previamente.<br/>                   |



 

## <a name="remarks"></a>Comentarios

Se [**crea una interfaz ID3DX11EffectVariable**](id3dx11effectvariable.md) cuando se lee un efecto en la memoria.

Las variables de efecto se guardan en memoria en el almacén de respaldo; cuando se aplica una técnica, los valores de la tienda de respaldo se copian en el dispositivo. Puede usar cualquiera de estos métodos para devolver el estado.

> [!Note]  
> El SDK de DirectX no proporciona archivos binarios compilados para efectos. Debe usar el origen De efectos 11 para compilar la aplicación de tipo de efectos. Para obtener más información sobre el uso del origen de Efectos 11, vea Diferencias entre los efectos [10 y los efectos 11.](d3d11-graphics-programming-guide-effects-differences.md)

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx11effect.h</dt> </dl>                                                    |
| Biblioteca<br/> | <dl> <dt>N/A (una biblioteca effects 11 está disponible en línea como origen compartido).</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Efectos 11 interfaces](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[D3DX Interfaces](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





