---
description: Reenvía el trabajo en la resolución de las importaciones de carga retrasada del archivo binario primario a un binario de destino.
ms.assetid: 65629d7b-36b0-426b-a20d-ec736b8461dc
title: ResolveDelayLoadsFromDll función)
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
ms.openlocfilehash: a0fb517de7384a964c21c9e1a0a3e695a0d6e6cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671625"
---
# <a name="resolvedelayloadsfromdll-function"></a>ResolveDelayLoadsFromDll función)

Reenvía el trabajo en la resolución de las importaciones de carga retrasada del archivo binario primario a un binario de destino.

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

*ParentBase* \[ de\]
</dt> <dd>

La dirección base del módulo que retrasa la carga otro binario.

</dd> <dt>

*TargetDllName* \[ de\]
</dt> <dd>

Nombre del archivo DLL de destino.

</dd> <dt>

*Marcas* 
</dt> <dd>

Sector debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La dirección del descriptor de carga retrasada, si se encuentra; de lo contrario, **es null**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad del vinculador con Delay-Loaded dll](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




