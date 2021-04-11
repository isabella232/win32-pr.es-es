---
description: Calcula el Radiance de origen resultante de un único rebote de luz interreflejada. Este método se puede usar para cualquier escena iluminada, incluido un modelo Radiance (PRT) precalculado basado en armónico (SH).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'ID3DXPRTEngine:: ComputeBounce (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d40d4b2686087864cad17df0feb99dbc890033b0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362740"
---
# <a name="id3dxprtenginecomputebounce-method"></a>ID3DXPRTEngine:: ComputeBounce (método)

Calcula el Radiance de origen resultante de un único rebote de luz interreflejada. Este método se puede usar para cualquier escena iluminada, incluido un modelo Radiance (PRT) precalculado basado en armónico (SH).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDataIn* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa el objeto 3D del rebote de luz anterior. Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que modela un único rebote de la luz interreflejada. Este búfer de salida debe tener asignado el número adecuado de canales de color para la simulación.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que es la suma de todas las salidas pDataOut anteriores. Puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Utilice la siguiente secuencia de llamada para modelar varios rebotes claros con iluminación directa.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



Use la siguiente secuencia de llamada para modelar varios rebotes claros con dispersión de subsuperficies.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



La salida de este método no incluye albedo y solo la luz entrante está integrada en el simulador. Si no se multiplica el albedo, puede modelar la variación de Albedo en una escala más precisa que el Radiance de origen, con lo que se obtienen resultados más precisos de la compresión.

Llame a [**ID3DXPRTEngine:: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) para multiplicar cada vector de PRT por el albedo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine:: Compute (no es)**](id3dxprtengine--computess.md)
</dt> </dl>

 

 




