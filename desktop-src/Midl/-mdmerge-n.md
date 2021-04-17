---
title: /n (modificador)
description: El modificador/n especifica la profundidad de composición para crear archivos de metadatos.
ms.assetid: 7A1F8A9E-B3CC-4BB2-BF50-5662D4560280
keywords:
- /n cambiar MIDL
topic_type:
- apiref
api_name:
- /n
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78197c0f79c6bbe21ae4eb883620b95e6f0bd4c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690824"
---
# <a name="n-switch"></a><span data-ttu-id="9c723-104">/n (modificador)</span><span class="sxs-lookup"><span data-stu-id="9c723-104">/n switch</span></span>

<span data-ttu-id="9c723-105">El modificador **/n** especifica la profundidad de composición para crear archivos de metadatos.</span><span class="sxs-lookup"><span data-stu-id="9c723-105">The **/n** switch specifies the composition depth for composing metadata files.</span></span>

``` syntax
mdmerge /n namespace_depth
```

## <a name="switch-options"></a><span data-ttu-id="9c723-106">Opciones de conmutador</span><span class="sxs-lookup"><span data-stu-id="9c723-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="9c723-107">*profundidad del espacio de nombres \_*</span><span class="sxs-lookup"><span data-stu-id="9c723-107">*namespace\_depth*</span></span> 
</dt> <dd>

<span data-ttu-id="9c723-108">Especifica la profundidad del espacio de nombres que se va a componer en un único archivo de metadatos.</span><span class="sxs-lookup"><span data-stu-id="9c723-108">Specifies the namespace depth to compose into a single metadata file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c723-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c723-109">Remarks</span></span>

<span data-ttu-id="9c723-110">Estos son los posibles formatos de valores que puede especificar con el modificador **/n** .</span><span class="sxs-lookup"><span data-stu-id="9c723-110">Here are the possible value formats that you can specify with the **/n** switch.</span></span>



| <span data-ttu-id="9c723-111">Formato del valor</span><span class="sxs-lookup"><span data-stu-id="9c723-111">Value format</span></span>                   | <span data-ttu-id="9c723-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="9c723-112">Description</span></span>                                                                     |
|--------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="9c723-113">Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="9c723-113">Int32 > 0</span></span>                   | <span data-ttu-id="9c723-114">Cree todos los tipos en la profundidad de espacio de nombres especificada en el modificador.</span><span class="sxs-lookup"><span data-stu-id="9c723-114">Compose all types at the namespace depth specified in the switch.</span></span>               |
| <span data-ttu-id="9c723-115">-1</span><span class="sxs-lookup"><span data-stu-id="9c723-115">-1</span></span>                             | <span data-ttu-id="9c723-116">Cree todos los tipos en un archivo IDL por espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="9c723-116">Compose all types into one IDL file per namespace.</span></span>                              |
| <span data-ttu-id="9c723-117"><namespace>: Int32 > 0</span><span class="sxs-lookup"><span data-stu-id="9c723-117"><namespace>:Int32 > 0</span></span> | <span data-ttu-id="9c723-118">Cree todos los tipos con el espacio de nombres coincidente a la profundidad especificada en el modificador.</span><span class="sxs-lookup"><span data-stu-id="9c723-118">Compose all types with matching namespace at the depth specified in the switch.</span></span> |
| <span data-ttu-id="9c723-119"><namespace>:-1</span><span class="sxs-lookup"><span data-stu-id="9c723-119"><namespace>:-1</span></span>           | <span data-ttu-id="9c723-120">Cree todos los tipos con espacio de nombres coincidente en un archivo por espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="9c723-120">Compose all types with matching namespace into one file per namespace.</span></span>          |



 

<span data-ttu-id="9c723-121">En la tabla siguiente se muestran los resultados de distintas combinaciones del modificador **/n** que funcionan en estos espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="9c723-121">The following table shows the results from different combinations of the **/n** switch working on these namespaces.</span></span>

