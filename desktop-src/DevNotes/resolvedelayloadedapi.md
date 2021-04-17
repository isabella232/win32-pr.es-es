---
description: Busca la función de destino de la importación especificada y reemplaza el puntero de función en el código thunk de importación con el destino de la implementación de función.
ms.assetid: 4ab79b7c-81d1-40bf-a76b-217d93567e40
title: ResolveDelayLoadedAPI función)
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
ms.openlocfilehash: 019729cacb45cce87de2cc4015c661c494125108
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671120"
---
# <a name="resolvedelayloadedapi-function"></a>ResolveDelayLoadedAPI función)

Busca la función de destino de la importación especificada y reemplaza el puntero de función en el código thunk de importación con el destino de la implementación de función.

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

*ParentModuleBase* \[ de\]
</dt> <dd>

La dirección de la base del módulo que importa una función de carga retrasada.

</dd> <dt>

*DelayloadDescriptor* \[ de\]
</dt> <dd>

Descriptor del módulo que se va a cargar.

</dd> <dt>

*FailureDllHook* \[ en, opcional\]
</dt> <dd>

Dirección del enlace de error. Vea [**DelayLoadFailureHook**](delayloadfailurehook.md).

</dd> <dt>

*FailureSystemHook* \[ en, opcional\]
</dt> <dd>

Dirección del enlace de error del sistema.

</dd> <dt>

*ThunkAddress* \[ enuncia\]
</dt> <dd>

Los datos de thunk de la función de destino. Se utiliza para buscar la entrada de la tabla de nombres específica de la función.

</dd> <dt>

*Marcas* 
</dt> <dd>

Sector debe ser 0.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La dirección de la importación o el código auxiliar de error correspondiente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Biblioteca<br/> | <dl> <dt>Kernel32.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Compatibilidad del vinculador con Delay-Loaded dll](https://msdn.microsoft.com/library/151kt790(v=VS.71).aspx)
</dt> </dl>

 

 




