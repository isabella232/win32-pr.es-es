---
description: Obtiene acceso a los datos del archivo. x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'ID3DXFileData:: Lock (método) (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718321"
---
# <a name="id3dxfiledatalock-method"></a>ID3DXFileData:: Lock (método)

Obtiene acceso a los datos del archivo. x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSize* \[ de\]
</dt> <dd>

Tipo: **[ **tamaño \_ T**](../winprog/windows-data-types.md)\***

Puntero al tamaño de los datos del archivo. x.

</dd> <dt>

*ppData* \[ de\]
</dt> <dd>

Tipo: **const void \* \***

Dirección de un puntero para recibir el puntero de interfaz del objeto de datos del archivo [**ID3DXFileData**](id3dxfiledata.md) . Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Observaciones

El puntero *ppData* solo es válido durante un **ID3DXFileData:: Lock** ... [**ID3DXFileData:: Unlock**](id3dxfiledata--unlock.md) (secuencia). Puede realizar varias llamadas de bloqueo. Sin embargo, debe asegurarse de que el número de llamadas de bloqueo coincide con el número de llamadas de desbloqueo.

Dado que no se garantiza que los datos de archivo se alineen correctamente con límites de bytes, debe acceder a *ppData* con punteros no alineados.

No se garantiza que los valores de parámetro devueltos sean válidos debido a posibles daños en los archivos. por lo tanto, el código debe comprobar los valores de parámetro devueltos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
