---
description: Comienza un paso, dentro de la técnica activa.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: Método ID3DXEffect::BeginPass (D3DX9Effect.h)
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
ms.openlocfilehash: 9013a67c2d4e0e9760167bc979ac05edd4879c5414ce5c9b9c55528baf3f6a18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987555"
---
# <a name="id3dxeffectbeginpass-method"></a>Método ID3DXEffect::BeginPass

Comienza un paso, dentro de la técnica activa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pass* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice entero de base cero en la técnica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Una aplicación establece un paso activo (dentro de una técnica activa) en el sistema de efectos mediante una llamada a **ID3DXEffect::BeginPass**. Una aplicación señala el final del paso activo llamando a [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md). **ID3DXEffect::BeginPass** e **ID3DXEffect::EndPass** deben producirse en un par correspondiente, dentro de un par correspondiente de [**llamadas ID3DXEffect::Begin**](id3dxeffect--begin.md) e [**ID3DXEffect::End.**](id3dxeffect--end.md)

Si la aplicación cambia cualquier estado de efecto mediante cualquiera de los métodos [**Effect::Setx**](id3dxeffect.md) dentro de un par de **coincidencias ID3DXEffect::BeginPass** / [**ID3DXEffect::EndPass,**](id3dxeffect--endpass.md) la aplicación debe llamar a [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) para establecer la actualización del dispositivo con los cambios de estado. Si no se produce ningún cambio de estado dentro de un par de **coincidencias ID3DXEffect::BeginPass** e **ID3DXEffect::EndPass,** no es necesario llamar a **ID3DXEffect::CommitChanges**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 
