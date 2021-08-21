---
description: Establece la técnica activa.
ms.assetid: 18f19773-a9f8-47f9-9334-acc95e0f0eb7
title: Método ID3DXEffect::SetTechnique (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.SetTechnique
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7b10190df7c4527535a35c2c352933ec652452d51804e23b8aad338e6ca40522
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987554"
---
# <a name="id3dxeffectsettechnique-method"></a>Método ID3DXEffect::SetTechnique

Establece la técnica activa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTechnique(
  [in] D3DXHANDLE hTechnique
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hTechnique* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la técnica. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




