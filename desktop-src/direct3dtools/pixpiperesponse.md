---
description: Enumeración que se usa para enviar respuestas desde el motor de captura a Diagnóstico de gráficos.
MS-HAID: vspixengine.PixPipeResponse
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumeración PixelPipeResponse
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
ms.openlocfilehash: ad00d7bada935dd27f711499e5975d31709b9940
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631693"
---
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span id="vspixengine.pixpiperesponse"></span>Enumeración PixelPipeResponse

Enumeración que se usa para enviar respuestas desde el motor de captura a Diagnóstico de gráficos.

## <a name="syntax"></a>Sintaxis


```C++
};
```

## <a name="constants"></a>Constantes

<span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NUEVOS \_ DATOS \_ DISPONIBLES**  
Respuesta que indica que se han escrito nuevos datos en el registro de gráficos y está listo para leerse.

<span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**DATOS DE \_ EXPERIMENTO**  
Respuesta que indica información de configuración sobre la sesión de captura.

<span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**  
Respuesta que indica que el motor de captura ha encontrado un error.

<span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**  
Respuesta que indica que el motor de captura ha empezado a capturar información de gráficos. Esto no indica que los datos estén disponibles para examinarse todavía.

<span id="PARTIAL_DATA"></span><span id="partial_data"></span>**DATOS \_ PARCIALES**  
Respuesta que indica que se han escrito datos parciales en el registro de gráficos.

<span id="READY"></span><span id="ready"></span>**LISTO**  
Respuesta que indica que el motor de captura está listo para empezar a capturar información de gráficos.

<span id="DONE"></span><span id="done"></span>**HECHO**  
Interno

<span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**  
Respuesta que indica que se ha iniciado una captura de fotogramas.

<span id="STATUS"></span><span id="status"></span>**ESTADO**  
Respuesta que indica la información de estado sobre la aplicación que se captura. por ejemplo, velocidad de fotogramas.

## <a name="requirements"></a>Requisitos

<table><colgroup><col  /><col  /></colgroup><tbody><tr class="odd"><td><p>Encabezado</p></td><td>Vspixengine.h</td></tr></tbody></table>

 

 



