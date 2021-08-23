---
title: IOrpcDebugNotify ServerNotify (método)
description: Informa al servidor de una solicitud entrante del depurador del cliente.
ms.assetid: 6c868b9e-f25b-4d27-80ff-697d0c005b8d
keywords:
- Método COM serverNotify
- Método ServerNotify COM , IOrpcDebugNotify (interfaz)
- IOrpcDebugNotify (interfaz COM), Método ServerNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ServerNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cff0faac4ee4e5fa691088afa9de8871a8bf9382ce3da629b3fc14dd9d932ab8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048103"
---
# <a name="iorpcdebugnotifyservernotify-method"></a>IOrpcDebugNotify::ServerNotify (Método)

Informa al servidor de una solicitud entrante del depurador del cliente.

> [!Note]  
> Una biblioteca de importación que contiene la **función ServerNotify** no se incluye en el Kit de desarrollo de software (SDK) de Microsoft Windows. Una aplicación puede usar las funciones [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar un puntero de función a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll y proporcionar esta función a través de la interfaz [**IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

## <a name="syntax"></a>Sintaxis


```C++
void ServerNotify(
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

 

