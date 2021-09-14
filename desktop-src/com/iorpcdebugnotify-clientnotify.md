---
title: IOrpcDebugNotify ClientNotify (método)
description: Informa al cliente de una solicitud del depurador saliente al servidor.
ms.assetid: a41e3eaa-6d1f-46bf-9103-f83e45b2cd90
keywords:
- Método Com de ClientNotify
- Método ClientNotify COM , IOrpcDebugNotify (interfaz)
- IOrpcDebugNotify (interfaz COM), método ClientNotify
topic_type:
- apiref
api_name:
- IOrpcDebugNotify.ClientNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e788a51e278df09715aaf9d4993ac5724ed65b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126889097"
---
# <a name="iorpcdebugnotifyclientnotify-method"></a>IOrpcDebugNotify::ClientNotify (Método)

Informa al cliente de una solicitud del depurador saliente al servidor.

> [!Note]  
> Una biblioteca de importación que contiene la **función ClientNotify** no se incluye en el Kit de desarrollo de software (SDK) de Microsoft Windows. Una aplicación puede usar las funciones [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) y [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar un puntero de función a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) desde oleaut.dll y proporcionar esta función a través de la [**interfaz IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

## <a name="syntax"></a>Sintaxis


```C++
void ClientNotify(
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
| IDL<br/>                      | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

