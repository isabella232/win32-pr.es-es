---
description: Emisión de comandos AV/C sin formato
ms.assetid: 18081652-962f-4605-84b7-1fa60f61ad05
title: Emisión de comandos AV/C sin formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf1cf1b25d45a0eb35ede7151941d0cd49d30db0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422844"
---
# <a name="issuing-raw-avc-commands"></a><span data-ttu-id="5a9d7-103">Emisión de comandos AV/C sin formato</span><span class="sxs-lookup"><span data-stu-id="5a9d7-103">Issuing Raw AV/C Commands</span></span>

<span data-ttu-id="5a9d7-104">Las interfaces [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)y [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) funcionan mediante la traducción de las llamadas de método en comandos para el controlador y, a continuación, la interpretación de la respuesta del controlador y su devolución a través de un **valor HRESULT** o un parámetro de salida.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-104">The [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice), [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport), and [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) interfaces work by translating the method calls into commands for the driver, then interpreting the driver's response and returning it through an **HRESULT** or an output parameter.</span></span> <span data-ttu-id="5a9d7-105">Sin embargo, es posible que algunas funciones del dispositivo no sean accesibles a través de estos métodos.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-105">However, some device functions may not be accessible through these methods.</span></span> <span data-ttu-id="5a9d7-106">Por lo tanto, MSDV admite el envío de comandos AV/C sin formato al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-106">Therefore, MSDV supports sending raw AV/C commands to the device.</span></span>

<span data-ttu-id="5a9d7-107">Debe tener en cuenta los siguientes puntos al usar esta característica:</span><span class="sxs-lookup"><span data-stu-id="5a9d7-107">You should keep the following points in mind when using this feature:</span></span>

-   <span data-ttu-id="5a9d7-108">El comando se pasa directamente al dispositivo, sin comprobación de errores o validación de parámetros.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-108">The command is passed directly to the device, with no error checking or parameter validation.</span></span> <span data-ttu-id="5a9d7-109">Por esta razón, debe emitir comandos AV/C sin procesar solo cuando las interfaces de DirectShow no implementan la funcionalidad que necesita.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-109">For this reason, you should issue raw AV/C commands only when the DirectShow interfaces do not implement the functionality you need.</span></span>
-   <span data-ttu-id="5a9d7-110">Todos los comandos AV/C sin procesar son sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-110">All raw AV/C commands are synchronous.</span></span> <span data-ttu-id="5a9d7-111">El subproceso que emite el comando se bloquea hasta que el comando devuelve.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-111">The thread issuing the command blocks until the command returns.</span></span>
-   <span data-ttu-id="5a9d7-112">Solo se puede proporcionar un comando cada vez.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-112">Only one command can be given at a time.</span></span> <span data-ttu-id="5a9d7-113">Mientras se está procesando el comando, el dispositivo rechazará los comandos adicionales.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-113">While the command is being processed, the device will reject any additional commands.</span></span>
-   <span data-ttu-id="5a9d7-114">El controlador UVC no admite comandos AV/C sin formato.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-114">The UVC driver does not support raw AV/C commands.</span></span>

<span data-ttu-id="5a9d7-115">Para enviar un comando AV/C, formatee el comando como una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-115">To send an AV/C command, format the command as an array of bytes.</span></span> <span data-ttu-id="5a9d7-116">Después, llame a [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span><span class="sxs-lookup"><span data-stu-id="5a9d7-116">Then call [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters).</span></span> <span data-ttu-id="5a9d7-117">Pase la marca ED \_ raw \_ ext \_ dev \_ cmd, el tamaño de la matriz y la matriz.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-117">Pass in the ED\_RAW\_EXT\_DEV\_CMD flag, the array size, and the array.</span></span> <span data-ttu-id="5a9d7-118">Debe convertir la dirección de matriz en un tipo \*\* \* LPOLESTR\* _, porque el propósito original de este parámetro era devolver un valor de cadena.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-118">You must cast the array address to an \**LPOLESTR\** _ type, because the original purpose of this parameter was to return a string value.</span></span>


```C++
BYTE AvcCmd[] = { ... }; // Contains the AV/C command (not shown)
long cbCmd = sizeof(AvcCmd);
hr = pTransport->GetTransportBasicParameters(
    ED_RAW_EXT_DEV_CMD, 
    &cbCmd,
    (LPOLESTR_) AvcCmd);
```



<span data-ttu-id="5a9d7-119">El contenido de la matriz se pasa directamente al dispositivo, por lo que debe tener cuidado de formatearlo correctamente.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-119">The contents of the array are passed directly to the device, so you must be careful to format it correctly.</span></span> <span data-ttu-id="5a9d7-120">Un comando puede tener como destino la unidad (videocámara) o una subunidad (cinta o cámara).</span><span class="sxs-lookup"><span data-stu-id="5a9d7-120">A command can target the unit (camcorder) or a subunit (tape or camera).</span></span> <span data-ttu-id="5a9d7-121">Los estándares pertinentes están disponibles en el [sitio web de la asociación comercial 1394](https://1394ta.org).</span><span class="sxs-lookup"><span data-stu-id="5a9d7-121">The relevant standards are available from the [1394 Trade Association Web site](https://1394ta.org).</span></span>

-   <span data-ttu-id="5a9d7-122">Especificación general del conjunto de comandos de la interfaz digital AV/C</span><span class="sxs-lookup"><span data-stu-id="5a9d7-122">AV/C Digital Interface Command Set General Specification</span></span>
-   <span data-ttu-id="5a9d7-123">Grabadora de cinta AV/C/especificación de subunidad del reproductor</span><span class="sxs-lookup"><span data-stu-id="5a9d7-123">AV/C Tape Recorder/Player Subunit Specification</span></span>

