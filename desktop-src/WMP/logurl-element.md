---
title: Elemento LOGURL
description: El elemento LOGURL indica a Windows Media Player que envíe los datos de registro a la dirección URL especificada.
ms.assetid: fc1895af-c9d7-43ca-9839-7e884cc219f4
keywords:
- Elemento LOGURL Media Player Windows
topic_type:
- apiref
api_name:
- LOGURL Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0f5fc4a5259f009e7298c0609fc4e6fa8c533b94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708831"
---
# <a name="logurl-element"></a><span data-ttu-id="4916d-104">Elemento LOGURL</span><span class="sxs-lookup"><span data-stu-id="4916d-104">LOGURL Element</span></span>

<span data-ttu-id="4916d-105">El elemento **LOGURL** indica a Windows Media Player que envíe los datos de registro a la dirección URL especificada.</span><span class="sxs-lookup"><span data-stu-id="4916d-105">The **LOGURL** element instructs Windows Media Player to submit any log data to the specified URL.</span></span>

``` syntax
<LOGURL
   HREF = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="4916d-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="4916d-106">Attributes</span></span>

<span data-ttu-id="4916d-107">**Href** (obligatorio)</span><span class="sxs-lookup"><span data-stu-id="4916d-107">**HREF** (required)</span></span>

<span data-ttu-id="4916d-108">Dirección URL de un host que puede procesar solicitudes de registro.</span><span class="sxs-lookup"><span data-stu-id="4916d-108">URL to a host that is able to process logging requests.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="4916d-109">Elementos primarios y secundarios</span><span class="sxs-lookup"><span data-stu-id="4916d-109">Parent/Child Elements</span></span>



| <span data-ttu-id="4916d-110">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="4916d-110">Hierarchy</span></span>       | <span data-ttu-id="4916d-111">Elementos</span><span class="sxs-lookup"><span data-stu-id="4916d-111">Elements</span></span>           |
|-----------------|--------------------|
| <span data-ttu-id="4916d-112">Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="4916d-112">Parent elements</span></span> | <span data-ttu-id="4916d-113">**ASX**, **entrada**</span><span class="sxs-lookup"><span data-stu-id="4916d-113">**ASX**, **ENTRY**</span></span> |
| <span data-ttu-id="4916d-114">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="4916d-114">Child elements</span></span>  | <span data-ttu-id="4916d-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4916d-115">None</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="4916d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4916d-116">Remarks</span></span>

<span data-ttu-id="4916d-117">El elemento **LOGURL** permite que una lista de reproducción de metarchivo de cliente envíe información de registro adicional a los servidores especificados.</span><span class="sxs-lookup"><span data-stu-id="4916d-117">The **LOGURL** element enables a client metafile playlist to send additional logging information to specified servers.</span></span> <span data-ttu-id="4916d-118">La información de registro se envía automáticamente al servidor de origen de una lista de reproducción cuando se abre y a cada uno de los **LOGURL** especificados para el elemento **ASX** , si hay alguno.</span><span class="sxs-lookup"><span data-stu-id="4916d-118">Logging information is automatically sent to the origin server of a playlist when it is opened and to each **LOGURL** specified for the **ASX** element, if any are present.</span></span> <span data-ttu-id="4916d-119">La información de registro también se envía a cada **LOGURL** especificado para un elemento de **entrada** cuando se alcanza dicha entrada.</span><span class="sxs-lookup"><span data-stu-id="4916d-119">Logging information is also sent to each **LOGURL** specified for an **ENTRY** element when that entry is reached.</span></span> <span data-ttu-id="4916d-120">La dirección URL especificada en el atributo **href** de un elemento **LOGURL** debe ser la dirección de un host que pueda procesar solicitudes de registro.</span><span class="sxs-lookup"><span data-stu-id="4916d-120">The URL specified in the **HREF** attribute of a **LOGURL** element must be the address of a host that is able to process logging requests.</span></span> <span data-ttu-id="4916d-121">La dirección URL puede ser cualquier dirección URL HTTP válida.</span><span class="sxs-lookup"><span data-stu-id="4916d-121">The URL can be any valid HTTP URL.</span></span> <span data-ttu-id="4916d-122">La dirección URL también puede indicar la ubicación de un script CGI.</span><span class="sxs-lookup"><span data-stu-id="4916d-122">The URL can also indicate the location of a CGI script.</span></span>

<span data-ttu-id="4916d-123">Los únicos protocolos válidos para un elemento **LOGURL** son http y https.</span><span class="sxs-lookup"><span data-stu-id="4916d-123">The only valid protocols for a **LOGURL** element are HTTP and HTTPS.</span></span>

<span data-ttu-id="4916d-124">Un elemento **LOGURL** dentro del ámbito de un elemento **ASX** solo es aplicable al metarchivo en el que reside, independientemente de si se hace referencia a ese metarchivo desde otro metarchivo.</span><span class="sxs-lookup"><span data-stu-id="4916d-124">A **LOGURL** element within the scope of an **ASX** element is applicable only to the metafile in which it resides, regardless of whether that metafile is referenced from another metafile.</span></span> <span data-ttu-id="4916d-125">Un elemento **LOGURL** fuerza el envío de datos de registro para todo el contenido transmitido desde dentro de su ámbito definido y solo para el contenido transmitido desde dentro de su ámbito definido.</span><span class="sxs-lookup"><span data-stu-id="4916d-125">A **LOGURL** element forces the submission of log data for all content streamed from within its defined scope and only for content streamed from within its defined scope.</span></span> <span data-ttu-id="4916d-126">Los datos de registro se enviarán al servidor de origen y a todas las direcciones URL que aparecen en cada elemento **LOGURL** en el ámbito.</span><span class="sxs-lookup"><span data-stu-id="4916d-126">Log data will be submitted to the origin server and to all URLs listed in every **LOGURL** element in scope.</span></span> <span data-ttu-id="4916d-127">Los datos de registro se enviarán una sola vez a cada dirección URL indicada, incluso si la misma dirección URL aparece más de una vez en un ámbito determinado.</span><span class="sxs-lookup"><span data-stu-id="4916d-127">Log data will be submitted only once to each listed URL, even if the same URL is listed more than once in a given scope.</span></span> <span data-ttu-id="4916d-128">Una repetición de una **entrada** produciría otro envío a las direcciones URL enumeradas.</span><span class="sxs-lookup"><span data-stu-id="4916d-128">A repeat of an **ENTRY** would result in another submission to the listed URLs.</span></span>

<span data-ttu-id="4916d-129">No hay ningún límite en el número de elementos **LOGURL** de una lista de reproducción de metarchivo.</span><span class="sxs-lookup"><span data-stu-id="4916d-129">There is no limit to the number of **LOGURL** elements in a metafile playlist.</span></span>

## <a name="examples"></a><span data-ttu-id="4916d-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="4916d-130">Examples</span></span>


```XML
<ASX VERSION="3.0">
  <TITLE>Example Media Player Show</TITLE>
  <LOGURL HREF="https://example.microsoft.com/info/showlog.asp?whatsup" />
  <ENTRY>
    <REF href="mms://ucast.proseware.com/Media1.asf" />
    <LOGURL HREF="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal"/>
  </ENTRY>
