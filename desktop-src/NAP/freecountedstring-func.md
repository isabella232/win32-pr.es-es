---
title: Función FreeCountedString (NapUtil.h)
description: Libera una estructura de datos CountedString.
ms.assetid: d080d247-9339-474b-866e-b412e82dd35f
keywords:
- Función Nap de FreeCountedString
topic_type:
- apiref
api_name:
- FreeCountedString
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dff73bc3511f34c8d791c4daf784d57ad12cc343ee9ed5628dd92cc6f4e5fc16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368885"
---
# <a name="freecountedstring-function"></a>Función FreeCountedString

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función FreeCountedString** libera una [**estructura de datos CountedString.**](/windows/win32/api/naptypes/ns-naptypes-countedstring)

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI FreeCountedString(
  _In_ CountedString *countedString
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*countedString* \[ En\]
</dt> <dd>

Puntero a la estructura [**de datos CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) que se liberará.

</dd> </dl>

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

[**AllocCountedString**](alloccountedstring-func.md)
</dt> </dl>

 

 





