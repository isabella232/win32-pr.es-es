---
description: La función ExpertMemorySize devuelve la cantidad de memoria asignada por la función ExpertAllocMemory.
ms.assetid: 60d3f33d-dc03-4c39-98fa-ec093398b51b
title: Función ExpertMemorySize (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertMemorySize
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 69dae4ca2a7f7a9e3b2f77047475c5dd35f54a3394b4481c2f452a46e983c35e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744275"
---
# <a name="expertmemorysize-function"></a>Función ExpertMemorySize

La **función ExpertMemorySize** devuelve la cantidad de memoria asignada por la [función ExpertAllocMemory.](expertallocmemory.md)

## <a name="syntax"></a>Sintaxis


```C++
SIZE_T WINAPI ExpertMemorySize(
  _In_ HEXPERTKEY hExpertKey,
  _In_ LPVOID     pOriginalMemory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* \[ En\]
</dt> <dd>

Identificador único de experto. Monitor de red pasa *hExpertKey* al experto cuando llama a la [función Run.](run.md)

</dd> <dt>

*pOriginalMemory* \[ En\]
</dt> <dd>

Puntero a la dirección de memoria del experto asignado por [ExpertAllocMemory](expertallocmemory.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve la cantidad de memoria asignada en bytes.

## <a name="remarks"></a>Comentarios

Para obtener información sobre el **tipo de datos SIZE \_ T** que **devuelve ExpertMemorySize,** vea Tipos de datos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




