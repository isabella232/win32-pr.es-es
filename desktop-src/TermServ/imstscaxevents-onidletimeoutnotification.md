---
title: IMsTscAxEvents OnIdleTimeoutNotification, método
description: Se llama cuando el usuario no ha realizado ninguna entrada del mouse o del teclado durante el período de tiempo establecido por el \_ método IMsRdpClientAdvancedSettings Put MinutesToIdleTimeout.
ms.assetid: 303f23c9-3544-4e06-93f0-3aca35d29fb5
ms.tgt_platform: multiple
keywords:
- Método OnIdleTimeoutNotification Servicios de Escritorio remoto
- Método OnIdleTimeoutNotification Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnIdleTimeoutNotification
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
ms.openlocfilehash: 3e305b0ed22e733053e33451aa35d3b8f8d6c138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676819"
---
# <a name="imstscaxeventsonidletimeoutnotification-method"></a>IMsTscAxEvents:: OnIdleTimeoutNotification (método)

Se llama cuando el usuario no ha realizado ninguna entrada del mouse o del teclado durante el período de tiempo establecido por el método [**IMsRdpClientAdvancedSettings::p UT \_ MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) .

## <a name="syntax"></a>Sintaxis


```C++
void OnIdleTimeoutNotification();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

De forma predeterminada, el valor de la propiedad [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) se establece en cero y el sistema no supervisa los tiempos de espera de inactividad. Este evento solo se produce si la propiedad está establecida en un valor distinto de cero.

El valor de [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) se restablece automáticamente cada vez que se produce el evento.

Las aplicaciones pueden utilizar [**MinutesToIdleTimeout**](imsrdpclientadvancedsettings-minutestoidletimeout.md) en situaciones en las que resulta útil desconectar a un usuario. por ejemplo, en un escenario quiosco u otro terminal público.

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

 

 





