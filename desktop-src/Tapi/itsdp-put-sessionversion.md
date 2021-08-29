---
description: El método put \_ SessionVersion establece la versión de la sesión.
ms.assetid: 8984d608-0fad-4979-9c58-ac2fb7926796
title: Método ITSdp::p ut_SessionVersion (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f76ccf38b6d8df2a52b48777b49efbe2507b6be24dafd8c5f8874c45f0a9da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119405675"
---
# <a name="itsdpput_sessionversion-method"></a>ItSdp::p ut \_ SessionVersion

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método put \_ SessionVersion** establece la versión de la sesión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_SessionVersion(
  [in] DOUBLE SessionVersion
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SessionVersion* \[ En\]
</dt> <dd>

Valor de versión de la sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro SessionVersion* no es válido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

El valor devuelto de este método podría ser **ULONG,** Visual Basic no admite el **tipo ULONG.** Double **es** el siguiente tipo más pequeño que abarca todo el intervalo de valores necesarios.

Esta función puede enviar datos a través de la conexión en formato sin cifrar; por lo tanto, es posible que alguien interceptado en la red pueda leer los datos. El riesgo de seguridad de enviar los datos en texto no texto debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::get \_ SessionVersion**](itsdp-get-sessionversion.md)
</dt> </dl>

 

 




