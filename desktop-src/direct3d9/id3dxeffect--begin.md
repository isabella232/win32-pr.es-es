---
description: Inicia una técnica activa.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: Método ID3DXEffect::Begin (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4f4e41830b0bb4507e3969c327c84a85c5336e5f07389fa12e05f3a92f4089a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675465"
---
# <a name="id3dxeffectbegin-method"></a>Método ID3DXEffect::Begin

Inicia una técnica activa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPasses* \[ out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero a un valor devuelto que indica el número de pases necesarios para representar la técnica actual.

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

DWORD que determina si el estado modificado por un efecto se guarda y restaura. El valor predeterminado 0 especifica que **ID3DXEffect::Begin** e [**ID3DXEffect::End**](id3dxeffect--end.md) guardarán y restaurarán todo el estado modificado por el efecto (incluidas las constantes de sombreador de píxeles y vértices). Las marcas válidas se pueden ver en Effect State Save and Restore Flags (Guardar [y restaurar marcas de estado de efecto).](d3dxfx.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Una aplicación establece una técnica activa en el sistema de efectos mediante una llamada **a ID3DXEffect::Begin**. El sistema de efectos responde capturando todo el estado de canalización que la técnica puede cambiar en un bloque de estado. Una aplicación señala el final de una técnica mediante una llamada a [**ID3DXEffect::End**](id3dxeffect--end.md), que usa el bloque de estado para restaurar el estado original. Por lo tanto, el sistema de efectos se encarga de guardar el estado cuando una técnica se activa y de restaurar el estado cuando finaliza una técnica. Si decide deshabilitar esta funcionalidad de guardado y restauración, vea [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).

Dentro del par **ID3DXEffect::Begin** e [**ID3DXEffect::End,**](id3dxeffect--end.md) una aplicación usa [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) para establecer el paso activo, [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) si se produjo algún cambio de estado después de activar el paso e [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) para finalizar el paso activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
