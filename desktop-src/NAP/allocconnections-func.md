---
title: Función AllocConnections (NapUtil.h)
description: Asigna memoria para un número especificado de estructuras Connections.
ms.assetid: 0e0075ed-6e4c-43f7-af40-c6dea2808d05
keywords:
- Función Nap de AllocConnections
topic_type:
- apiref
api_name:
- AllocConnections
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf86a44b81ef12234fdac675aa55d36c5e1a336b4316382c3fd322cf0d6ba87a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800216"
---
# <a name="allocconnections-function"></a>AllocConnections (función)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función AllocConnections** asigna memoria para un número especificado de estructuras [**Connections.**](connections-struct.md)

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI HRESULT WINAPI AllocConnections(
  _Inout_ Connections **connections,
  _In_    UINT16      connectionsCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*conexiones* \[ in, out\]
</dt> <dd>

Puntero a una matriz de estructuras Connections [**recién**](connections-struct.md) asignadas.

</dd> <dt>

*connectionsCount* \[ En\]
</dt> <dd>

Número de estructuras que se asignarán a las *conexiones*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                                   | Descripción                                                                |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | La operación se ha completado correctamente.<br/>                       |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Se pasó un argumento no válido.<br/>                                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | El sistema está sin memoria virtual. Se ha dado error en esta operación.<br/> |



 

## <a name="remarks"></a>Comentarios

Todas las interfaces COM compatibles con el sistema NAP usan reglas de administración de memoria COM estándar y los asignadores de memoria COM (**CoTaskMemAlloc** y **CoTaskMemFree**):

-   **El** autor de la llamada asigna y libera los parámetros de .
-   **El** destinatario asigna los parámetros out y el autor de la llamada lo libera **mediante CoTaskMem**.
-   **El autor de** la llamada asigna los parámetros de entrada y salida, los libera y reasigna el destinatario y, en última instancia, los libera el autor de la llamada, mediante **CoTaskMem**.

Todas las funciones NAP para liberar memoria también liberan todos los punteros incrustados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Header<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**FreeConnections**](freeconnections-func.md)
</dt> </dl>

 

 





