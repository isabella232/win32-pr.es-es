---
title: Función FreeFixupInfo (NapUtil.h)
description: Libera una estructura de datos FixupInfo.
ms.assetid: 6bf71ccf-2618-46a3-8a04-9f83a5b7b429
keywords:
- Función NAP FreeFixupInfo
topic_type:
- apiref
api_name:
- FreeFixupInfo
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c869123aadd5310a346dcf8e7a2184ec84f7e40500744cbaf610cbfc54db42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368875"
---
# <a name="freefixupinfo-function"></a>Función FreeFixupInfo

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función FreeFixupInfo** libera una [**estructura de datos FixupInfo.**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo)

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI FreeFixupInfo(
  _In_ FixupInfo *fixupInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fixupInfo* \[ En\]
</dt> <dd>

Puntero a la estructura [**de datos FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) que se liberará.

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

[**AllocFixupInfo**](allocfixupinfo-func.md)
</dt> </dl>

 

 





