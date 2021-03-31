---
description: La función ExpertAllocMemory asigna memoria para el experto.
ms.assetid: 9ada5d3f-5f1d-4d3a-b79a-d51e021240f6
title: Función ExpertAllocMemory (Netmon. h)
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
ms.openlocfilehash: b30aba5e2b448df141d0c82e6ec5a2b0d9b3303f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808731"
---
# <a name="expertallocmemory-function"></a>ExpertAllocMemory función)

La función **ExpertAllocMemory** asigna memoria para el experto.

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

Identificador de experto único. Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .

</dd> <dt>

*nBytes* \[ de\]
</dt> <dd>

Memoria asignada, medida en bytes.

</dd> <dt>

*perror* \[ enuncia\]
</dt> <dd>

Indicador de error. Si se produce un error en la función, el parámetro *nBytes* contiene el código de error. Si el código de error es NMERR \_ Expert \_ Terminate, el experto debe limpiar y volver inmediatamente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero a la memoria asignada.

Si la función no se realiza correctamente, el valor devuelto es **null** y el *perror* proporciona un código de error que indica la razón del error.

## <a name="remarks"></a>Observaciones

Es importante tener en cuenta que un experto debe usar las funciones de asignación de memoria Monitor de red (incluido [ExpertReallocMemory](expertreallocmemory.md)) para la administración de memoria. Si se produce un error en el experto durante el tiempo de ejecución, el uso de estas funciones permitirá a Monitor de red liberar la memoria que ha asignado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




