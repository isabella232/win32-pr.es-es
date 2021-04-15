---
title: Función MpManagerStatusQueryEx (MpClient. h)
description: Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de. | Función MpManagerStatusQueryEx (MpClient. h)
ms.assetid: 98088AB9-C7CF-46A1-B444-2C0EF882AA66
keywords:
- Función MpManagerStatusQueryEx características de entorno heredado de Windows
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
ms.openlocfilehash: ca541b5f1aff2e0ba03b88d69c451891c3a174bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689856"
---
# <a name="mpmanagerstatusqueryex-function"></a>MpManagerStatusQueryEx función)

Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de.

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

*hMpHandle* \[ de\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*dwFlag* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Controla qué información de consulta se devuelve. Algunos datos son caros y es posible que no sean necesarios.



| Value                                                                                                                                                                                                         | Significado                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="MP_STATUS_QUERY_FLAGS_NONE"></span><span id="mp_status_query_flags_none"></span><dl> <dt>**marcas de consulta de estado de MP \_ \_ \_ \_ ninguno**</dt> </dl>       | Predeterminada.<br/>                            |
| <span id="MP_STATUS_QUERY_FLAG_NOSTATE"></span><span id="mp_status_query_flag_nostate"></span><dl> <dt>**marca de consulta de estado de MP \_ \_ \_ \_ nostate**</dt> </dl> | No consulte la información de estado.<br/> |



 

</dd> <dt>

*pStatusInfo* \[ enuncia\]
</dt> <dd>

Tipo: **PMPSTATUS \_ info**

Puntero a una estructura que devuelve información de estado relativa a los últimos análisis, amenazas activas y distintos Estados de los componentes. Vea [**\_ información de MPSTATUS**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**. Se garantiza que esta llamada de función se realiza correctamente aunque no se esté ejecutando un servicio antimalware.

Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo. El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**información de MPSTATUS \_**](mpstatus-info.md)
</dt> </dl>

 

 





