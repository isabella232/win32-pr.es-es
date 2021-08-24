---
description: Devuelve la dirección de una función de devolución de llamada de error de carga retrasada para el archivo DLL y el proceso especificados.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: Función DelayLoadFailureHook
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DelayLoadFailureHook
api_type:
- DllExport
api_location:
- kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-0.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
ms.openlocfilehash: 8724073a8f5f124cf23d6ba15390c8028d308354aa1e2c896f1d2c9f5030ea45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795287"
---
# <a name="delayloadfailurehook-function"></a>Función DelayLoadFailureHook

Devuelve la dirección de una función de devolución de llamada de error de carga retrasada para el archivo DLL y el proceso especificados.

## <a name="syntax"></a>Sintaxis


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszDllName* \[ En\]
</dt> <dd>

Nombre del archivo DLL.

</dd> <dt>

*pszProcName* \[ En\]
</dt> <dd>

Nombre del proceso.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Dirección de la función de devolución de llamada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Enlaces de error](https://msdn.microsoft.com/library/sfcfb0a3(v=VS.71).aspx)
</dt> </dl>

 

 




