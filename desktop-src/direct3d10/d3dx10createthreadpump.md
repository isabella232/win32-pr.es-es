---
description: Cree un bombeo de subprocesos.
ms.assetid: a7a016e2-784d-4d7a-8058-88895bf3c4e2
title: Función D3DX10CreateThreadPump (D3DX10. h)
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
ms.openlocfilehash: 8a27f8df1f4eaa8e7f41e863d703063308f9c595
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003937"
---
# <a name="d3dx10createthreadpump-function"></a>D3DX10CreateThreadPump función)

Cree un bombeo de subprocesos.

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

*cIoThreads* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de subprocesos de e/s que se van a crear. Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.

</dd> <dt>

*cProcThreads* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de subprocesos del proceso que se van a crear. Si se especifica 0, Direct3D intentará calcular el número óptimo de subprocesos en función de la configuración de hardware.

</dd> <dt>

*ppThreadPump* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\*\***

El bombeo de subprocesos creado. Consulte la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Un bombeo de subprocesos es un objeto que consume muchos recursos. Solo se debe crear un bombeo de subprocesos por aplicación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de De uso general](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
