---
description: El \_ método startTime Put establece el valor de hora de inicio de 32 bits NTP (Protocolo de tiempo de red). La sesión se considera activa desde este momento.
ms.assetid: c7c96265-4588-4f05-83b6-6ef54f02650b
title: 'ITTime: método de ut_StartTime de:p (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5b574f7c90d7cc2f92204e3a045b33e6fb8480
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679374"
---
# <a name="ittimeput_starttime-method"></a>ITTime::p \_ método startTime de UT

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El **método \_ startTime Put** establece el valor de hora de inicio de 32 bits NTP (Protocolo de tiempo de red). La sesión se considera activa desde este momento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_StartTime(
  [in] DOUBLE Time
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Hora* \[ de de\]
</dt> <dd>

Hora de inicio de la sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *Tim* e no es válido.<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Esta función puede enviar datos a través de la conexión en formato no cifrado. por lo tanto, es posible que alguien que escucha en la red pueda leer los datos. El riesgo de seguridad de enviar los datos en texto no cifrado debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITTime**](ittime.md)
</dt> <dt>

[**ITTime:: get \_ startTime**](ittime-get-starttime.md)
</dt> </dl>

 

 




