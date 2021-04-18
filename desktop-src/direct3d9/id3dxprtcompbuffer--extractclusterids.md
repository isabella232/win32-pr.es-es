---
description: Extrae los identificadores de clúster por ejemplo de un búfer de datos comprimidos de ID3DXPRTCompBuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'ID3DXPRTCompBuffer:: ExtractClusterIDs (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718553"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a>ID3DXPRTCompBuffer:: ExtractClusterIDs (método)

Extrae los identificadores de clúster por ejemplo de un búfer de datos comprimidos de [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pClusterIDs* \[ in, out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero a la ubicación en memoria donde se escriben los identificadores. La longitud de memoria necesaria es el valor devuelto por [**ID3DXPRTCompBuffer:: GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTCompBuffer](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
