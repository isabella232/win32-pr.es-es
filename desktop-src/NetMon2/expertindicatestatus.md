---
description: La función ExpertIndicateStatus indica el porcentaje de finalización del análisis de expertos del archivo de captura.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Función ExpertIndicateStatus (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153865"
---
# <a name="expertindicatestatus-function"></a>ExpertIndicateStatus función)

La función **ExpertIndicateStatus** indica el porcentaje de finalización del análisis del experto en el archivo de captura.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hExpertKey* \[ de\]
</dt> <dd>

Identificador de experto único. Monitor de red pasa *hExpertKey* al experto cuando llama a la función [Run](run.md) .

</dd> <dt>

*Estado* \[ de de\]
</dt> <dd>

Estado actual del análisis. Especifique uno de los siguientes valores de [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) .



| Value                                                                                                                                                                                 | Significado                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**EXPERTSTATUS \_ INactivo**</dt> </dl> | El experto nunca comenzó. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**Inicio de EXPERTSTATUS \_**</dt> </dl> | Se está iniciando el experto. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**EXPERTSTATUS en \_ ejecución**</dt> </dl>    | El experto se ejecuta con normalidad. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**problema de EXPERTSTATUS \_**</dt> </dl>    | Un problema especificado en el parámetro substatus detuvo el experto. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**EXPERTSTATUS \_ anulado**</dt> </dl>    | Monitor de red detuvo el experto. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**EXPERTSTATUS \_ completado**</dt> </dl>             | El experto ha finalizado el análisis correctamente. <br/>                     |



 

</dd> <dt>

*Subestado* \[ de\]
</dt> <dd>

Extensión o aclaración de la información proporcionada por el parámetro *status* .

</dd> <dt>

*szText* \[ de\]
</dt> <dd>

Indicador de estado de texto opcional.

Este valor de parámetro puede ser **null**.

</dd> <dt>

*PercentDone* \[ enuncia\]
</dt> <dd>

Porcentaje de los datos de captura que ha procesado el experto.

Cuando el experto completa correctamente el análisis de un archivo de captura, el sistema establece el porcentaje en 100. Se omitirá cualquier número mayor que 99.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es NMERR \_ Expert \_ Terminate; el experto debe limpiar y volver inmediatamente sin completar la captura.

## <a name="remarks"></a>Observaciones

La función **ExpertIndicateStatus** solo puede ser llamada por expertos que implementan la función de exportación [Ejecutar](run.md) o [configurar](configure.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
