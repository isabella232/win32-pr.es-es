---
description: La función ExpertReallocMemory aumenta o disminuye la cantidad de memoria asignada por Monitor de red.
ms.assetid: 78b99a66-692a-4e83-8b0d-d68caf156bb6
title: Función ExpertReallocMemory (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069342"
---
# <a name="expertreallocmemory-function"></a>Función ExpertReallocMemory

La **función ExpertReallocMemory** aumenta o disminuye la cantidad de memoria asignada por Monitor de red.

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

*hExpertKey* \[ En\]
</dt> <dd>

Identificador único pasado al experto en [**Ejecutar**](run.md) o [**configurar**](configure.md).

</dd> <dt>

*pOriginalMemory* \[ En\]
</dt> <dd>

Puntero a la memoria asignada por Monitor de red. El *puntero pOriginalMemory* se puede devolver mediante una llamada anterior a [**ExpertAllocMemory**](expertallocmemory.md) **o ExpertReallocMemory**.

</dd> <dt>

*nBytes* \[ En\]
</dt> <dd>

Tamaño de la memoria reasignada.

</dd> <dt>

*pError* \[ out\]
</dt> <dd>

En la devolución, código de error si se produce un error en la función. Si el código de error es NMERR EXPERT TERMINATE, el experto debe limpiar y \_ \_ volver inmediatamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria asignada.

Si la función no se realiza correctamente, el valor devuelto es **NULL** y *pError* (si es un valor distinto de **NULL)** indica el motivo del error.

## <a name="remarks"></a>Observaciones

Es importante tener en cuenta que un experto debe usar las Monitor de red de asignación de memoria para la administración de memoria. Si se produce un error en el experto durante el tiempo de ejecución, el uso de estas funciones Monitor de red liberar la memoria que ha asignado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




