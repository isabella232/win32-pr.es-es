---
title: IOrpcDebugNotify ClientGetBufferSize (método)
description: Recupera el tamaño del búfer RPC del depurador del lado cliente.
ms.assetid: 05475156-1508-4eb2-82a6-bb1701839fbd
keywords:
- Método COM clientGetBufferSize
- Método ClientGetBufferSize COM , IOrpcDebugNotify (interfaz)
- IOrpcDebugNotify (interfaz COM), método ClientGetBufferSize
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientGetBufferSize
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 038273dfd93264d483bacb314b78e33f3e8f16cef4f120be27bd48901ef5b060
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859475"
---
# <a name="iorpcdebugnotifyclientgetbuffersize-method"></a>IOrpcDebugNotify::ClientGetBufferSize (método)

Recupera el tamaño del búfer RPC del depurador del lado cliente.

> [!Note]  
> Una biblioteca de importación que contiene la **función ClientGetBufferSize** no se incluye en el Kit de desarrollo de software (SDK) de Microsoft Windows. Una aplicación puede usar las funciones [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar un puntero de función a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll y proporcionar esta función a través de la interfaz [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

## <a name="syntax"></a>Sintaxis


```C++
void ClientGetBufferSize(
   ORPC_DBG_ALL *lpOrpcDebugAll
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpOrpcDebugAll* 
</dt> <dd>

Puntero a una estructura [**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md) que contiene información específica de notificación que el sistema RPC COM pasa al depurador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                           |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl> |
| Idl<br/>                      | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ARGUMENTOS \_ DE ORPC INIT \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

