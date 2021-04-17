---
description: Comienza un paso, dentro de la técnica activa.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'ID3DXEffect:: BeginPass (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718241"
---
# <a name="id3dxeffectbeginpass-method"></a>ID3DXEffect:: BeginPass (método)

Comienza un paso, dentro de la técnica activa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pass* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de entero de base cero de la técnica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Una aplicación establece un paso activo (dentro de una técnica activa) en el sistema de efectos llamando a **ID3DXEffect:: BeginPass**. Una aplicación señala el final del paso activo mediante una llamada a [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md). **ID3DXEffect:: BeginPass** y **ID3DXEffect:: EndPass** deben aparecer en un par coincidente, dentro de un par coincidente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) y [**ID3DXEffect:: end**](id3dxeffect--end.md) calls.

Si la aplicación cambia cualquier estado de efecto mediante cualquiera de los métodos [**Effect:: setx**](id3dxeffect.md) dentro de un par de coincidencia **ID3DXEffect:: BeginPass** / [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) , la aplicación debe llamar a [**ID3DXEffect:: commitChanges**](id3dxeffect--commitchanges.md) para establecer la actualización del dispositivo con los cambios de estado. Si no se produce ningún cambio de estado dentro de un par de coincidencia **ID3DXEffect:: BeginPass** y **ID3DXEffect:: EndPass** , no es necesario llamar a **ID3DXEffect:: commitChanges**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
