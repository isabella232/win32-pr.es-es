---
title: Función D3DX11UnsetAllDeviceObjects (D3DX11core.h)
description: Nota La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para las aplicaciones de Windows Store. Nota En lugar de usar esta función, se recomienda usar el método ClearState ID3D11DeviceContext.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- Función D3DX11UnsetAllDeviceObjects Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e046bbb67cfaf5e13a22e5b704e202c21ebc8fa82dfde3a21fb83f09dfc3a345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535980"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a>Función D3DX11UnsetAllDeviceObjects

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 

> [!Note]  
> En lugar de usar esta función, se recomienda usar el [**método ID3D11DeviceContext::ClearState.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate)

 

Quita todos los recursos del dispositivo estableciendo sus punteros en **NULL.** Se debe llamar a este método durante el cierre de la aplicación. Ayuda a garantizar que, cuando se liberan todos sus recursos, ninguno de ellos está enlazado al dispositivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pContext* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Puntero a un [**objeto ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno [de Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





