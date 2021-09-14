---
description: Agrega una salida de animación al controlador de animación y registra punteros para transformaciones de escala, rotación y traducción (SRT).
ms.assetid: 8c3197bc-9d03-40ba-869b-151f9c8e96ba
title: Método ID3DXAnimationController::RegisterAnimationOutput (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationOutput
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670f8b311532d096b9957ebbefcf1f6fb15d952
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964887"
---
# <a name="id3dxanimationcontrollerregisteranimationoutput-method"></a>Método ID3DXAnimationController::RegisterAnimationOutput

Agrega una salida de animación al controlador de animación y registra punteros para transformaciones de escala, rotación y traducción (SRT).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterAnimationOutput(
  [in] LPCSTR         Name,
  [in] D3DXMATRIX     *pMatrix,
  [in] D3DXVECTOR3    *pScale,
  [in] D3DXQUATERNION *pRotation,
  [in] D3DXVECTOR3    *pTranslation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre de la salida de animación.

</dd> <dt>

*pMatrix* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una [**estructura D3DXMATRIX**](d3dxmatrix.md) que contiene datos de transformación de SRT. Puede ser **NULL.**

</dd> <dt>

*pScale* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la escala del conjunto de animación. Puede ser **NULL.**

</dd> <dt>

*pRotation* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***

Puntero a un [**cuaternión D3DXQUATERNION**](d3dxquaternion.md) que describe la rotación del conjunto de animación. Puede ser **NULL.**

</dd> <dt>

*pTranslation* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR3**](d3dxvector3.md)\***

Puntero a un vector [**D3DXVECTOR3**](d3dxvector3.md) que describe la traducción del conjunto de animaciones. Puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Si la salida de animación ya está registrada, pMatrix se rellenará con los datos de transformación de entrada.

Los conjuntos de animación creados [**con D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) registran automáticamente todos los conjuntos de animación cargados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
