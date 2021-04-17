---
description: El Windows SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede usar para consultar o modificar la base de datos de los servicios instalados. Sus comandos se corresponden con las funciones proporcionadas por el SCM. La sintaxis es la siguiente.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Configuración de un servicio mediante SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666348"
---
# <a name="configuring-a-service-using-sc"></a><span data-ttu-id="6fb54-105">Configuración de un servicio mediante SC</span><span class="sxs-lookup"><span data-stu-id="6fb54-105">Configuring a Service Using SC</span></span>

<span data-ttu-id="6fb54-106">El Windows SDK contiene una utilidad de línea de comandos, Sc.exe, que se puede usar para consultar o modificar la base de datos de los servicios instalados.</span><span class="sxs-lookup"><span data-stu-id="6fb54-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to query or modify the database of installed services.</span></span> <span data-ttu-id="6fb54-107">Sus comandos se corresponden con las funciones proporcionadas por el SCM.</span><span class="sxs-lookup"><span data-stu-id="6fb54-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="6fb54-108">La sintaxis es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="6fb54-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fb54-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6fb54-109">Syntax</span></span>

<span data-ttu-id="6fb54-110">**SC** \[ *NombreDeServidor* \] *Comando* \[  \] ServiceName \[  \] Opción1 \[ *opción2* \] ...</span><span class="sxs-lookup"><span data-stu-id="6fb54-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="6fb54-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span><span class="sxs-lookup"><span data-stu-id="6fb54-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="6fb54-112">Nombre de servidor opcional.</span><span class="sxs-lookup"><span data-stu-id="6fb54-112">Optional server name.</span></span> <span data-ttu-id="6fb54-113">Use el formato \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="6fb54-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="6fb54-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span><span class="sxs-lookup"><span data-stu-id="6fb54-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="6fb54-115">Uno de los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="6fb54-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="6fb54-116">boot</span><span class="sxs-lookup"><span data-stu-id="6fb54-116">boot</span></span></dd> <dd><span data-ttu-id="6fb54-117">config</span><span class="sxs-lookup"><span data-stu-id="6fb54-117">config</span></span></dd> <dd><span data-ttu-id="6fb54-118">create</span><span class="sxs-lookup"><span data-stu-id="6fb54-118">create</span></span></dd> <dd><span data-ttu-id="6fb54-119">delete</span><span class="sxs-lookup"><span data-stu-id="6fb54-119">delete</span></span></dd> <dd><span data-ttu-id="6fb54-120">description</span><span class="sxs-lookup"><span data-stu-id="6fb54-120">description</span></span></dd> <dd><span data-ttu-id="6fb54-121">EnumDepend</span><span class="sxs-lookup"><span data-stu-id="6fb54-121">EnumDepend</span></span></dd> <dd><span data-ttu-id="6fb54-122">failure</span><span class="sxs-lookup"><span data-stu-id="6fb54-122">failure</span></span></dd> <dd><span data-ttu-id="6fb54-123">failureflag</span><span class="sxs-lookup"><span data-stu-id="6fb54-123">failureflag</span></span></dd> <dd><span data-ttu-id="6fb54-124">GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="6fb54-124">GetDisplayName</span></span></dd> <dd><span data-ttu-id="6fb54-125">GetKeyName</span><span class="sxs-lookup"><span data-stu-id="6fb54-125">GetKeyName</span></span></dd> <dd><span data-ttu-id="6fb54-126">Lock</span><span class="sxs-lookup"><span data-stu-id="6fb54-126">Lock</span></span></dd> <dd><span data-ttu-id="6fb54-127">qc</span><span class="sxs-lookup"><span data-stu-id="6fb54-127">qc</span></span></dd> <dd><span data-ttu-id="6fb54-128">qdescription</span><span class="sxs-lookup"><span data-stu-id="6fb54-128">qdescription</span></span></dd> <dd><span data-ttu-id="6fb54-129">qfailure</span><span class="sxs-lookup"><span data-stu-id="6fb54-129">qfailure</span></span></dd> <dd><span data-ttu-id="6fb54-130">qfailureflag</span><span class="sxs-lookup"><span data-stu-id="6fb54-130">qfailureflag</span></span></dd> <dd><span data-ttu-id="6fb54-131">qprivs</span><span class="sxs-lookup"><span data-stu-id="6fb54-131">qprivs</span></span></dd> <dd><span data-ttu-id="6fb54-132">qsidtype</span><span class="sxs-lookup"><span data-stu-id="6fb54-132">qsidtype</span></span></dd> <dd><span data-ttu-id="6fb54-133">Query</span><span class="sxs-lookup"><span data-stu-id="6fb54-133">query</span></span></dd> <dd><span data-ttu-id="6fb54-134">QueryEx</span><span class="sxs-lookup"><span data-stu-id="6fb54-134">queryex</span></span></dd> <dd><span data-ttu-id="6fb54-135">priv</span><span class="sxs-lookup"><span data-stu-id="6fb54-135">privs</span></span></dd> <dd><span data-ttu-id="6fb54-136">QueryLock</span><span class="sxs-lookup"><span data-stu-id="6fb54-136">QueryLock</span></span></dd> <dd><span data-ttu-id="6fb54-137">sdset</span><span class="sxs-lookup"><span data-stu-id="6fb54-137">sdset</span></span></dd> <dd><span data-ttu-id="6fb54-138">sdshow</span><span class="sxs-lookup"><span data-stu-id="6fb54-138">sdshow</span></span></dd> <dd><span data-ttu-id="6fb54-139">showsid</span><span class="sxs-lookup"><span data-stu-id="6fb54-139">showsid</span></span></dd> <dd><span data-ttu-id="6fb54-140">SID</span><span class="sxs-lookup"><span data-stu-id="6fb54-140">sidtype</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="6fb54-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span><span class="sxs-lookup"><span data-stu-id="6fb54-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="6fb54-142">Nombre del servicio, tal y como se especificó cuando se instaló.</span><span class="sxs-lookup"><span data-stu-id="6fb54-142">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="6fb54-143"><span id="option1"></span><span id="OPTION1"></span>*Opción1*</span><span class="sxs-lookup"><span data-stu-id="6fb54-143"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="6fb54-144">Parámetro opcional.</span><span class="sxs-lookup"><span data-stu-id="6fb54-144">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="6fb54-145"><span id="option2"></span><span id="OPTION2"></span>*opción2*</span><span class="sxs-lookup"><span data-stu-id="6fb54-145"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="6fb54-146">Parámetro opcional.</span><span class="sxs-lookup"><span data-stu-id="6fb54-146">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fb54-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6fb54-147">Remarks</span></span>

<span data-ttu-id="6fb54-148">Para ver la sintaxis completa de un comando, use el siguiente comando:</span><span class="sxs-lookup"><span data-stu-id="6fb54-148">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="6fb54-149">**SC** ( *comando* )</span><span class="sxs-lookup"><span data-stu-id="6fb54-149">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="6fb54-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6fb54-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fb54-151">Configuración de servicio</span><span class="sxs-lookup"><span data-stu-id="6fb54-151">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="6fb54-152">Instalación, eliminación y enumeración del servicio</span><span class="sxs-lookup"><span data-stu-id="6fb54-152">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



