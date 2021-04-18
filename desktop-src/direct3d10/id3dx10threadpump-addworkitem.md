---
description: Agregue un elemento de trabajo al bombeo de subprocesos.
ms.assetid: f07789dc-a3d5-4bad-9768-527e701271b8
title: 'ID3DX10ThreadPump:: AddWorkItem (método) (D3DX10. h)'
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
ms.openlocfilehash: aaf5286ca6cf7b61b0027b176d9a9261bd0beaa8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708110"
---
# <a name="id3dx10threadpumpaddworkitem-method"></a>ID3DX10ThreadPump:: AddWorkItem (método)

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

*pDataLoader* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DX10DataLoader**](id3dx10dataloader.md)\***

Cargador que el bombeo de subprocesos usará cuando un elemento de trabajo requiera que se carguen los datos.

</dd> <dt>

*pDataProcessor* \[ de\]
</dt> <dd>

Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\***

Procesador que utilizará el bombeo de subprocesos cuando un elemento de trabajo requiera que se procesen los datos.

</dd> <dt>

*pHResult* \[ de\]
</dt> <dd>

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Puntero al valor devuelto. Puede ser **null**.

</dd> <dt>

*ppDeviceObject* \[ enuncia\]
</dt> <dd>

Tipo: **void \* \***

El dispositivo que usa el objeto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10ThreadPump](id3dx10threadpump.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




