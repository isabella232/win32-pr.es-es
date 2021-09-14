---
title: Función MpThreatEnumerate (MpClient.h)
description: Devuelve información sobre la siguiente amenaza en la lista de enumeración. Se puede llamar a esta función repetidamente hasta que se complete la enumeración de todas las amenazas.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Función MpThreatEnumerate Legacy Windows Environment Features
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168289"
---
# <a name="mpthreatenumerate-function"></a>Función MpThreatEnumerate

Devuelve información sobre la siguiente amenaza en la lista de enumeración. Se puede llamar a esta función repetidamente hasta que se complete la enumeración de todas las amenazas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hThreatEnumHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de un contexto de enumeración de amenazas devuelto [**por MpThreatOpen**](mpthreatopen.md).

</dd> <dt>

*ppThreatInfo* \[ out\]
</dt> <dd>

Tipo: **PMPTHREAT \_ \* INFO**

Devuelve un puntero a una estructura de información de amenazas, [**MPTHREAT \_ INFO**](mpthreat-info.md). La estructura contiene información como el identificador de amenaza, el nombre y la gravedad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**.

Si no hay más elementos para devolver el valor devuelto es **S \_ FALSE.**

Si se produce un error en la función, el valor devuelto es un **código HRESULT** con errores. El autor de la llamada puede [**usar la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpThreatOpen**](mpthreatopen.md)
</dt> <dt>

[**INFORMACIÓN DE \_ MPTHREAT**](mpthreat-info.md)
</dt> </dl>

 

 





