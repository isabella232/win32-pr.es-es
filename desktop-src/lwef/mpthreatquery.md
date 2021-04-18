---
title: Función MpThreatQuery (MpClient. h)
description: Se usa para consultar información estática (como gravedad y categoría) o localizada (como descripción de la categoría y consejos) sobre una amenaza determinada.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Función MpThreatQuery características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665963"
---
# <a name="mpthreatquery-function"></a>MpThreatQuery función)

Se usa para consultar información estática (como gravedad y categoría) o localizada (como descripción de la categoría y consejos) sobre una amenaza determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMpHandle* \[ de\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*ThreatID* \[ de\]
</dt> <dd>

Tipo: **\_ ID. de MPTHREAT**

Identificador de amenaza para el que se solicita información.

</dd> <dt>

*ppThreatInfo* \[ enuncia\]
</dt> <dd>

Tipo: **PMPTHREAT \_ info \** _

Devuelve un puntero a una estructura de información de amenazas, [_ *MPTHREAT \_ info* *](mpthreat-info.md). La estructura contiene información como el identificador, el nombre y la gravedad de la amenaza.

</dd> <dt>

*ppThreatLocalizedInfo* \[ out, opcional\]
</dt> <dd>

Tipo: **PMPTHREAT \_ \_ información \* localizada* _

Devuelve un puntero a una estructura que contiene información localizada sobre la amenaza. Puede pasar _ *null** si no está interesado en información localizada sobre la amenaza. Consulte [**\_ \_ información localizada de MPTHREAT**](mpthreat-localized-info.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.

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

[**información de MPTHREAT \_**](mpthreat-info.md)
</dt> <dt>

[**\_información localizada de MPTHREAT \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





