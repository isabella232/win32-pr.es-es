---
title: Función MpManagerStatusQueryEx (MpClient.h)
description: Devuelve información de estado sobre varios componentes del administrador de protección contra malware. | Función MpManagerStatusQueryEx (MpClient.h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Función MpManagerStatusQueryEx Características heredadas del Windows entorno
topic_type:
- apiref
api_name:
- MpManagerStatusQueryEx
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8d7e3e6135a5f01691528480b760cfea422c78b9c032219f6e100da5ebd929d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961115"
---
# <a name="mpmanagerstatusqueryex-function"></a>Función MpManagerStatusQueryEx

Devuelve información de estado sobre varios componentes del administrador de protección contra malware.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpManagerStatusQueryEx(
  _In_  MPHANDLE       hMpHandle,
  _In_  DWORD          dwFlag,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMpHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*dwFlag* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Controla qué información de consulta se devuelve. Parte de la información es costosa y puede que no sea necesaria.



| Value                                                                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**MP \_ STATUS \_ QUERY \_ FLAGS \_ NONE**</dt> </dl>       | Predeterminada.<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**MARCA DE \_ CONSULTA DE ESTADO DE MP \_ \_ \_ NOSTATE**</dt> </dl> | No consulte la información de estado.<br/> |



 

</dd> <dt>

*pStatusInfo* \[ out\]
</dt> <dd>

Tipo: **PMPSTATUS \_ INFO**

Puntero a una estructura que devuelve información de estado relacionada con los últimos exámenes, las amenazas activas y el estado de varios componentes. Vea [**MPSTATUS \_ INFO**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**. Se garantiza que esta llamada de función se realiza correctamente incluso si no se está ejecutando un servicio AntiMalware.

Si se produce un error en la función, el valor devuelto es un **código HRESULT** con errores. El autor de la llamada puede [**usar la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerAbrir**](mpmanageropen.md)
</dt> <dt>

[**INFORMACIÓN \_ DE MPSTATUS**](mpstatus-info.md)
</dt> </dl>

 

 





