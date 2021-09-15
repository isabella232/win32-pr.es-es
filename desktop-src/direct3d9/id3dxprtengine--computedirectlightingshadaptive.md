---
description: Calcula la contribución de iluminación directa a objetos 3D donde el sonido de origen se representa mediante una aproximación armónica esférica (SH), mediante muestreo adaptable.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: Método ID3DXPRTEngine::ComputeDirectLightingSHAdaptive (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569908"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>Método ID3DXPRTEngine::ComputeDirectLightingSHAdaptive

Calcula la contribución de iluminación directa a objetos 3D donde el sonido de origen se representa mediante una aproximación armónica esférica (SH), mediante muestreo adaptable. Este método genera nuevos vértices y caras en la malla para aproximarse con más precisión a la señal de transferencia de radiancia precalcalada (PRT).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*AdaptiveThresh* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Umbral en el vector PRT que se usará para subdividir las caras y los vértices de malla. Si es menor que 1e-6f, se especifica un valor predeterminado de 1e-6f.

</dd> <dt>

*MinEdgeLength* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Longitud mínima del borde de la cara que se generará en el muestreo adaptable. Si el método determina que el valor es demasiado pequeño, se especifica un valor dependiente del modelo. Si es cero, se especifica un valor predeterminado de 4.

</dd> <dt>

*MaxSubdiv* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nivel máximo de subdivisión de una cara que se usará en el muestreo adaptable.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida. Este búfer debe tener el número adecuado de canales de color asignados para la simulación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
