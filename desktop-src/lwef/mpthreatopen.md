---
title: Función MpThreatOpen (MpClient.h)
description: Devuelve un identificador de enumeración para recuperar amenazas.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Función MpThreatOpen Características de entorno de Windows heredado
topic_type:
- apiref
api_name:
- MpThreatOpen
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca30435f9d7cba32771a2445d8a1156f0edaa9b1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168285"
---
# <a name="mpthreatopen-function"></a>Función MpThreatOpen

Devuelve un identificador de enumeración para recuperar amenazas. Esta función se puede usar para abrir las amenazas detectadas por un examen específico, todas las amenazas activas del sistema, el historial de la limpieza de amenazas o todas las amenazas presentes en la base de datos de firmas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpThreatOpen(
  _In_  MPHANDLE        hScanHandle,
  _In_  MPTHREAT_SOURCE ThreatSource,
  _In_  MPTHREAT_TYPE   ThreatType,
  _Out_ PMPHANDLE       phThreatEnumHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hScanHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Puede ser un identificador de una operación de examen completada, devuelta por la [**función MpScanStart.**](mpscanstart.md) Como alternativa, este parámetro se puede establecer en el identificador de interfaz del administrador de protección contra malware devuelto por [**MpManagerOpen**](mpmanageropen.md) para enumerar todas las amenazas activas del sistema, el historial de la limpieza de amenazas o las amenazas de la base de datos de firmas.

</dd> <dt>

*ThreatSource* \[ En\]
</dt> <dd>

Tipo: **MPTHREAT \_ SOURCE**

Se usa para controlar el origen de la enumeración de amenazas. Este parámetro admite los siguientes valores:



| Value                                                                                                                                                                                                 | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <dt>**MPTHREAT \_ SOURCE \_ SCAN**</dt> </dl>                   | Amenazas asociadas al identificador de examen específico.<br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <dt>**MPTHREAT \_ SOURCE \_ ACTIVE**</dt> </dl>             | Amenazas que están activas actualmente en el sistema.<br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <dt>**HISTORIAL DE ORIGEN DE \_ \_ MPTHREAT**</dt> </dl>          | Amenazas que se actúan y se conservan como un historial.<br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <dt>**CUARENTENA DE ORIGEN DE MPTHREAT \_ \_**</dt> </dl> | Amenazas que están en cuarentena.<br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <dt>**FIRMA DE ORIGEN \_ DE MPTHREAT \_**</dt> </dl>    | Amenazas que se pueden detectar con la base de datos de firma actual.<br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <dt>**ESTADO DE ORIGEN DE \_ \_ MPTHREAT**</dt> </dl>                | Amenazas sobre las que se ha actuado recientemente. ("Recently" se define mediante una configuración interna configurable).<br/> |



 

</dd> <dt>

*ThreatType* \[ En\]
</dt> <dd>

Tipo: **MPTHREAT \_ TYPE**

Se usa para filtrar las amenazas enumeradas en función del tipo de detección. Este parámetro admite los siguientes valores:



| Value                                                                                                                                                                                           | Significado                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <dt>**TIPO MPTHREAT \_ \_ KNOWNBAD**</dt> </dl>       | La detección se realiza en función de una firma, emulación u otro método de detección de amenazas específico.<br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <dt>**TIPO MPTHREAT \_ \_ SOSPECHOSO**</dt> </dl> | La detección se realiza en función de la supervisión del comportamiento.<br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <dt>**TIPO MPTHREAT \_ \_ DESCONOCIDO**</dt> </dl>          | La detección se realiza en función de amenazas desconocidas (sin clasificar).<br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <dt>**TIPO MPTHREAT \_ \_ KNOWNGOOD**</dt> </dl>    | La detección se realiza en función de las amenazas seguras conocidas.<br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <dt>**MPTHREAT \_ TYPE \_ NIS**</dt> </dl>                      | La detección se realiza en función de las amenazas de NIS.<br/>                                                       |



 

</dd> <dt>

*phThreatEnumHandle* \[ out\]
</dt> <dd>

Tipo: **PMPHANDLE**

Identificador de enumeración de amenazas devuelto que identifica el contexto de enumeración. Este identificador se puede usar para enumerar información sobre amenazas mediante [**MpThreatEnumerate**](mpthreatenumerate.md). El identificador debe cerrarse con la [**función MpHandleClose.**](mphandleclose.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**.

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

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerAbrir**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> </dl>

 

 





