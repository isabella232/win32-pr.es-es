---
description: El método \_ put TransportProtocol establece el protocolo de transporte.
ms.assetid: d2f74d4a-a65d-4829-ad17-7548ef06cfeb
title: ItMedia::p ut_TransportProtocol (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13c0806fcdc2e8a53c63cf9e00e74f16f63120fd1ea1d20962d49ecb91e2feff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867175"
---
# <a name="itmediaput_transportprotocol-method"></a>ItMedia::p ut \_ TransportProtocol (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método \_ put TransportProtocol** establece el protocolo de transporte. Esto se especifica además del formato multimedia para que el mismo formato multimedia estándar se pueda trasladar a través de distintos protocolos de transporte incluso cuando el protocolo de red sea el mismo, como con el audio PCM de Iva y el audio PCM RTP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_TransportProtocol(
  [in] BSTR pProtocol
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProtocol* \[ En\]
</dt> <dd>

Puntero a un **BSTR** que contiene el protocolo de transporte.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pProtocol* no es un puntero válido.<br/>    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysAllocString para**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) asignar memoria para el parámetro *pProtocol* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria cuando la variable ya no sea necesaria.

Esta función puede enviar datos a través de la conexión sin cifrar; por lo tanto, alguien que intercepta en la red puede leer los datos. El riesgo de seguridad de enviar los datos en texto sin formato debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::get \_ TransportProtocol**](itmedia-get-transportprotocol.md)
</dt> </dl>

 

