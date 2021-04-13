---
description: Finaliza una técnica activa.
ms.assetid: 7297aa67-5cd4-4557-b5ef-faa6c27eaeb5
title: 'ID3DXEffect:: end (método) (D3DX9Effect. h)'
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
ms.openlocfilehash: baaccd7710845296497dcc7f16d3d71c7ceeb9bd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362602"
---
# <a name="id3dxeffectend-method"></a>ID3DXEffect:: end (método)

Finaliza una técnica activa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT End();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método siempre devuelve el valor S \_ correcto.

## <a name="remarks"></a>Observaciones

Toda la representación en un efecto se realiza dentro de un par coincidente de llamadas a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) y **ID3DXEffect:: end** . Una vez que se representan todas las pasadas, se debe llamar a **ID3DXEffect:: end** para finalizar la técnica activa. El sistema de efecto responde mediante el uso del bloque de estado creado cuando se llamó a **ID3DXEffect:: Begin** para restaurar automáticamente el estado de la canalización antes de **ID3DXEffect:: Begin**.

De forma predeterminada, el sistema de efectos se encarga de guardar el estado antes de una técnica y restaurar el estado después de una técnica. Si decide deshabilitar esta funcionalidad de guardar y restaurar, consulte [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




