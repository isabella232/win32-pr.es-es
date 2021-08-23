---
description: Busca la función de destino de la importación especificada y reemplaza el puntero de función en el elemento thunk de importación por el destino de la implementación de la función.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: Función ResolveDelayLoadedAPI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ResolveDelayLoadedAPI
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-DelayLoad-l1-1-1.dll
- kernelbase.dll
- mincoredload.dll
- minkernelbase.dll
ms.openlocfilehash: 359de5c52417f09c35e2fc994e36f0efd054f2a18dc3063be71dc12d588c60e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571555"
---
# <a name="resolvedelayloadedapi-function"></a>Función ResolveDelayLoadedAPI

Busca la función de destino de la importación especificada y reemplaza el puntero de función en el elemento thunk de importación por el destino de la implementación de la función.

## <a name="syntax"></a>Sintaxis


```C++
PVOID WINAPI ResolveDelayLoadedAPI(
  _In_       PVOID                             ParentModuleBase,
  _In_       PCIMAGE_DELAYLOAD_DESCRIPTOR      DelayloadDescriptor,
  _In_opt_   PDELAYLOAD_FAILURE_DLL_CALLBACK   FailureDllHook,
  _In_opt_   PDELAYLOAD_FAILURE_SYSTEM_ROUTINE FailureSystemHook,
  _Out_      PIMAGE_THUNK_DATA                 ThunkAddress,
  _Reserved_ ULONG                             Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ParentModuleBase* \[ En\]
</dt> <dd>

Dirección de la base del módulo que importa una función de carga retrasada.

</dd> <dt>

*DelayloadDescriptor* \[ En\]
</dt> <dd>

Descriptor del módulo que se va a cargar.

</dd> <dt>

*FailureDllHook* \[ in, opcional\]
</dt> <dd>

Dirección del enlace de error. Consulte [**DelayLoadFailureHook.**](delayloadfailurehook.md)

</dd> <dt>

*FailureSystemHook* \[ in, opcional\]
</dt> <dd>

Dirección del enlace de error del sistema.

</dd> <dt>

*ThunkAddress* \[ out\]
</dt> <dd>

Los datos thunk de la función de destino. Se usa para buscar la entrada de tabla de nombres específica de la función.

</dd> <dt>

*Marcas* 
</dt> <dd>

Reservado; debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La dirección de la importación o el código auxiliar de error para ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad del vinculador con Delay-Loaded dll](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




