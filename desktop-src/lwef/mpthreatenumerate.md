---
title: Función MpThreatEnumerate (MpClient. h)
description: Devuelve información sobre la siguiente amenaza en la lista de enumeración. Se puede llamar a esta función varias veces hasta que se complete la enumeración de todas las amenazas.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Función MpThreatEnumerate características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996759"
---
# <a name="mpthreatenumerate-function"></a>MpThreatEnumerate función)

Devuelve información sobre la siguiente amenaza en la lista de enumeración. Se puede llamar a esta función varias veces hasta que se complete la enumeración de todas las amenazas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hThreatEnumHandle* \[ de\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de un contexto de enumeración de amenazas devuelto por [**MpThreatOpen**](mpthreatopen.md).

</dd> <dt>

*ppThreatInfo* \[ enuncia\]
</dt> <dd>

Tipo: **PMPTHREAT \_ info \** _

Devuelve un puntero a una estructura de información de amenazas, [_ *MPTHREAT \_ info* *](mpthreat-info.md). La estructura contiene información como el identificador, el nombre y la gravedad de la amenaza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.

Si no hay más elementos para devolver, el valor devuelto es **S \_ false**.

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

[**MpThreatOpen**](mpthreatopen.md)
</dt> <dt>

[**información de MPTHREAT \_**](mpthreat-info.md)
</dt> </dl>

 

 





