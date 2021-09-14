---
description: Establece un puntero a una función de devolución de llamada opcional que calcula el porcentaje de cálculos armónicos esféricos (SH) completados y ofrece al autor de la llamada la opción de anular el simulador.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: Método ID3DXPRTEngine::SetCallBack (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966695"
---
# <a name="id3dxprtenginesetcallback-method"></a>Método ID3DXPRTEngine::SetCallBack

Establece un puntero a una función de devolución de llamada opcional que calcula el porcentaje de cálculos armónicos esféricos (SH) completados y ofrece al autor de la llamada la opción de anular el simulador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCB* \[ En\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Puntero a la [función de devolución de llamada LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que calcula el porcentaje de cálculos SH completados. La función de devolución de llamada debe implementarse para devolver S \_ OK para seguir ejecutando el simulador. Cualquier otro valor anulará el simulador.

</dd> <dt>

*Frecuencia* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Frecuencia de llamadas de devolución de llamada. El inverso de Frequency es aproximadamente el número de veces que se llamará a la función de devolución de llamada.

</dd> <dt>

*lpUserContext* \[ En\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada. Normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
