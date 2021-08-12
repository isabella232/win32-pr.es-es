---
description: Cree una bomba de subprocesos.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: Función D3DX10CreateThreadPump (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateThreadPump
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 99b5766625f2a269d1fb36e9e808c206d0e3040419f505622ccfe1e27ca4bcdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541069"
---
# <a name="d3dx10createthreadpump-function"></a>Función D3DX10CreateThreadPump

Cree una bomba de subprocesos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX10ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cIoThreads* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de subprocesos de E/S que se crearán. Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.

</dd> <dt>

*cProcThreads* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de subprocesos de proceso que se crearán. Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.

</dd> <dt>

*ppThreadPump* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***

El bombeo de subprocesos creado. Vea [**Id3DX10ThreadPump (interfaz).**](id3dx10threadpump.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Observaciones

Una bomba de subprocesos es un objeto que consume muchos recursos. Solo se debe crear un bombeo de subprocesos por aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[De uso general Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
