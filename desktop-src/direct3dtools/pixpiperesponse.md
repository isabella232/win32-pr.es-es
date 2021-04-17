---
description: Enumeración que se usa para enviar las respuestas del motor de captura a Diagnóstico de gráficos.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración PixPipeResponse
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5BFEE25D-3E03-493E-AFEF-DD8C70C53FC5
api_name:
- PixPipeResponse
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 09ab253be5e02cc7329195016a406758b7a82e2b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105705209"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>Enumeración PixPipeResponse

Enumeración que se usa para enviar las respuestas del motor de captura a Diagnóstico de gráficos.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NUEVOS \_ datos \_ disponibles**  
Respuesta que indica que los nuevos datos se han escrito en el registro de gráficos y están listos para ser leídos.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**datos del experimento \_**  
Respuesta que indica la información de configuración sobre la sesión de captura.

<span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**  
Respuesta que indica que el motor de captura ha encontrado un error.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
Respuesta que indica que el motor de captura ha empezado A capturar información de gráficos. Esto no indica que los datos estén disponibles para ser examinados todavía.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**\_datos parciales**  
Respuesta que indica que los datos parciales se han escrito en el registro de gráficos.

<span id="READY"></span><span id="ready"></span>**Párese**  
Respuesta que indica que el motor de captura está listo para empezar a capturar información de gráficos.

<span id="DONE"></span><span id="done"></span>**VERTIR**  
Interno

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
Una respuesta que indica que se ha iniciado una captura de fotogramas.

<span id="STATUS"></span><span id="status"></span>**ESTATUS**  
Respuesta que indica la información de estado sobre la aplicación que se va a capturar. por ejemplo, velocidad de fotogramas.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine. h</td></tr></tbody></table>

 

 



