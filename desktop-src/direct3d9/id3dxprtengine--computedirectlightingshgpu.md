---
description: Usa la GPU para calcular la contribución de iluminación directa a objetos 3D en los que el sonido de origen se representa mediante una aproximación esférica (SH). La computación de la iluminación en la GPU suele ser mucho más rápida que en la CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: Método ID3DXPRTEngine::ComputeDirectLightingSHGPU (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHGPU
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56dd807d28ba6952cd20c971b675b83687a3015
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170449"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>Método ID3DXPRTEngine::ComputeDirectLightingSHGPU

Usa la GPU para calcular la contribución de iluminación directa a objetos 3D en los que el sonido de origen se representa mediante una aproximación esférica (SH). La computación de la iluminación en la GPU suele ser mucho más rápida que en la CPU.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeDirectLightingSHGPU(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in]      UINT              Flags,
  [in]      UINT              Order,
  [in]      FLOAT             ZBias,
  [in]      FLOAT             ZAngleBias,
  [in, out] LPD3DXPRTBUFFER   pDataOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero al objeto [**de dispositivo IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se usa para ejecutar la simulación en la GPU. El dispositivo debe admitir [sombreadores ps \_ \_ 2 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) píxeles.

> [!Note]  
> Las funciones de devolución de llamada no deben usar el objeto de dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que usa el simulador de GPU.

 

</dd> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Parámetro de simulación de GPU que define la resolución del búfer z de sombra. Debe establecerse en uno de los valores constantes de [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md). Para la simulación de precisión más alta, el valor D3DXSHGPUSIMOPT HIGHQUALITY se puede combinar con uno de los valores \_ D3DXSHGPUSIMOPT \_ SHADOWRESxxx.

</dd> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*ZBias* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Sesgo en la dirección normal.

</dd> <dt>

*ZAngleBias* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Sesgo en la dirección normal, escalado en uno menos el coseno del ángulo con el rayo de luz.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un [**objeto ID3DXPRTBuffer.**](id3dxprtbuffer.md) Este búfer debe tener asignado el número adecuado de canales de color para la simulación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

En este método, el albedo no se multiplica por la señal de luz y solo la luz entrante se integra en el simulador. Al no multiplicar el albedo, puede modelar la variación de albedo a una escala más precisa que la de origen, lo que produce resultados más precisos a partir de la compresión.

Llame [**a MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de transferencia de radiancia precalutada (PRT) por el albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