</ASX>
```



<span data-ttu-id="4916d-131">A continuación se muestran ejemplos de direcciones URL válidas.</span><span class="sxs-lookup"><span data-stu-id="4916d-131">The following are examples of valid URLs.</span></span>

<span data-ttu-id="4916d-132">Dirección URL de una aplicación ISAPI:</span><span class="sxs-lookup"><span data-stu-id="4916d-132">URL of an ISAPI application:</span></span>


```XML
https://www.proseware.com/logs/WMSLogging.dll
```



<span data-ttu-id="4916d-133">Dirección URL de un script CGI:</span><span class="sxs-lookup"><span data-stu-id="4916d-133">URL of a CGI script:</span></span>


```XML
https://www.proseware.com/cgi-bin/My_WMS_Logging_Script.pl
```



<span data-ttu-id="4916d-134">Una dirección URL HTTP válida:</span><span class="sxs-lookup"><span data-stu-id="4916d-134">A valid HTTP URL:</span></span>


```XML
https://www.proseware.com/some/arbitrary/path/My_WMS_Logging_Page.asp?PubPoint=FooPubPoint&AnotherName=AnotherValue
```



## <a name="requirements"></a><span data-ttu-id="4916d-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4916d-135">Requirements</span></span>



| <span data-ttu-id="4916d-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="4916d-136">Requirement</span></span> | <span data-ttu-id="4916d-137">Value</span><span class="sxs-lookup"><span data-stu-id="4916d-137">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="4916d-138">Versión</span><span class="sxs-lookup"><span data-stu-id="4916d-138">Version</span></span><br/> | <span data-ttu-id="4916d-139">Windows Media Player versión 70 o posterior</span><span class="sxs-lookup"><span data-stu-id="4916d-139">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4916d-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="4916d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4916d-141">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4916d-141">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> <dt>

[<span data-ttu-id="4916d-142">**Referencia de metarchivos de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="4916d-142">**Windows Media Metafile Reference**</span></span>](windows-media-metafile-reference.md)
</dt> </dl>

 

 





