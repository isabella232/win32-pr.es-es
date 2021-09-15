---
title: Función D3D12GetFormatPlaneCount (D3dx12.h)
description: Obtiene el número de planos para el formato DXGI especificado para el adaptador virtual especificado (id. 3D12Device).
ms.assetid: CD21F6F9-A9AA-4CE8-A430-57C70326CB4B
keywords:
- Función D3D12GetFormatPlaneCount
topic_type:
- apiref
api_name:
- D3D12GetFormatPlaneCount
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfc2e88c162068de2b97c9df5071398e2fab068
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359820"
---
# <a name="d3d12getformatplanecount-function"></a>Función D3D12GetFormatPlaneCount

Obtiene el número de planos para el formato DXGI especificado para el adaptador virtual especificado **(un ID3D12Device**).

## <a name="syntax"></a>Sintaxis


```C++
UINT8 inline D3D12GetFormatPlaneCount(
  _In_ ID3D12Device *pDevice,
       DXGI_FORMAT  Format
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)\***

Adaptador virtual [**(id. 3D12Device)**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)para el que se va a obtener el número de plano.

</dd> <dt>

*Format* 
</dt> <dd>

Tipo: **[ **DXGI \_ FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)**

FORMATO [**DXGI \_ para**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) el que se va a obtener el recuento de plano.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UINT8**

Número de plano para el formato especificado en el adaptador virtual especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**INFORMACIÓN DE FORMATO DE DATOS \_ DE CARACTERÍSTICAS \_ DE \_ D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_format_info)
</dt> <dt>

[**CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport)
</dt> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

