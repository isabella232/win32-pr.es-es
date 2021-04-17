---
description: El método SourceListAddSource agrega una red o un origen de dirección URL. Acepta SourcePath, tipo e índice como parámetros. Este método llama a MsiSourceListAddSourceEx.
ms.assetid: 87797a8c-f1ba-4bfb-9296-3d3ef2a3c37f
title: Patch. SourceListAddSource (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cc0a3bc0d966ec6836d1523745b296350562aaa7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653565"
---
# <a name="patchsourcelistaddsource-method"></a><span data-ttu-id="be8ea-105">Patch. SourceListAddSource (método)</span><span class="sxs-lookup"><span data-stu-id="be8ea-105">Patch.SourceListAddSource method</span></span>

<span data-ttu-id="be8ea-106">El método **SourceListAddSource** agrega una red o un origen de dirección URL.</span><span class="sxs-lookup"><span data-stu-id="be8ea-106">The **SourceListAddSource** method adds a network or URL source.</span></span> <span data-ttu-id="be8ea-107">Acepta *SourcePath*, *tipo* e *Índice* como parámetros.</span><span class="sxs-lookup"><span data-stu-id="be8ea-107">Accepts *SourcePath*, *Type* and *Index* as parameters.</span></span> <span data-ttu-id="be8ea-108">Este método llama a [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span><span class="sxs-lookup"><span data-stu-id="be8ea-108">This method calls [**MsiSourceListAddSourceEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa).</span></span>

## <a name="syntax"></a><span data-ttu-id="be8ea-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be8ea-109">Syntax</span></span>


```JScript
Patch.SourceListAddSource(
  Type,
  SourcePath,
  Index
)
```



## <a name="parameters"></a><span data-ttu-id="be8ea-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="be8ea-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be8ea-111">*Tipo*</span><span class="sxs-lookup"><span data-stu-id="be8ea-111">*Type*</span></span> 
</dt> <dd>

<span data-ttu-id="be8ea-112">Tipo de origen que se va a agregar: MSISOURCETYPE \_ Network o MSISOURCETYPE \_ URL.</span><span class="sxs-lookup"><span data-stu-id="be8ea-112">Type of source to be added: MSISOURCETYPE\_NETWORK or MSISOURCETYPE\_URL.</span></span>

</dd> <dt>

<span data-ttu-id="be8ea-113">*SourcePath*</span><span class="sxs-lookup"><span data-stu-id="be8ea-113">*SourcePath*</span></span> 
</dt> <dd>

<span data-ttu-id="be8ea-114">Ruta de acceso al origen que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="be8ea-114">Path to the source to be added.</span></span>

</dd> <dt>

<span data-ttu-id="be8ea-115">*Index*</span><span class="sxs-lookup"><span data-stu-id="be8ea-115">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="be8ea-116">Si se llama a **SourceListAddSource** con un nuevo origen e *Índice* establecido en 0, el instalador agrega el origen al final de la lista de origen.</span><span class="sxs-lookup"><span data-stu-id="be8ea-116">If **SourceListAddSource** is called with a new source and *Index* set to 0, the installer adds the source to the end of the source list.</span></span>

<span data-ttu-id="be8ea-117">Si se llama a esta función con un origen que ya existe en la lista de origen y el *Índice* se establece en 0, el instalador conserva el índice existente del origen.</span><span class="sxs-lookup"><span data-stu-id="be8ea-117">If this function is called with a source already existing in the source list and *Index* is set to 0, the installer retains the source's existing index.</span></span>

<span data-ttu-id="be8ea-118">Si se llama a la función con un origen existente en la lista de origen y el *Índice* se establece en un valor distinto de cero, el origen se quita de su ubicación actual en la lista y se inserta en la posición especificada por el *Índice*, antes de cualquier origen que ya exista en esa posición.</span><span class="sxs-lookup"><span data-stu-id="be8ea-118">If the function is called with an existing source in the source list and *Index* is set to a non-zero value, the source is removed from its current location in the list and inserted at the position specified by *Index*, before any source that already exists at that position.</span></span>

<span data-ttu-id="be8ea-119">Si se llama a la función con un nuevo origen y el *Índice* se establece en un valor distinto de cero, el origen se inserta en la posición especificada por el *Índice*, antes de cualquier origen que ya exista en esa posición.</span><span class="sxs-lookup"><span data-stu-id="be8ea-119">If the function is called with a new source and *Index* is set to a non-zero value, the source is inserted at the position specified by *Index*, before any source that already exists at that position.</span></span> <span data-ttu-id="be8ea-120">El valor de índice de todos los orígenes de la lista después del índice especificado por el *Índice* se actualiza para garantizar que los valores de índice son únicos y se garantiza que el orden existente permanece sin cambios.</span><span class="sxs-lookup"><span data-stu-id="be8ea-120">The index value for all sources in the list after the index specified by *Index* are updated to ensure unique index values and the preexisting order is guaranteed to remain unchanged.</span></span>

<span data-ttu-id="be8ea-121">Si el *Índice* es mayor que el número de orígenes de la lista, el origen se coloca al final de la lista con un valor de índice de uno mayor que cualquier origen existente.</span><span class="sxs-lookup"><span data-stu-id="be8ea-121">If *Index* is greater than the number of sources in the list, the source is placed at the end of the list with an index value one larger than any existing source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be8ea-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="be8ea-122">Return value</span></span>

<span data-ttu-id="be8ea-123">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="be8ea-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="be8ea-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be8ea-124">Requirements</span></span>



| <span data-ttu-id="be8ea-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="be8ea-125">Requirement</span></span> | <span data-ttu-id="be8ea-126">Value</span><span class="sxs-lookup"><span data-stu-id="be8ea-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be8ea-127">Versión</span><span class="sxs-lookup"><span data-stu-id="be8ea-127">Version</span></span><br/> | <span data-ttu-id="be8ea-128">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be8ea-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="be8ea-129">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be8ea-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="be8ea-130">Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="be8ea-130">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="be8ea-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be8ea-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="be8ea-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be8ea-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="be8ea-133">IID</span><span class="sxs-lookup"><span data-stu-id="be8ea-133">IID</span></span><br/>     | <span data-ttu-id="be8ea-134">IID \_ IPatch se define como 000C10A1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="be8ea-134">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="be8ea-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="be8ea-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8ea-136">**Distribución**</span><span class="sxs-lookup"><span data-stu-id="be8ea-136">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="be8ea-137">**MsiSourceListAddSourceEx**</span><span class="sxs-lookup"><span data-stu-id="be8ea-137">**MsiSourceListAddSourceEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourceexa)
</dt> <dt>

[<span data-ttu-id="be8ea-138">No se admite en Windows Installer 2,0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="be8ea-138">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




