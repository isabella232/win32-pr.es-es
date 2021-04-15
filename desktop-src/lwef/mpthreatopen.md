---
title: Función MpThreatOpen (MpClient. h)
description: Devuelve un identificador de enumeración con el fin de recuperar las amenazas.
ms.assetid: E1178F0C-E9C0-4532-AE9B-452770600DF2
keywords:
- Función MpThreatOpen características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665999"
---
# <a name="mpthreatopen-function"></a>MpThreatOpen función)

Devuelve un identificador de enumeración con el fin de recuperar las amenazas. Esta función se puede usar para abrir amenazas detectadas por un análisis específico, todas las amenazas activas del sistema, el historial de la desinfección de amenazas o todas las amenazas presentes en la base de datos de firmas.

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

*hScanHandle* \[ de\]
</dt> <dd>

Tipo: **MPHANDLE**

Puede ser un identificador de una operación de examen completada, devuelta por la función [**MpScanStart**](mpscanstart.md) . Como alternativa, este parámetro se puede establecer en el identificador de la interfaz del administrador de protección contra malware devuelto por [**MpManagerOpen**](mpmanageropen.md) para enumerar todas las amenazas activas del sistema, el historial de la desinfección de amenazas o las amenazas de la base de datos de firmas.

</dd> <dt>

*ThreatSource* \[ de\]
</dt> <dd>

Tipo: **MPTHREAT \_ source**

Se usa para controlar el origen de la enumeración de amenazas. Los valores posibles para este parámetro son:



| Value                                                                                                                                                                                                 | Significado                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_SOURCE_SCAN"></span><span id="mpthreat_source_scan"></span><dl> <dt>**\_examen de origen de MPTHREAT \_**</dt> </dl>                   | Amenazas asociadas al identificador de examen específico.<br/>                                              |
| <span id="MPTHREAT_SOURCE_ACTIVE"></span><span id="mpthreat_source_active"></span><dl> <dt>**origen de MPTHREAT \_ \_ activo**</dt> </dl>             | Amenazas que están activas actualmente en el sistema.<br/>                                                        |
| <span id="MPTHREAT_SOURCE_HISTORY"></span><span id="mpthreat_source_history"></span><dl> <dt>**\_historial de origen de MPTHREAT \_**</dt> </dl>          | Amenazas a las que se les actúa y se conserva como historial.<br/>                                                 |
| <span id="MPTHREAT_SOURCE_QUARANTINE"></span><span id="mpthreat_source_quarantine"></span><dl> <dt>**MPTHREAT \_ cuarentena de origen \_**</dt> </dl> | Amenazas que se ponen en cuarentena.<br/>                                                                           |
| <span id="MPTHREAT_SOURCE_SIGNATURE"></span><span id="mpthreat_source_signature"></span><dl> <dt>**\_firma de origen de MPTHREAT \_**</dt> </dl>    | Amenazas que se pueden detectar con la base de datos de firmas actual.<br/>                                |
| <span id="MPTHREAT_SOURCE_STATE"></span><span id="mpthreat_source_state"></span><dl> <dt>**\_Estado de origen de MPTHREAT \_**</dt> </dl>                | Amenazas que han actuado recientemente. ("Recientemente" se define mediante una configuración interna configurable).<br/> |



 

</dd> <dt>

*ThreatType* \[ de\]
</dt> <dd>

Tipo: **MPTHREAT \_ Type**

Se utiliza para filtrar amenazas enumeradas en función del tipo de detección. Los valores posibles para este parámetro son:



| Value                                                                                                                                                                                           | Significado                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span><dl> <dt>**MPTHREAT \_ Type \_ KNOWNBAD**</dt> </dl>       | La detección se realiza en función de una firma específica, emulación u otro método de detección de amenazas.<br/> |
| <span id="MPTHREAT_TYPE_SUSPICIOUS"></span><span id="mpthreat_type_suspicious"></span><dl> <dt>**tipo de MPTHREAT \_ \_ sospechoso**</dt> </dl> | La detección se realiza en función de la supervisión del comportamiento.<br/>                                               |
| <span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span><dl> <dt>**\_tipo MPTHREAT \_ desconocido**</dt> </dl>          | La detección se realiza en función de amenazas desconocidas (sin clasificar).<br/>                                    |
| <span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span><dl> <dt>**MPTHREAT \_ Type \_ KNOWNGOOD**</dt> </dl>    | La detección se realiza en función de amenazas seguras conocidas.<br/>                                                |
| <span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span><dl> <dt>**MPTHREAT \_ tipo \_ NIS**</dt> </dl>                      | La detección se realiza en función de las amenazas de NIS.<br/>                                                       |



 

</dd> <dt>

*phThreatEnumHandle* \[ enuncia\]
</dt> <dd>

Tipo: **PMPHANDLE**

Identificador de enumeración de amenazas devuelto que identifica el contexto de enumeración. Este identificador se puede usar para enumerar información de amenazas mediante [**MpThreatEnumerate**](mpthreatenumerate.md). El identificador debe cerrarse con la función [**MpHandleClose**](mphandleclose.md) .

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

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**MpScanStart**](mpscanstart.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> </dl>

 

 





