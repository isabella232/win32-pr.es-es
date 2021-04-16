---
description: La función ExpertReallocMemory aumenta o reduce la cantidad de memoria asignada por Monitor de red.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Función ExpertReallocMemory (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertReallocMemory
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8f562443f9ca66def7e053f5958b17e70af50140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652369"
---
# <a name="expertreallocmemory-function"></a>ExpertReallocMemory función)

La función **ExpertReallocMemory** aumenta o reduce la cantidad de memoria asignada por monitor de red.

## <a name="syntax"></a>Sintaxis


```C++
LPVOID WINAPI ExpertReallocMemory(
  _In_  HEXPERTKEY hExpertKey,
  _In_  LPVOID     pOriginalMemory,
  _In_  SIZE_T     nBytes,
  _Out_ LPDWORD    pError
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* \[ de\]
</dt> <dd>

Identificador único que se pasa al experto en [**Ejecutar**](run.md) o [**configurar**](configure.md).

</dd> <dt>

*pOriginalMemory* \[ de\]
</dt> <dd>

Puntero a la memoria asignada por Monitor de red. El puntero *pOriginalMemory* puede ser devuelto por una llamada anterior a [**ExpertAllocMemory**](expertallocmemory.md) o **ExpertReallocMemory**.

</dd> <dt>

*nBytes* \[ de\]
</dt> <dd>

Tamaño de la memoria reasignada.

</dd> <dt>

*perror* \[ enuncia\]
</dt> <dd>

En la devolución, un código de error si se produce un error en la función. Si el código de error es NMERR \_ Expert \_ Terminate, el experto debe limpiar y volver inmediatamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria asignada.

Si la función no se realiza correctamente, el valor devuelto es **null** y el *perror* (si es un valor distinto de **null** ) indica el motivo del error.

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



 

 




