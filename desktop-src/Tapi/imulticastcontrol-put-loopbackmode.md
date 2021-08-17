---
description: Put \_ LoopbackMode establece el modo de bucle atrás de multidifusión.
ms.assetid: 38b28529-224f-4624-bb5e-22fee500e8e6
title: Método IMulticastControl::p ut_LoopbackMode (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d564fbfd3e5ea0db2c168b6207823945eceb148af17d78bed25cbc59bb4e5ee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140418"
---
# <a name="imulticastcontrolput_loopbackmode-method"></a>Método IMulticastControl::p ut \_ LoopbackMode

\[**put \_ LoopbackMode** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Put **\_ LoopbackMode establece** el modo de bucle atrás de multidifusión.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_LoopbackMode(
  [in] MULTICAST_LOOPBACK_MODE mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* \[ En\]
</dt> <dd>

[**MULTIDIFUSIÓN \_ Descriptor LOOPBACK \_ MODE**](multicast-loopback-mode.md) del nuevo modo de bucle atrás.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                  | Descripción                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | El método se realizó correctamente.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro mode* no es válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMulticastControl**](imulticastcontrol.md)
</dt> </dl>

 

 




