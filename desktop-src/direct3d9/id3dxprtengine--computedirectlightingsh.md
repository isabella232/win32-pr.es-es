---
description: Calcula la contribución de iluminación directa a objetos 3D donde el sonido de origen se representa mediante una aproximación esférica (SH).
ms.assetid: 52d614cc-578a-4f2b-ba91-70d0c4371042
title: Método ID3DXPRTEngine::ComputeDirectLightingSH (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 01b6c3cff082c40c4df5d9bee1d997599a41965b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969631"
---
# <a name="id3dxprtenginecomputedirectlightingsh-method"></a>Método ID3DXPRTEngine::ComputeDirectLightingSH

Calcula la contribución de iluminación directa a objetos 3D donde el sonido de origen se representa mediante una aproximación esférica (SH).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeDirectLightingSH(
  [in]      UINT            Order,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida que modela la contribución de iluminación directa con la aproximación SH. Este búfer debe tener asignado el número adecuado de canales de color para la simulación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

La salida no incluye albedo y solo se integra la luz entrante en el simulador. Al no multiplicar el albedo, puede modelar la variación de albedo a una escala más precisa que la de origen, lo que produce resultados más precisos a partir de la compresión.

Llame [**a ID3DXPRTEngine::MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de transferencia de radiancia precalutizado (PRT) por el albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
