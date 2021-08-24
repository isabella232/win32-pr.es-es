---
description: Finaliza una técnica activa.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: Método ID3DXEffect::End (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.End
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6c93dc98febe2f5e539d3be678322860fe14069c2f8bf6b75cc42864b922e1f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748665"
---
# <a name="id3dxeffectend-method"></a>Método ID3DXEffect::End

Finaliza una técnica activa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT End();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método siempre devuelve el valor S \_ OK.

## <a name="remarks"></a>Comentarios

Toda la representación de un efecto se realiza dentro de un par correspondiente de [**llamadas ID3DXEffect::Begin**](id3dxeffect--begin.md) e **ID3DXEffect::End.** Después de representar todos los pases, se debe llamar a **ID3DXEffect::End** para finalizar la técnica activa. El sistema de efectos responde mediante el bloque de estado creado cuando se llamó a **ID3DXEffect::Begin,** para restaurar automáticamente el estado de canalización antes **de ID3DXEffect::Begin**.

De forma predeterminada, el sistema de efectos se encarga de guardar el estado antes de una técnica y restaurar el estado después de una técnica. Si decide deshabilitar esta funcionalidad de guardado y restauración, vea [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




