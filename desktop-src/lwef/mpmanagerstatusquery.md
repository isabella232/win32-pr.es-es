---
title: Función MpManagerStatusQuery (MpClient.h)
description: Devuelve información de estado sobre varios componentes del administrador de protección contra malware. | Función MpManagerStatusQuery (MpClient.h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Función MpManagerStatusQuery Características heredadas del Windows entorno
topic_type:
- apiref
api_name:
- MpManagerStatusQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d05751f30e1579ef8b12e31a4f858469b1c997cf9c29d7643c0600a133840fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883380"
---
# <a name="mpmanagerstatusquery-function"></a>Función MpManagerStatusQuery

\[**MpManagerStatusQuery** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, [**use MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]

Devuelve información de estado sobre varios componentes del administrador de protección contra malware.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
  _Out_ PMPSTATUS_INFO pStatusInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMpHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Controle la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*pStatusInfo* \[ out\]
</dt> <dd>

Tipo: **PMPSTATUS \_ INFO**

Puntero a una estructura que devuelve información de estado relacionada con los últimos exámenes, las amenazas activas y el estado de varios componentes. Vea [**MPSTATUS \_ INFO**](mpstatus-info.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**. Se garantiza que esta llamada de función se realiza correctamente incluso si no se está ejecutando un servicio AntiMalware.

Si se produce un error en la función, el valor devuelto es un **código HRESULT con** errores. El autor de la llamada puede usar [**la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpManagerAbrir**](mpmanageropen.md)
</dt> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**INFORMACIÓN \_ DE MPSTATUS**](mpstatus-info.md)
</dt> </dl>

 

 





