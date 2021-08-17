---
description: Enumeración que se usa para enviar respuestas desde el motor de captura a Diagnóstico de gráficos.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración DePipeResponse
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
ms.openlocfilehash: b28971a4a4011422fae5f37c11b4d8fc665cce7c0989842ab81dda027777c253
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119269"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>Enumeración DePipeResponse

Enumeración que se usa para enviar respuestas desde el motor de captura a Diagnóstico de gráficos.

## <a name="syntax"></a>Syntax


```C++
};
```

## <a name="constants"></a>Constantes

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NUEVOS \_ DATOS \_ DISPONIBLES**  
Respuesta que indica que se han escrito nuevos datos en el registro de gráficos y está listo para leerse.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**DATOS DEL \_ EXPERIMENTO**  
Respuesta que indica información de configuración sobre la sesión de captura.

<span id="ERRORCODE"></span><span id="errorcode"></span>**CÓDIGO DE ERROR**  
Respuesta que indica que el motor de captura ha encontrado un error.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
Respuesta que indica que el motor de captura ha empezado a capturar información de gráficos. Esto no indica que los datos estén disponibles para examinarse todavía.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**DATOS \_ PARCIALES**  
Respuesta que indica que se han escrito datos parciales en el registro de gráficos.

<span id="READY"></span><span id="ready"></span>**Listo**  
Respuesta que indica que el motor de captura está listo para empezar a capturar información de gráficos.

<span id="DONE"></span><span id="done"></span>**Hecho**  
Interno

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
Respuesta que indica que se ha iniciado una captura de fotogramas.

<span id="STATUS"></span><span id="status"></span>**Estado**  
Respuesta que indica la información de estado sobre la aplicación que se está capturando. por ejemplo, velocidad de fotogramas.

## <a name="requirements"></a>Requisitos

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Header</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



