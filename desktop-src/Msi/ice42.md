---
description: ICE42 valida que los servidores INPROC no están vinculados a archivos EXE de la tabla de clases. También valida que solo las clases LocalServer y LocalServer32 tengan argumentos y valores DefInProc.
ms.assetid: 14976772-c873-46d8-8687-dcdad2420d83
title: ICE42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebe2ea09431870ac7b52ccd69d0ae16c646286ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652813"
---
# <a name="ice42"></a><span data-ttu-id="d4f6e-104">ICE42</span><span class="sxs-lookup"><span data-stu-id="d4f6e-104">ICE42</span></span>

<span data-ttu-id="d4f6e-105">ICE42 valida que los servidores INPROC no están vinculados a archivos EXE de la [tabla de clases](class-table.md).</span><span class="sxs-lookup"><span data-stu-id="d4f6e-105">ICE42 validates that InProc servers are not linked to EXE files in the [Class table](class-table.md).</span></span> <span data-ttu-id="d4f6e-106">También valida que solo las clases LocalServer y LocalServer32 tengan argumentos y valores DefInProc.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-106">It also validates that only LocalServer and LocalServer32 classes have arguments and DefInProc values.</span></span>

## <a name="result"></a><span data-ttu-id="d4f6e-107">Resultado</span><span class="sxs-lookup"><span data-stu-id="d4f6e-107">Result</span></span>

<span data-ttu-id="d4f6e-108">ICE42 publica un error si hay servidores INPROC vinculados a archivos EXE en la tabla de clases.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-108">ICE42 posts an error if there are InProc servers linked to EXE files in the Class table.</span></span>

## <a name="example"></a><span data-ttu-id="d4f6e-109">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d4f6e-109">Example</span></span>

<span data-ttu-id="d4f6e-110">ICE42 notificaría los siguientes errores para el ejemplo que se muestra.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-110">ICE42 would report the following errors for the example shown.</span></span>



| <span data-ttu-id="d4f6e-111">Error ICE42</span><span class="sxs-lookup"><span data-stu-id="d4f6e-111">ICE42 error</span></span>                                                                                                                             | <span data-ttu-id="d4f6e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4f6e-112">Description</span></span>                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f6e-113">El CLSID ' {GUID1} ' es un servidor INPROC, pero el componente de implementación ' Component1 ' tiene un archivo EXE (' test.exe ') como KeyFile.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-113">CLSID '{GUID1}' is an InProc server, but the implementing component 'Component1' has an EXE ('test.exe') as its KeyFile.</span></span>                | <span data-ttu-id="d4f6e-114">Hay un archivo ejecutable especificado como servidor INPROC.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-114">There is an executable file specified as an InProc server.</span></span> <span data-ttu-id="d4f6e-115">Los archivos EXE no pueden ser servidores INPROC.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-115">EXE files cannot be InProc servers.</span></span>                                                                                                                            |
| <span data-ttu-id="d4f6e-116">El CLSID ' {GUID1} ' en el contexto ' InProcServer32 ' tiene un argumento.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-116">CLSID '{GUID1}' in context 'InProcServer32' has an argument.</span></span> <span data-ttu-id="d4f6e-117">Solo los contextos LocalServer pueden tener argumentos.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-117">Only LocalServer contexts can have arguments.</span></span>                              | <span data-ttu-id="d4f6e-118">Para corregir este error, quite el argumento.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-118">To fix this error, remove the argument.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="d4f6e-119">El CLSID ' {GUID1} ' en el contexto ' InProcServer32 ' especifica un valor INPROC predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-119">CLSID '{GUID1}' in context 'InProcServer32' specifies a default InProc value.</span></span> <span data-ttu-id="d4f6e-120">Solo los contextos LocalServer pueden tener valores INPROC predeterminados.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-120">Only LocalServer contexts can have default InProc values.</span></span> | <span data-ttu-id="d4f6e-121">Hay un objeto con un valor INPROC predeterminado que no es un objeto que funciona en los contextos LocalServer o LocalServer32.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-121">There is an object with a default InProc value that is not an object operating in the LocalServer or LocalServer32 contexts.</span></span> <span data-ttu-id="d4f6e-122">Para corregir este error, quite el valor DeflnProc o cambie el contexto de la clase.</span><span class="sxs-lookup"><span data-stu-id="d4f6e-122">To fix this error, remove the DeflnProc value or change the context of the class.</span></span><br/> |



 

