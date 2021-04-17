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
# <a name="span-idvspixenginepixpiperesponsespanpixpiperesponse-enumeration"></a><span data-ttu-id="9a0e9-103"><span id="vspixengine.pixpiperesponse"></span>Enumeración PixPipeResponse</span><span class="sxs-lookup"><span data-stu-id="9a0e9-103"><span id="vspixengine.pixpiperesponse"></span>PixPipeResponse enumeration</span></span>

<span data-ttu-id="9a0e9-104">Enumeración que se usa para enviar las respuestas del motor de captura a Diagnóstico de gráficos.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-104">An enum used to send responses from the capture engine to Graphics Diagnostics.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a0e9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9a0e9-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="9a0e9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="9a0e9-106">Constants</span></span>

<span data-ttu-id="9a0e9-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NUEVOS \_ datos \_ disponibles**</span><span class="sxs-lookup"><span data-stu-id="9a0e9-107"><span id="NEW_DATA_AVAILABLE"></span><span id="new_data_available"></span>**NEW\_DATA\_AVAILABLE**</span></span>  
<span data-ttu-id="9a0e9-108">Respuesta que indica que los nuevos datos se han escrito en el registro de gráficos y están listos para ser leídos.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-108">A response which indicates that new data has been written to the graphics log and is ready to be read.</span></span>

<span data-ttu-id="9a0e9-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**datos del experimento \_**</span><span class="sxs-lookup"><span data-stu-id="9a0e9-109"><span id="EXPERIMENT_DATA"></span><span id="experiment_data"></span>**EXPERIMENT\_DATA**</span></span>  
<span data-ttu-id="9a0e9-110">Respuesta que indica la información de configuración sobre la sesión de captura.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-110">A response which indicates configuration information about the capture session.</span></span>

<span data-ttu-id="9a0e9-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span><span class="sxs-lookup"><span data-stu-id="9a0e9-111"><span id="ERRORCODE"></span><span id="errorcode"></span>**ERRORCODE**</span></span>  
<span data-ttu-id="9a0e9-112">Respuesta que indica que el motor de captura ha encontrado un error.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-112">A response which indicates that the capture engine has encountered an error.</span></span>

<span data-ttu-id="9a0e9-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span><span class="sxs-lookup"><span data-stu-id="9a0e9-113"><span id="APPLICATIONCAPTUREINPROGRESS"></span><span id="applicationcaptureinprogress"></span>**APPLICATIONCAPTUREINPROGRESS**</span></span>  
<span data-ttu-id="9a0e9-114">Respuesta que indica que el motor de captura ha empezado A capturar información de gráficos.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-114">A response which indicates that the capture engine has started capturing graphics information.</span></span> <span data-ttu-id="9a0e9-115">Esto no indica que los datos estén disponibles para ser examinados todavía.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-115">This does not indicate that data is available to be examined yet.</span></span>

<span data-ttu-id="9a0e9-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**\_datos parciales**</span><span class="sxs-lookup"><span data-stu-id="9a0e9-116"><span id="PARTIAL_DATA"></span><span id="partial_data"></span>**PARTIAL\_DATA**</span></span>  
<span data-ttu-id="9a0e9-117">Respuesta que indica que los datos parciales se han escrito en el registro de gráficos.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-117">A response which indicates that partial data has been written to the graphics log.</span></span>

<span data-ttu-id="9a0e9-118"><span id="READY"></span><span id="ready"></span>**Párese**</span><span class="sxs-lookup"><span data-stu-id="9a0e9-118"><span id="READY"></span><span id="ready"></span>**READY**</span></span>  
<span data-ttu-id="9a0e9-119">Respuesta que indica que el motor de captura está listo para empezar a capturar información de gráficos.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-119">A response which indicates that the capture engine is ready to start capturing graphics information.</span></span>

<span data-ttu-id="9a0e9-120"><span id="DONE"></span><span id="done"></span>**VERTIR**</span><span class="sxs-lookup"><span data-stu-id="9a0e9-120"><span id="DONE"></span><span id="done"></span>**DONE**</span></span>  
<span data-ttu-id="9a0e9-121">Interno</span><span class="sxs-lookup"><span data-stu-id="9a0e9-121">Internal</span></span>

<span data-ttu-id="9a0e9-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span><span class="sxs-lookup"><span data-stu-id="9a0e9-122"><span id="CAPTURESTARTED"></span><span id="capturestarted"></span>**CAPTURESTARTED**</span></span>  
<span data-ttu-id="9a0e9-123">Una respuesta que indica que se ha iniciado una captura de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-123">A response which indicates that a frame capture has started.</span></span>

<span data-ttu-id="9a0e9-124"><span id="STATUS"></span><span id="status"></span>**ESTATUS**</span><span class="sxs-lookup"><span data-stu-id="9a0e9-124"><span id="STATUS"></span><span id="status"></span>**STATUS**</span></span>  
<span data-ttu-id="9a0e9-125">Respuesta que indica la información de estado sobre la aplicación que se va a capturar. por ejemplo, velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9a0e9-125">A response which indicates status information about the app being captured; for example, framerate.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0e9-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a0e9-126">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="9a0e9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a0e9-127">Header</span></span></p></td><td><span data-ttu-id="9a0e9-128">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="9a0e9-128">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