<span data-ttu-id="5a9d7-124">En el primer procedimiento se describe cómo dar formato a los comandos AV/C y se enumeran los comandos de la unidad.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-124">The former describes how to format AV/C commands and lists the unit commands.</span></span> <span data-ttu-id="5a9d7-125">La última especificación muestra los comandos de la subunidad.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-125">The latter specification lists the subunit commands.</span></span>

<span data-ttu-id="5a9d7-126">El método **GetTransportBasicParameters** puede devolver uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="5a9d7-126">The **GetTransportBasicParameters** method may return one of the following error codes:</span></span>



| <span data-ttu-id="5a9d7-127">Código de error</span><span class="sxs-lookup"><span data-stu-id="5a9d7-127">Error Code</span></span>              | <span data-ttu-id="5a9d7-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a9d7-128">Description</span></span>                                                                      |
|-------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5a9d7-129">tiempo de espera de ERROR \_</span><span class="sxs-lookup"><span data-stu-id="5a9d7-129">ERROR\_TIMEOUT</span></span>          | <span data-ttu-id="5a9d7-130">El comando agotó el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-130">The command timed out.</span></span>                                                           |
| <span data-ttu-id="5a9d7-131">ERROR \_ req \_ no \_ ACCEP</span><span class="sxs-lookup"><span data-stu-id="5a9d7-131">ERROR\_REQ\_NOT\_ACCEP</span></span>  | <span data-ttu-id="5a9d7-132">El dispositivo no aceptó el comando.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-132">The device did not accept the command.</span></span>                                           |
| <span data-ttu-id="5a9d7-133">ERROR \_ no \_ admitido</span><span class="sxs-lookup"><span data-stu-id="5a9d7-133">ERROR\_NOT\_SUPPORTED</span></span>   | <span data-ttu-id="5a9d7-134">El dispositivo no admite el comando.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-134">The device does not support the command.</span></span>                                         |
| <span data-ttu-id="5a9d7-135">solicitud de ERROR \_ \_ anulada</span><span class="sxs-lookup"><span data-stu-id="5a9d7-135">ERROR\_REQUEST\_ABORTED</span></span> | <span data-ttu-id="5a9d7-136">El comando se anuló.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-136">The command was aborted.</span></span> <span data-ttu-id="5a9d7-137">Possbly el dispositivo se quitó o se produjo un restablecimiento de bus.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-137">Possbly the device was removed or a bus reset occurred.</span></span> |



 

> [!Note]  
> <span data-ttu-id="5a9d7-138">Estos errores se devuelven como códigos de error de Win32, no como HRESULT, por lo que debe probar estos valores directamente, en lugar de usar las macros **Succeeded** y **failed** .</span><span class="sxs-lookup"><span data-stu-id="5a9d7-138">These errors are returned as Win32 error codes, not HRESULTs, so you should test for these values directly, rather than using the **SUCCEEDED** and **FAILED** macros.</span></span>

 

<span data-ttu-id="5a9d7-139">Si el método devuelve S \_ correcto, la respuesta del dispositivo se copia en la matriz.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-139">If the method returns S\_OK, the response from the device is copied into the array.</span></span> <span data-ttu-id="5a9d7-140">La carga útil de respuesta puede ser mayor que el comando, por lo que debe asignar un búfer lo suficientemente grande como para almacenarlo.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-140">The response payload might be larger than the command, so you must allocate a buffer large enough to hold it.</span></span> <span data-ttu-id="5a9d7-141">El tamaño máximo de carga es de 512 bytes.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-141">The maximum payload size is 512 bytes.</span></span> <span data-ttu-id="5a9d7-142">Tenga en cuenta que un valor devuelto de S \_ OK no siempre significa que el dispositivo ha realizado correctamente el comando.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-142">Note that a return value of S\_OK does not always mean the device successfully carried out the command.</span></span> <span data-ttu-id="5a9d7-143">La aplicación debe examinar la carga de respuesta para determinar el estado.</span><span class="sxs-lookup"><span data-stu-id="5a9d7-143">The application must examine the response payload to determine the status.</span></span>

<span data-ttu-id="5a9d7-144">En el ejemplo siguiente se muestra el comando para buscar una búsqueda de número de pista absoluta:</span><span class="sxs-lookup"><span data-stu-id="5a9d7-144">The following example shows the command to search for an absolute track number search:</span></span>


```C++
// Set up the ATN search command.
BYTE AvcCmd[] = 
{ 
    0x00,   // ctype = "control"
    0x20,   // subunit_type, subunit_id
    0x52,   // opcode (ATN)
    0x20,   // operand 0 = "search"
    0x00,   // operand 1 = ATN
    0x00,   // operand 2 = ATN
    0x00,   // operand 3 = ATN
    0xFF   //  operand 4 = D-VCR medium type.
};
// Specify a track number.
ULONG ulTrackNumber = track_number; // Specify the track number here.
// Shift over by 1 (LSB of operand 1 is a 1-bit blank flag)
ulTrackNumber = ulTrackNumber << 1; 
// Plug this number into operands 1 - 3.
AvcCmd[4] = (BYTE) (ulTrackNumber & 0x000000FF);
AvcCmd[5] = (BYTE)((ulTrackNumber & 0x0000FF00) >> 8);
AvcCmd[6] = (BYTE)((ulTrackNumber & 0x00FF0000) >> 16);
```



## <a name="related-topics"></a><span data-ttu-id="5a9d7-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a9d7-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a9d7-146">Control de una videocámara DV</span><span class="sxs-lookup"><span data-stu-id="5a9d7-146">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