<span data-ttu-id="d4f6e-123">[Tabla de clases](class-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d4f6e-123">[Class Table](class-table.md) (partial)</span></span>



| <span data-ttu-id="d4f6e-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="d4f6e-124">CLSID</span></span>   | <span data-ttu-id="d4f6e-125">Context</span><span class="sxs-lookup"><span data-stu-id="d4f6e-125">Context</span></span>        | <span data-ttu-id="d4f6e-126">Componente\_</span><span class="sxs-lookup"><span data-stu-id="d4f6e-126">Component\_</span></span> | <span data-ttu-id="d4f6e-127">DefInProcHandler</span><span class="sxs-lookup"><span data-stu-id="d4f6e-127">DefInProcHandler</span></span> | <span data-ttu-id="d4f6e-128">Argumento</span><span class="sxs-lookup"><span data-stu-id="d4f6e-128">Argument</span></span> |
|---------|----------------|-------------|------------------|----------|
| <span data-ttu-id="d4f6e-129">GUID1</span><span class="sxs-lookup"><span data-stu-id="d4f6e-129">{GUID1}</span></span> | <span data-ttu-id="d4f6e-130">InProcServer32</span><span class="sxs-lookup"><span data-stu-id="d4f6e-130">InProcServer32</span></span> | <span data-ttu-id="d4f6e-131">Component1</span><span class="sxs-lookup"><span data-stu-id="d4f6e-131">Component1</span></span>  | <span data-ttu-id="d4f6e-132">InProcServer</span><span class="sxs-lookup"><span data-stu-id="d4f6e-132">InProcServer</span></span>     | <span data-ttu-id="d4f6e-133">Argumento</span><span class="sxs-lookup"><span data-stu-id="d4f6e-133">Arg</span></span>      |



 

<span data-ttu-id="d4f6e-134">[Tabla de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d4f6e-134">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="d4f6e-135">Componente</span><span class="sxs-lookup"><span data-stu-id="d4f6e-135">Component</span></span>  | <span data-ttu-id="d4f6e-136">Rutas</span><span class="sxs-lookup"><span data-stu-id="d4f6e-136">KeyPath</span></span> |
|------------|---------|
| <span data-ttu-id="d4f6e-137">Component1</span><span class="sxs-lookup"><span data-stu-id="d4f6e-137">Component1</span></span> | <span data-ttu-id="d4f6e-138">Archivo1</span><span class="sxs-lookup"><span data-stu-id="d4f6e-138">File1</span></span>   |



 

<span data-ttu-id="d4f6e-139">[Tabla de archivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d4f6e-139">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="d4f6e-140">Archivo</span><span class="sxs-lookup"><span data-stu-id="d4f6e-140">File</span></span>  | <span data-ttu-id="d4f6e-141">Nombre de archivo</span><span class="sxs-lookup"><span data-stu-id="d4f6e-141">Filename</span></span> |
|-------|----------|
| <span data-ttu-id="d4f6e-142">Archivo1</span><span class="sxs-lookup"><span data-stu-id="d4f6e-142">File1</span></span> | <span data-ttu-id="d4f6e-143">test.exe</span><span class="sxs-lookup"><span data-stu-id="d4f6e-143">test.exe</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d4f6e-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d4f6e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d4f6e-145">Referencia de ICE</span><span class="sxs-lookup"><span data-stu-id="d4f6e-145">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 




