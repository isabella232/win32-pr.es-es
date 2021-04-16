---
description: Usa la GPU para calcular la contribución de iluminación directa a objetos 3D donde el Radiance de origen se representa mediante una aproximación de armónico (SH) esférica. Calcular la iluminación en la GPU generalmente será mucho más rápido que en la CPU.
ms.assetid: ccea5a5e-23f1-4fdf-bce8-9bfc35d45257
title: 'ID3DXPRTEngine:: ComputeDirectLightingSHGPU (método) (D3DX9Mesh. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678853"
---
# <a name="id3dxprtenginecomputedirectlightingshgpu-method"></a>ID3DXPRTEngine:: ComputeDirectLightingSHGPU (método)

Usa la GPU para calcular la contribución de iluminación directa a objetos 3D donde el Radiance de origen se representa mediante una aproximación de armónico (SH) esférica. Calcular la iluminación en la GPU generalmente será mucho más rápido que en la CPU.

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

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero al objeto de dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se usa para ejecutar la simulación en la GPU. El dispositivo debe admitir los sombreadores de píxeles de [PS \_ 2 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-ps-2-0.md) .

> [!Note]  
> Las funciones de devolución de llamada no deben usar el objeto de dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que usa el simulador de GPU.

 

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Parámetro de simulación de GPU que define la resolución de la sombra del búfer de z. Debe establecerse en uno de los valores constantes de [**D3DXSHGPUSIMOPT**](./d3dxshgpusimopt.md). Para especificar una simulación de precisión mayor, el \_ valor de D3DXSHGPUSIMOPT highquality puede combinarse con uno de los valores de D3DXSHGPUSIMOPT \_ SHADOWRESxxx.

</dd> <dt>

*Pedido* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. La evaluación genera coeficientes de pedido ². El grado de evaluación es order-1.

</dd> <dt>

*ZBias* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Sesgo en la dirección normal.

</dd> <dt>

*ZAngleBias* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Sesgo en la dirección normal, escalada en una menos el coseno del ángulo con el rayo claro.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) . Este búfer debe tener asignado el número adecuado de canales de color para la simulación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

En este método, el albedo no se multiplica por la señal luminosa y solo se integra la luz entrante en el simulador. Si no se multiplica el albedo, puede modelar la variación de Albedo en una escala más precisa que el Radiance de origen, con lo que se obtienen resultados más precisos de la compresión.

Llame a [**MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de transferencia Radiance (PRT) precalculado por Albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
