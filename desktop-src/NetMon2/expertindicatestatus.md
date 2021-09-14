---
description: La función ExpertIndicateStatus indica el porcentaje de finalización del análisis de expertos del archivo de captura.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Función ExpertIndicateStatus (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069344"
---
# <a name="expertindicatestatus-function"></a>Función ExpertIndicateStatus

La **función ExpertIndicateStatus** indica el porcentaje de finalización del análisis del experto del archivo de captura.

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

*hExpertKey* \[ En\]
</dt> <dd>

Identificador experto único. Monitor de red pasa *hE expert al* experto cuando llama a la [función Run.](run.md)

</dd> <dt>

*Estado* \[ En\]
</dt> <dd>

Estado actual del análisis. Especifique uno de los [siguientes valores DE EXPERTSTATUSENUMERATION.](expertstatusenumeration.md)



| Value                                                                                                                                                                                 | Significado                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <dt>**EXPERTSTATUS \_ INACTIVE**</dt> </dl> | El experto nunca empezó. <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <dt>**INICIO \_ DE EXPERTSTATUS**</dt> </dl> | El experto se está iniciando. <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <dt>**EJECUCIÓN \_ DE EXPERTSTATUS**</dt> </dl>    | El experto se ejecuta con normalidad. <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <dt>**PROBLEMA \_ DE EXPERTSTATUS**</dt> </dl>    | Un problema especificado en el parámetro SubStatus detuvo al experto. <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <dt>**EXPERTSTATUS \_ ABORTED**</dt> </dl>    | Monitor de red detuvo al experto. <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <dt>**EXPERTSTATUS \_ DONE**</dt> </dl>             | El experto finalizó el análisis correctamente. <br/>                     |



 

</dd> <dt>

*SubStatus* \[ En\]
</dt> <dd>

Extensión o aclaración de la información proporcionada por el *parámetro Status.*

</dd> <dt>

*sztext* \[ En\]
</dt> <dd>

Indicador de estado de texto opcional.

Este valor de parámetro puede ser **NULL.**

</dd> <dt>

*PercentDone* \[ out\]
</dt> <dd>

Porcentaje de los datos de captura que el experto ha procesado.

Cuando el experto completa correctamente el análisis de un archivo de captura, el sistema establece el porcentaje en 100. Se omitirá cualquier número mayor que 99.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es NMERR EXPERT TERMINATE; el experto debe limpiar y devolver inmediatamente sin \_ \_ completar la captura.

## <a name="remarks"></a>Observaciones

La **función ExpertIndicateStatus** solo puede ser llamada por expertos que implementan la [función de](run.md) exportación Ejecutar [o](configure.md) configurar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |
