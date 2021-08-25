---
description: La función ExpertAllocMemory asigna memoria al experto.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Función ExpertAllocMemory (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertAllocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd932a5330baf687d5578bac4e4bfac77ad4f5bad0560263ab7f1e8832e61fe6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890855"
---
# <a name="expertallocmemory-function"></a>Función ExpertAllocMemory

La **función ExpertAllocMemory** asigna memoria al experto.

## <a name="syntax"></a>Sintaxis


```C++
LPVOID WINAPI ExpertAllocMemory(
        HEXPERTKEY hExpertKey,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Identificador único de experto. Monitor de red pasa *hExpertKey* al experto cuando llama a la [función Run.](run.md)

</dd> <dt>

*nBytes* \[ En\]
</dt> <dd>

Memoria asignada, medida en bytes.

</dd> <dt>

*pError* \[ out\]
</dt> <dd>

Indicador de error. Si se produce un error en la función, *el parámetro nBytes* contiene el código de error. Si el código de error es NMERR EXPERT TERMINATE, el experto debe limpiar y \_ \_ volver inmediatamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria asignada.

Si la función no se realiza correctamente, el valor devuelto es **NULL** y *pError* proporciona un código de error que indica el motivo del error.

## <a name="remarks"></a>Comentarios

Es importante tener en cuenta que un experto debe usar las Monitor de red de asignación de memoria (incluido [ExpertReallocMemory)](expertreallocmemory.md)para la administración de memoria. Si se produce un error en el experto durante el tiempo de ejecución, el uso de estas funciones Monitor de red liberar la memoria que ha asignado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




