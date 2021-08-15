---
description: Accede a los datos del archivo .x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: Método ID3DXFileData::Lock (D3DX9Xof.h)
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
ms.openlocfilehash: c052f570b3206c5a0661a4cf4ab38b259fb476f4eda1322df80e709608d09bf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118520712"
---
# <a name="id3dxfiledatalock-method"></a>Método ID3DXFileData::Lock

Accede a los datos del archivo .x.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSize* \[ En\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Puntero al tamaño de los datos del archivo .x.

</dd> <dt>

*ppData* \[ En\]
</dt> <dd>

Tipo: **const \* \* VOID**

Dirección de un puntero para recibir el puntero de interfaz del objeto de datos de archivo [**ID3DXFileData.**](id3dxfiledata.md) Vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor: D3DXFERR \_ BADVALUE.

## <a name="remarks"></a>Comentarios

El *puntero ppData* solo es válido durante un **id3DXFileData::Lock...** [**Secuencia ID3DXFileData::Unlock.**](id3dxfiledata--unlock.md) Puede realizar varias llamadas de bloqueo. Sin embargo, debe asegurarse de que el número de llamadas de bloqueo coincide con el número de llamadas de desbloqueo.

Dado que no se garantiza que los datos de archivo se alineen correctamente con los límites de bytes, debe tener acceso a *ppData* con punteros UNALIGNED.

No se garantiza que los valores de parámetro devueltos sean válidos debido a posibles daños en el archivo. por lo tanto, el código debe comprobar los valores de parámetro devueltos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
