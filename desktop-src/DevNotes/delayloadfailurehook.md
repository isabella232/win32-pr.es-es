---
description: Devuelve la dirección de una función de devolución de llamada de error de carga retrasada para la DLL y el proceso especificados.
ms.assetid: db1d34cb-800a-4984-b4a3-d1ce1c6ee86c
title: DelayLoadFailureHook función)
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
ms.openlocfilehash: f4986b70332a2581580d7e3b274e9d3cdcd96532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660494"
---
# <a name="delayloadfailurehook-function"></a>DelayLoadFailureHook función)

Devuelve la dirección de una función de devolución de llamada de error de carga retrasada para la DLL y el proceso especificados.

## <a name="syntax"></a>Sintaxis


```C++
FARPROC WINAPI DelayLoadFailureHook(
  _In_ LPCSTR pszDllName,
  _In_ LPCSTR pszProcName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pszDllName* \[ de\]
</dt> <dd>

Nombre del archivo DLL.

</dd> <dt>

*pszProcName* \[ de\]
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

 

 




