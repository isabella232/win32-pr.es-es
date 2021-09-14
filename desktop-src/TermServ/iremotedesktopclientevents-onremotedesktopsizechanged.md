---
title: Método IRemoteDesktopClientEvents OnRemoteDesktopSizeChanged
description: Se llama cuando el tamaño del escritorio remoto ha cambiado.
ms.assetid: DA641CA7-3214-4DB6-9A7F-75903FE93DB4
ms.tgt_platform: multiple
keywords:
- Método OnRemoteDesktopSizeChanged Servicios de Escritorio remoto
- Método OnRemoteDesktopSizeChanged Servicios de Escritorio remoto interfaz , IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto método , OnRemoteDesktopSizeChanged
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnRemoteDesktopSizeChanged
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7431d1a6f41a6f87bb34fe1486c203168f2c3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073315"
---
# <a name="iremotedesktopclienteventsonremotedesktopsizechanged-method"></a>IRemoteDesktopClientEvents::OnRemoteDesktopSizeChanged (método)

Se llama cuando el tamaño del escritorio remoto ha cambiado.

## <a name="syntax"></a>Sintaxis


```C++
void OnRemoteDesktopSizeChanged(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*width* \[ En\]
</dt> <dd></dd> <dt>

*height* \[ En\]
</dt> <dd></dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





