---
description: El Windows SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede utilizar para controlar un servicio. Sus comandos se corresponden con las funciones proporcionadas por el SCM. La sintaxis es la siguiente.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Controlar un servicio mediante SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668295"
---
# <a name="controlling-a-service-using-sc"></a><span data-ttu-id="d8821-105">Controlar un servicio mediante SC</span><span class="sxs-lookup"><span data-stu-id="d8821-105">Controlling a Service Using SC</span></span>

<span data-ttu-id="d8821-106">El Windows SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede utilizar para controlar un servicio.</span><span class="sxs-lookup"><span data-stu-id="d8821-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to control a service.</span></span> <span data-ttu-id="d8821-107">Sus comandos se corresponden con las funciones proporcionadas por el SCM.</span><span class="sxs-lookup"><span data-stu-id="d8821-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="d8821-108">La sintaxis es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="d8821-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8821-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d8821-109">Syntax</span></span>

<span data-ttu-id="d8821-110">**SC** \[ *NombreDeServidor* \] *Comando* \[  \] ServiceName \[  \] Opción1 \[ *opción2* \] ...</span><span class="sxs-lookup"><span data-stu-id="d8821-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="d8821-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span><span class="sxs-lookup"><span data-stu-id="d8821-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="d8821-112">Nombre de servidor opcional.</span><span class="sxs-lookup"><span data-stu-id="d8821-112">Optional server name.</span></span> <span data-ttu-id="d8821-113">Use el formato \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="d8821-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="d8821-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span><span class="sxs-lookup"><span data-stu-id="d8821-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="d8821-115">Uno de los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="d8821-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="d8821-116">continue</span><span class="sxs-lookup"><span data-stu-id="d8821-116">continue</span></span></dd> <dd><span data-ttu-id="d8821-117">control</span><span class="sxs-lookup"><span data-stu-id="d8821-117">control</span></span></dd> <dd><span data-ttu-id="d8821-118">interrogar</span><span class="sxs-lookup"><span data-stu-id="d8821-118">interrogate</span></span></dd> <dd><span data-ttu-id="d8821-119">pause</span><span class="sxs-lookup"><span data-stu-id="d8821-119">pause</span></span></dd> <dd><span data-ttu-id="d8821-120">start</span><span class="sxs-lookup"><span data-stu-id="d8821-120">start</span></span></dd> <dd><span data-ttu-id="d8821-121">stop</span><span class="sxs-lookup"><span data-stu-id="d8821-121">stop</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="d8821-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span><span class="sxs-lookup"><span data-stu-id="d8821-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="d8821-123">Nombre del servicio, tal y como se especificó cuando se instaló.</span><span class="sxs-lookup"><span data-stu-id="d8821-123">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="d8821-124"><span id="option1"></span><span id="OPTION1"></span>*Opción1*</span><span class="sxs-lookup"><span data-stu-id="d8821-124"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="d8821-125">Parámetro opcional.</span><span class="sxs-lookup"><span data-stu-id="d8821-125">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d8821-126"><span id="option2"></span><span id="OPTION2"></span>*opción2*</span><span class="sxs-lookup"><span data-stu-id="d8821-126"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="d8821-127">Parámetro opcional.</span><span class="sxs-lookup"><span data-stu-id="d8821-127">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8821-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8821-128">Remarks</span></span>

<span data-ttu-id="d8821-129">Para ver la sintaxis completa de un comando, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="d8821-129">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="d8821-130">**SC** ( *comando* )</span><span class="sxs-lookup"><span data-stu-id="d8821-130">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8821-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d8821-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8821-132">Solicitudes de control de servicio</span><span class="sxs-lookup"><span data-stu-id="d8821-132">Service Control Requests</span></span>](service-control-requests.md)
</dt> <dt>

[<span data-ttu-id="d8821-133">Inicio del servicio</span><span class="sxs-lookup"><span data-stu-id="d8821-133">Service Startup</span></span>](service-startup.md)
</dt> </dl>

 

 



