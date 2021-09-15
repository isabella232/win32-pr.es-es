---
title: Función DllDebugObjectRPCHook
description: Exportadas por archivos DLL COM para habilitar la depuración remota.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- Función COM de DllDebugObjectRPCHook
topic_type:
- apiref
api_name:
- DllDebugObjectRPCHook
api_location:
- ole32.dll
- API-MS-Win-Core-Com-private-l1-1-0.dll
- ComBase.dll
- API-MS-Win-Core-COM-Private-l1-1-1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62fffe6cc2d9ca650442d0a1c3fea2048fc6c84b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570025"
---
# <a name="dlldebugobjectrpchook-function"></a>Función DllDebugObjectRPCHook

Exportadas por archivos DLL COM para habilitar la depuración remota.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI DllDebugObjectRPCHook(
   BOOL             fTrace,
   LPORPC_INIT_ARGS lpOrpcInitArgs
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fTrace* 
</dt> <dd>

Si **es TRUE,** la depuración remota está habilitada. Si **es FALSE,** la depuración remota no está habilitada.

</dd> <dt>

*lpOrpcInitArgs* 
</dt> <dd>

Puntero a una [**estructura ORPC \_ INIT \_ ARGS.**](orpc-init-args.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**TRUE si** se realiza correctamente, **FALSE en caso** contrario

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Ole32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ole32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**BÚFER \_ DE DBG DE ORPC \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





