---
description: La función ExpertFreeMemory libera la memoria adquirida por las llamadas a las funciones ExpertAllocMemory y ExpertReallocMemory.
ms.assetid: 0e7cc791-98dd-4522-afab-76ac9e74c715
title: Función ExpertFreeMemory (Netmon. h)
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
ms.openlocfilehash: cc26056a3ec3e8820c363d97f92c7eb382cd0622
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666299"
---
# <a name="expertfreememory-function"></a>ExpertFreeMemory función)

La función **ExpertFreeMemory** libera la memoria adquirida por las llamadas a las funciones [**ExpertAllocMemory**](expertallocmemory.md) y [**ExpertReallocMemory**](expertreallocmemory.md) .

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

Identificador de experto único. Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .

</dd> <dt>

*pMemory* \[ de\]
</dt> <dd>

Puntero a la memoria que Monitor de red asigna. El puntero *pMemory* puede ser devuelto por una llamada anterior a [**ExpertAllocMemory**](expertallocmemory.md) o [**ExpertReallocMemory**](expertreallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente. el valor devuelto es NMERR \_ Success.

Si la función no se realiza correctamente, el valor devuelto indica la razón del error. Si el valor devuelto es NMERR \_ Expert \_ Terminate, el experto limpia y devuelve inmediatamente.

## <a name="remarks"></a>Observaciones

Es importante tener en cuenta que un experto debe usar las funciones de asignación de memoria Monitor de red para la administración de memoria. Si se produce un error en el experto durante el tiempo de ejecución, el uso de estas funciones permitirá a Monitor de red liberar la memoria que ha asignado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




