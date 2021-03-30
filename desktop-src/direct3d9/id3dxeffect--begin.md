---
description: Inicia una técnica activa.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'ID3DXEffect:: Begin (método) (D3DX9Effect. h)'
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
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280353"
---
# <a name="id3dxeffectbegin-method"></a>ID3DXEffect:: Begin (método)

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

*pPasses* \[ enuncia\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero a un valor devuelto que indica el número de pasos necesarios para representar la técnica actual.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

DWORD que determina si se guarda y restaura el estado modificado por un efecto. El valor predeterminado 0 especifica que **ID3DXEffect:: Begin** y [**ID3DXEffect:: end**](id3dxeffect--end.md) guardarán y restaurarán todos los Estados modificados por el efecto (incluidas las constantes de sombreador de píxeles y vértices). Las marcas válidas pueden verse en el [Estado de efecto guardar y restaurar](d3dxfx.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Una aplicación establece una técnica activa en el sistema de efectos llamando a **ID3DXEffect:: Begin**. El sistema de efecto responde capturando todo el estado de canalización que se puede cambiar mediante la técnica en un bloque de estado. Una aplicación señala el final de una técnica mediante una llamada a [**ID3DXEffect:: end**](id3dxeffect--end.md), que usa el bloque de estado para restaurar el estado original. Por lo tanto, el sistema de efectos se encarga de guardar el estado cuando se activa una técnica y restaurar el estado cuando finaliza una técnica. Si decide deshabilitar esta funcionalidad de guardar y restaurar, consulte [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).

En el par **ID3DXEffect:: Begin** y [**ID3DXEffect:: end**](id3dxeffect--end.md) , una aplicación usa [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) para establecer el paso activo, [**ID3DXEffect:: commitChanges**](id3dxeffect--commitchanges.md) si se produce algún cambio de estado después de que se activara el paso, y [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) para finalizar el paso activo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
