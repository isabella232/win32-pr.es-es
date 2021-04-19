---
title: Códigos de error de WER (Werapi. h)
description: En la tabla siguiente se proporciona una lista de códigos de error personalizados usados por Informe de errores de Windows.
ms.assetid: c409b222-5e02-4b48-b39a-f2e29d199944
topic_type:
- apiref
api_name:
- WER_E_INSUFFICIENT_BUFFER
- WER_E_INVALID_STATE
- WER_E_LENGTH_EXCEEDED
- WER_E_MISSING_PARAM
- WER_E_NOT_FOUND
- WER_E_STORE_DISABLED
api_location:
- Werapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cc4c37d21a38679f1ea36151eb14d21a6c43af0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695910"
---
# <a name="wer-error-codes"></a>Códigos de error de WER

En la tabla siguiente se proporciona una lista de códigos de error personalizados usados por Informe de errores de Windows.



| Constante                                                                                                                                                                                            | Descripción                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WER_E_INSUFFICIENT_BUFFER"></span><span id="wer_e_insufficient_buffer"></span><dl> <dt>**\_ \_ búfer insuficiente de Wer \_**</dt> </dl> | Un búfer es demasiado pequeño para contener los datos.<br/>      |
| <span id="WER_E_INVALID_STATE"></span><span id="wer_e_invalid_state"></span><dl> <dt>**\_ \_ Estado no válido de Wer E \_**</dt> </dl>                   | Se llamó a una función de forma no compatible.<br/> |
| <span id="WER_E_LENGTH_EXCEEDED"></span><span id="wer_e_length_exceeded"></span><dl> <dt>**\_ \_ longitud \_ superada de Wer E**</dt> </dl>             | Se ha superado uno de los límites de longitud.<br/>     |
| <span id="WER_E_MISSING_PARAM"></span><span id="wer_e_missing_param"></span><dl> <dt>**falta el parámetro de WER \_ E \_ \_**</dt> </dl>                   | Faltan uno o varios parámetros.<br/>             |
| <span id="WER_E_NOT_FOUND"></span><span id="wer_e_not_found"></span><dl> <dt>**WER \_ E \_ no \_ encontrado**</dt> </dl>                               | Elemento no encontrado.<br/>                              |
| <span id="WER_E_STORE_DISABLED"></span><span id="wer_e_store_disabled"></span><dl> <dt>**almacén de WER \_ E \_ \_ deshabilitado**</dt> </dl>                | Se ha deshabilitado el almacén.<br/>                    |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Werapi. h</dt> </dl> |



 

 





