---
title: DllDebugObjectRPCHook función)
description: Exportado por DLL COM para habilitar la depuración remota.
ms.assetid: a0f8bf12-0889-452d-84d0-255c5c143bc1
keywords:
- DllDebugObjectRPCHook función COM
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714641"
---
# <a name="dlldebugobjectrpchook-function"></a>DllDebugObjectRPCHook función)

Exportado por DLL COM para habilitar la depuración remota.

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

Si es **true**, se habilita la depuración remota. Si es **false**, la depuración remota no está habilitada.

</dd> <dt>

*lpOrpcInitArgs* 
</dt> <dd>

Puntero a una estructura [**ORPC \_ init \_ args**](orpc-init-args.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

**True** si es correcto, **false** en caso contrario

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ole32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**\_búfer ORPC dbg \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ init \_ args**](orpc-init-args.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





