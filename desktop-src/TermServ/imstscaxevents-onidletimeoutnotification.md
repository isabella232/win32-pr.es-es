---
title: Método IMsTscAxEvents OnIdleTimeoutNotification
description: Se llama cuando el usuario no ha realizado ninguna entrada de mouse o teclado durante el período de tiempo establecido por el método IMsRdpClientAdvancedSettings \_ put MinutesToIdleTimeout.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Método OnIdleTimeoutNotification Servicios de Escritorio remoto
- Método OnIdleTimeoutNotification Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnIdleTimeoutNotification
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnIdleTimeoutNotification
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356414d03a6b102f37f93205e0dbb8c3261cffbbb5b71a58cdb3f80acda09212
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120125125"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a>Método IMsTscAxEvents::OnIdleTimeoutNotification

Se llama cuando el usuario no ha realizado ninguna entrada de mouse o teclado durante el período de tiempo establecido por el método [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout.**](imsrdpclientadvancedsettings-minutestoidletimeout.md)

## <a name="syntax"></a>Sintaxis


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

De forma predeterminada, el valor de la propiedad [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) se establece en cero y el sistema no supervisa los tiempos de espera de inactividad. Este evento solo se produce si la propiedad está establecida en un valor distinto de cero.

El valor de [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) se restablece automáticamente cada vez que se produce el evento.

Las aplicaciones pueden [**usar MinutesToIdleTimeout en**](imsrdpclientadvancedsettings-minutestoidletimeout.md) situaciones en las que resulta útil desconectar a un usuario. por ejemplo, en un quiosco o en otro escenario de terminal público.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





