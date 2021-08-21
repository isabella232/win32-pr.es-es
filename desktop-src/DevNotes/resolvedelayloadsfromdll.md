---
description: Reenvía el trabajo para resolver las importaciones de carga retrasada desde el binario primario a un binario de destino.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: Función ResolveDelayLoadsFromDll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadsFromDll
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 894360a20456b73d0cfad19cd125405caf0c3624821aca21e3e107699d1cc372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571545"
---
# <a name="resolvedelayloadsfromdll-function"></a>Función ResolveDelayLoadsFromDll

Reenvía el trabajo para resolver las importaciones de carga retrasada desde el binario primario a un binario de destino.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS WINAPI ResolveDelayLoadsFromDll(
  _In_       PVOID  ParentBase,
  _In_       LPCSTR TargetDllName,
  _Reserved_ ULONG  Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ParentBase* \[ En\]
</dt> <dd>

La dirección base del módulo que retrasa carga otro binario.

</dd> <dt>

*TargetDllName* \[ En\]
</dt> <dd>

Nombre del archivo DLL de destino.

</dd> <dt>

*Marcas* 
</dt> <dd>

Reservado; debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Dirección del descriptor de carga retrasada, si se encuentra; de lo contrario, **NULL.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad del vinculador con Delay-Loaded dll](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




