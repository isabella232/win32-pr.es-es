---
description: La función ExpertFreeMemory libera la memoria adquirida por llamadas a las funciones ExpertAllocMemory y ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Función ExpertFreeMemory (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertFreeMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: edc4d1a9e33139372d0f397053d233a28c9e2445ba270a47e7dbfe97090eb6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890835"
---
# <a name="expertfreememory-function"></a>Función ExpertFreeMemory

La **función ExpertFreeMemory** libera la memoria adquirida por llamadas a las funciones [**ExpertAllocMemory**](expertallocmemory.md) y [**ExpertReallocMemory.**](expertreallocmemory.md)

## <a name="syntax"></a>Sintaxis


```C++
SIZE_T WINAPI ExpertFreeMemory(
       HEXPERTKEY hExpertKey,
  _In_ LPVOID     pMemory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* 
</dt> <dd>

Identificador único de experto. Monitor de red pasa *hExpertKey* al experto cuando llama a la [función Run.](run.md)

</dd> <dt>

*pMemory* \[ En\]
</dt> <dd>

Puntero a la memoria Monitor de red asigna. El *puntero pMemory* se puede devolver mediante una llamada anterior a [**ExpertAllocMemory**](expertallocmemory.md) o [**ExpertReallocMemory**](expertreallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente. el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto indica el motivo del error. Si el valor devuelto es NMERR EXPERT TERMINATE, el experto limpia inmediatamente \_ \_ y devuelve.

## <a name="remarks"></a>Comentarios

Es importante tener en cuenta que un experto debe usar las Monitor de red de asignación de memoria para la administración de memoria. Si se produce un error en el experto durante el tiempo de ejecución, el uso de estas funciones Monitor de red liberar la memoria que ha asignado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




