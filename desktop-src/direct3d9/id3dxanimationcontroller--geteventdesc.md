---
description: Obtiene una descripción de un evento de animación especificado.
ms.assetid: 7fb3def5-8df2-458d-b68e-5d540fd0a738
title: 'ID3DXAnimationController:: GetEventDesc (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetEventDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9f717c032358dd921be2df1c8a84d1aa02a7a93a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718475"
---
# <a name="id3dxanimationcontrollergeteventdesc-method"></a>ID3DXAnimationController:: GetEventDesc (método)

Obtiene una descripción de un evento de animación especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetEventDesc(
  [in]  D3DXEVENTHANDLE  hEvent,
  [out] LPD3DXEVENT_DESC pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hEvent* \[ de\]
</dt> <dd>

Tipo: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Identificador de evento de un evento de animación que se va a describir.

</dd> <dt>

*pDesc* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXEVENT \_ DESC**](d3dxevent-desc.md)**

Puntero a una [**estructura \_ DESC de D3DXEVENT**](d3dxevent-desc.md) que contiene una descripción del evento de animación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




