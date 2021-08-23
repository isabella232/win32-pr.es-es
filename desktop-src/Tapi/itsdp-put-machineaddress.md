---
description: El método put \_ MachineAddress establece la dirección del equipo del host de origen.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: Método ITSdp::p ut_MachineAddress (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974286e846268686423d0ebdbbd083d07e9946401cb0192713b200b2354b89c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060803"
---
# <a name="itsdpput_machineaddress-method"></a>ItSdp::p ut \_ MachineAddress

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método put \_ MachineAddress** establece la dirección del equipo del host de origen.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMachineAddress* \[ En\]
</dt> <dd>

Puntero a un **BSTR** que contiene la dirección del equipo del host de conferencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                       |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pMachineAddress* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>    |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                      |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                     |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysAllocString para**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) asignar memoria para el parámetro *pMachineAddress* y usar [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria cuando la variable ya no sea necesaria.

El *parámetro pMachineAddress* puede ser un nombre DNS ("JohnSmith.workinghard.microsoft.com") o una dirección IP ("10.111.222.111").

Esta función puede enviar datos a través de la conexión en formato sin cifrar; por lo tanto, es posible que alguien interceptado en la red pueda leer los datos. El riesgo de seguridad de enviar los datos en texto no texto debe tenerse en cuenta antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITSdp::get \_ MachineAddress**](itsdp-get-machineaddress.md)
</dt> </dl>

 

