---
title: Función MpManagerStatusQuery (MpClient. h)
description: Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de. | Función MpManagerStatusQuery (MpClient. h)
ms.assetid: E993FD8B-A35D-41C1-9522-1B9F0BC10B3D
keywords:
- Función MpManagerStatusQuery características de entorno heredado de Windows
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
ms.openlocfilehash: ad2e28bab1794b53695872310a3a7cf5d088f1a1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362049"
---
# <a name="mpmanagerstatusquery-function"></a>MpManagerStatusQuery función)

\[**MpManagerStatusQuery** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md).\]

Devuelve información de estado sobre los distintos componentes del administrador de protección contra malware de.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpManagerStatusQuery(
  _In_  MPHANDLE       hMpHandle,
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

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**información de MPSTATUS \_**](mpstatus-info.md)
</dt> </dl>

 

 





