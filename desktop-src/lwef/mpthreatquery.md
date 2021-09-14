---
title: Función MpThreatQuery (MpClient.h)
description: Se usa para consultar información estática (como gravedad y categoría) o localizada (por ejemplo, descripción de categoría y consejos) sobre una amenaza determinada.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Función MpThreatQuery Características heredadas del Windows entorno
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168274"
---
# <a name="mpthreatquery-function"></a>Función MpThreatQuery

Se usa para consultar información estática (como gravedad y categoría) o localizada (por ejemplo, descripción de categoría y consejos) sobre una amenaza determinada.

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

*hMpHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Controle la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*ThreatID* \[ En\]
</dt> <dd>

Tipo: **Id. \_ de MPTHREAT**

Identificador de amenazas para el que se solicita información.

</dd> <dt>

*ppThreatInfo* \[ out\]
</dt> <dd>

Tipo: **PMPTHREAT \_ \* INFO**

Devuelve un puntero a una estructura de información de amenazas, [**MPTHREAT \_ INFO**](mpthreat-info.md). La estructura contiene información como el identificador de amenaza, el nombre y la gravedad.

</dd> <dt>

*ppThreatLocalizedInfo* \[ out, opcional\]
</dt> <dd>

Tipo: **PMPTHREAT \_ LOCALIZED \_ INFO \***

Devuelve un puntero a una estructura que contiene información localizada sobre la amenaza. Puede pasar **NULL si** no está interesado en la información localizada sobre la amenaza. Vea [**MPTHREAT LOCALIZED INFO ( \_ INFORMACIÓN \_ LOCALIZADA DE MPTHREAT).**](mpthreat-localized-info.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un **código HRESULT con** errores. El autor de la llamada puede usar [**la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

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

[**MpManagerAbrir**](mpmanageropen.md)
</dt> <dt>

[**INFORMACIÓN DE \_ MPTHREAT**](mpthreat-info.md)
</dt> <dt>

[**INFORMACIÓN LOCALIZADA DE MPTHREAT \_ \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