-   <span data-ttu-id="9c723-122">Windows. Foundation. Collections. IIterable</span><span class="sxs-lookup"><span data-stu-id="9c723-122">Windows.Foundation.Collections.IIterable</span></span>
-   <span data-ttu-id="9c723-123">Windows. UI. DirectUI. Controls. Button</span><span class="sxs-lookup"><span data-stu-id="9c723-123">Windows.UI.DirectUI.Controls.Button</span></span>
-   <span data-ttu-id="9c723-124">Windows. UI. DirectUI. Controls. ListView</span><span class="sxs-lookup"><span data-stu-id="9c723-124">Windows.UI.DirectUI.Controls.ListView</span></span>
-   <span data-ttu-id="9c723-125">Windows. UI. inmersivo. Application. Playto. Target</span><span class="sxs-lookup"><span data-stu-id="9c723-125">Windows.UI.Immersive.Application.PlayTo.Target</span></span>
-   <span data-ttu-id="9c723-126">Windows. Web. Syndication. RSS</span><span class="sxs-lookup"><span data-stu-id="9c723-126">Windows.Web.Syndication.RSS</span></span>



| <span data-ttu-id="9c723-127">Conmutadores</span><span class="sxs-lookup"><span data-stu-id="9c723-127">Switches</span></span>                         | <span data-ttu-id="9c723-128">Resultado</span><span class="sxs-lookup"><span data-stu-id="9c723-128">Result</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="9c723-129">Explicación</span><span class="sxs-lookup"><span data-stu-id="9c723-129">Explanation</span></span>                                                                                                                                                                                                                                                                                                                        |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c723-130">**/n:-1**  / **n:1**</span><span class="sxs-lookup"><span data-stu-id="9c723-130">**/n:-1** /**n:1**</span></span>               | <span data-ttu-id="9c723-131">Windows.winmd</span><span class="sxs-lookup"><span data-stu-id="9c723-131">Windows.winmd</span></span>                                                                                                                                                                                                                                                | <span data-ttu-id="9c723-132">El último modificador/n invalida todos los modificadores-n anteriores.</span><span class="sxs-lookup"><span data-stu-id="9c723-132">The last /n switch overrides all previous –n switches.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="9c723-133">**/n:-1/n: Windows. UI: 2**</span><span class="sxs-lookup"><span data-stu-id="9c723-133">**/n:-1/n:Windows.UI:2**</span></span>         | <dl> <span data-ttu-id="9c723-134">Windows. <dt>Foundation. winmd</dt> <dt>Windows. UI. Winmd</dt> <dt>Windows. Web. Syndication. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="9c723-134"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.winmd</dt> <dt>Windows.Web.Syndication.winmd</dt></span></span> </dl> | <dl> <span data-ttu-id="9c723-135"><dt>**Windows. Foundation** siempre se compone de – n:2.</dt></span><span class="sxs-lookup"><span data-stu-id="9c723-135"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="9c723-136"><dt>Los tipos de **Windows. UI** están agrupados.</dt></span><span class="sxs-lookup"><span data-stu-id="9c723-136"><dt>**Windows.UI** types are grouped.</dt></span></span> <span data-ttu-id="9c723-137"><dt>**Windows. Web. Syndication** se compone de n:-1.</dt></span><span class="sxs-lookup"><span data-stu-id="9c723-137"><dt>**Windows.Web.Syndication** is composed at n:-1.</dt></span></span> </dl>       |
| <span data-ttu-id="9c723-138">**/n: 1/n: Windows. UI. DirectUI: 3**</span><span class="sxs-lookup"><span data-stu-id="9c723-138">**/n:1/n:Windows.UI.DirectUI:3**</span></span> | <dl> <span data-ttu-id="9c723-139">Windows. <dt>Foundation. winmd</dt> <dt>Windows. UI. DirectUI. winmd</dt> <dt>Windows. winmd</dt></span><span class="sxs-lookup"><span data-stu-id="9c723-139"><dt>Windows.Foundation.winmd</dt> <dt>Windows.UI.DirectUI.winmd </dt> <dt>Windows.winmd</dt></span></span> </dl>       | <dl> <span data-ttu-id="9c723-140"><dt>**Windows. Foundation** siempre se compone de – n:2.</dt></span><span class="sxs-lookup"><span data-stu-id="9c723-140"><dt>**Windows.Foundation** is always composed at –n:2.</dt></span></span> <span data-ttu-id="9c723-141"><dt>**Windows. UI. DirectUI** se compone en el nivel 3.</dt></span><span class="sxs-lookup"><span data-stu-id="9c723-141"><dt>**Windows.UI.DirectUI** is composed at level 3.</dt></span></span> <span data-ttu-id="9c723-142"><dt>Todos los demás tipos se componen en el nivel 1.</dt></span><span class="sxs-lookup"><span data-stu-id="9c723-142"><dt>All other types are composed at level 1.</dt></span></span> </dl> |



 

