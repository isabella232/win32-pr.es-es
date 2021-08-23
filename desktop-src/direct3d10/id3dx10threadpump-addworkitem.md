---
description: Agregue un elemento de trabajo al bombeo de subprocesos.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: Método ID3DX10ThreadPump::AddWorkItem (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump.AddWorkItem
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 43602019018a9751453eb93f4ffb9b1c29eada6caf120a6721522982c3355dfc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609325"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a>Método ID3DX10ThreadPump::AddWorkItem

Agregue un elemento de trabajo al bombeo de subprocesos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddWorkItem(
  [in]  ID3DX10DataLoader    *pDataLoader,
  [in]  ID3DX10DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDataLoader* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***

Cargador que usará el bombeo de subprocesos cuando un elemento de trabajo requiera que se carguen los datos.

</dd> <dt>

*pDataProcessor* \[ En\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***

Procesador que usará la bomba de subprocesos cuando un elemento de trabajo requiera que se procese los datos.

</dd> <dt>

*pHResult* \[ En\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **NULL.**

</dd> <dt>

*ppDeviceObject* \[ out\]
</dt> <dd>

Tipo: **\* \* void**

Dispositivo que usa el objeto .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




