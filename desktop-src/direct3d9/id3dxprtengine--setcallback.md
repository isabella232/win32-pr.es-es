---
description: Establece un puntero a una función de devolución de llamada opcional que calcula el porcentaje de cálculos armónicos esférico (SH) completado y proporciona al llamador la opción de anular el simulador.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'ID3DXPRTEngine:: SetCallBack (método) (D3DX9Mesh. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707953"
---
# <a name="id3dxprtenginesetcallback-method"></a>ID3DXPRTEngine:: SetCallBack (método)

Establece un puntero a una función de devolución de llamada opcional que calcula el porcentaje de cálculos armónicos esférico (SH) completado y proporciona al llamador la opción de anular el simulador.

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

*pCB* \[ de\]
</dt> <dd>

Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**

Puntero a la función de devolución de llamada [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) que calcula el porcentaje de los cálculos de SH completados. La función de devolución de llamada se debe implementar para que se devuelvan \_ los elementos correctos para seguir ejecutando el simulador. Cualquier otro valor anulará el simulador.

</dd> <dt>

*Frecuencia* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Frecuencia de llamadas de devolución de llamada. El inverso de Frequency es aproximadamente el número de veces que se llamará a la función de devolución de llamada.

</dd> <dt>

*lpUserContext* \[ de\]
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada. Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es S \_ OK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