<span data-ttu-id="9c723-143">Estas son las reglas para administrar varias instancias del modificador **/n** .</span><span class="sxs-lookup"><span data-stu-id="9c723-143">Here are the rules for handling multiple instances of the **/n** switch.</span></span>

-   <span data-ttu-id="9c723-144">Prevalece la instancia más específica.</span><span class="sxs-lookup"><span data-stu-id="9c723-144">The most specific instance prevails.</span></span> <span data-ttu-id="9c723-145">Por ejemplo, si especifica **– n:A.B.C: 4 – n:A.B: 5**, MDMERGE resuelve a.b.c. D en el nivel 4, ya que a. B. C es más específico que A.B.</span><span class="sxs-lookup"><span data-stu-id="9c723-145">For example, if you specify **–n:A.B.C:4–n:A.B:5**, MDMERGE resolves A.B.C.D at level 4, because A.B.C is more specific than A.B.</span></span> <span data-ttu-id="9c723-146">A. B. E. F se resuelve en la profundidad 5, porque coincide con A. B pero no A.B.C.</span><span class="sxs-lookup"><span data-stu-id="9c723-146">A.B.E.F resolves at depth 5, because it matches A.B but not A.B.C.</span></span>
-   <span data-ttu-id="9c723-147">Prevalece la última instancia.</span><span class="sxs-lookup"><span data-stu-id="9c723-147">The last instance prevails.</span></span> <span data-ttu-id="9c723-148">Por ejemplo, si especifica **– n:5 – n:2**, los tipos se componen en el nivel 2.</span><span class="sxs-lookup"><span data-stu-id="9c723-148">For example, if you specify **–n:5–n:2**, the types are composed at level 2.</span></span>
-   <span data-ttu-id="9c723-149">Ambas reglas se aplican.</span><span class="sxs-lookup"><span data-stu-id="9c723-149">Both of these rules apply.</span></span> <span data-ttu-id="9c723-150">Si especifica – n:A.B.C: 4 – n:A.B.C: 1, el espacio de nombres A. B. C se compone en el nivel 1.</span><span class="sxs-lookup"><span data-stu-id="9c723-150">If you specify –n:A.B.C:4 –n:A.B.C:1, namespace A.B.C is composed at level 1.</span></span>

## <a name="examples"></a><span data-ttu-id="9c723-151">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9c723-151">Examples</span></span>

<span data-ttu-id="9c723-152">**mdmerge.exe-Metadata \_ dir $ ( \_ ruta de metadatos del SDK \_ )-i $ ( \_ \_ ruta de acceso de metadatos del SDK interno \_ )-o $ (obj \_ path) \\ $O \\ SystemMetadata-v-n:-1-n:Windows.Foundation: 2**</span><span class="sxs-lookup"><span data-stu-id="9c723-152">**mdmerge.exe -metadata\_dir $(SDK\_METADATA\_PATH) -i $(INTERNAL\_SDK\_METADATA\_PATH) -o $(OBJ\_PATH)\\$O\\SystemMetadata -v -n:-1 -n:Windows.Foundation:2**</span></span>

## <a name="requirements"></a><span data-ttu-id="9c723-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c723-153">Requirements</span></span>



| <span data-ttu-id="9c723-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c723-154">Requirement</span></span> | <span data-ttu-id="9c723-155">Value</span><span class="sxs-lookup"><span data-stu-id="9c723-155">Value</span></span> |
|-------------------|--------------------------------|
| <span data-ttu-id="9c723-156">Remoto</span><span class="sxs-lookup"><span data-stu-id="9c723-156">Client</span></span><br/> | <span data-ttu-id="9c723-157">Windows 8</span><span class="sxs-lookup"><span data-stu-id="9c723-157">Windows 8</span></span><br/>           |
| <span data-ttu-id="9c723-158">Servidor</span><span class="sxs-lookup"><span data-stu-id="9c723-158">Server</span></span><br/> | <span data-ttu-id="9c723-159">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c723-159">Windows Server 2012</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c723-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c723-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c723-161">Sintaxis de línea de comandos de MIDL general</span><span class="sxs-lookup"><span data-stu-id="9c723-161">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> </dl>

 

 





