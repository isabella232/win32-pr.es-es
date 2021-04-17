---
description: La propiedad FileAttributes del objeto Installer devuelve un número que representa los atributos de archivo combinados para la ruta de acceso designada a un archivo o carpeta.
ms.assetid: a09ac346-4e4d-440f-bfbe-ff8fb3f69823
title: Installer. FileAttributes (propiedad, Windows. Storage. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FileAttributes
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e9a4d2b956c7d325fabcda7d6950274249120a0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653337"
---
# <a name="installerfileattributes-property"></a><span data-ttu-id="e98c7-103">Installer. FileAttributes (propiedad)</span><span class="sxs-lookup"><span data-stu-id="e98c7-103">Installer.FileAttributes property</span></span>

<span data-ttu-id="e98c7-104">La propiedad **FileAttributes** del objeto [**Installer**](installer-object.md) devuelve un número que representa los atributos de archivo combinados para la ruta de acceso designada a un archivo o carpeta.</span><span class="sxs-lookup"><span data-stu-id="e98c7-104">The **FileAttributes** property of the [**Installer**](installer-object.md) object returns a number representing the combined file attributes for the designated path to a file or folder.</span></span>

<span data-ttu-id="e98c7-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e98c7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e98c7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e98c7-106">Syntax</span></span>


```JScript
propVal = Installer.FileAttributes
```



## <a name="property-value"></a><span data-ttu-id="e98c7-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e98c7-107">Property value</span></span>

<span data-ttu-id="e98c7-108">La ruta de acceso necesaria para el archivo o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="e98c7-108">The required path to the file or folder.</span></span> <span data-ttu-id="e98c7-109">Una ruta de acceso parcial supone el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="e98c7-109">A partial path assumes the current directory.</span></span>

## <a name="remarks"></a><span data-ttu-id="e98c7-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e98c7-110">Remarks</span></span>

<span data-ttu-id="e98c7-111">La propiedad **FileAttributes** devuelve los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="e98c7-111">The **FileAttributes** property returns the following values.</span></span>



| <span data-ttu-id="e98c7-112">Atributo de archivo</span><span class="sxs-lookup"><span data-stu-id="e98c7-112">File attribute</span></span>              | <span data-ttu-id="e98c7-113">Value</span><span class="sxs-lookup"><span data-stu-id="e98c7-113">Value</span></span>      | <span data-ttu-id="e98c7-114">Value</span><span class="sxs-lookup"><span data-stu-id="e98c7-114">Value</span></span> |
|-----------------------------|------------|-------|
| <span data-ttu-id="e98c7-115">FILE\_ATTRIBUTE\_READONLY</span><span class="sxs-lookup"><span data-stu-id="e98c7-115">FILE\_ATTRIBUTE\_READONLY</span></span>   | <span data-ttu-id="e98c7-116">0x00000001</span><span class="sxs-lookup"><span data-stu-id="e98c7-116">0x00000001</span></span> | <span data-ttu-id="e98c7-117">1</span><span class="sxs-lookup"><span data-stu-id="e98c7-117">1</span></span>     |
| <span data-ttu-id="e98c7-118">FILE\_ATTRIBUTE\_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="e98c7-118">FILE\_ATTRIBUTE\_HIDDEN</span></span>     | <span data-ttu-id="e98c7-119">0x00000002</span><span class="sxs-lookup"><span data-stu-id="e98c7-119">0x00000002</span></span> | <span data-ttu-id="e98c7-120">2</span><span class="sxs-lookup"><span data-stu-id="e98c7-120">2</span></span>     |
| <span data-ttu-id="e98c7-121">FILE\_ATTRIBUTE\_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="e98c7-121">FILE\_ATTRIBUTE\_SYSTEM</span></span>     | <span data-ttu-id="e98c7-122">0x00000004</span><span class="sxs-lookup"><span data-stu-id="e98c7-122">0x00000004</span></span> | <span data-ttu-id="e98c7-123">4</span><span class="sxs-lookup"><span data-stu-id="e98c7-123">4</span></span>     |
| <span data-ttu-id="e98c7-124">FILE\_ATTRIBUTE\_DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="e98c7-124">FILE\_ATTRIBUTE\_DIRECTORY</span></span>  | <span data-ttu-id="e98c7-125">0x00000010</span><span class="sxs-lookup"><span data-stu-id="e98c7-125">0x00000010</span></span> | <span data-ttu-id="e98c7-126">16</span><span class="sxs-lookup"><span data-stu-id="e98c7-126">16</span></span>    |
| <span data-ttu-id="e98c7-127">atributo de archivo \_ \_ temporal</span><span class="sxs-lookup"><span data-stu-id="e98c7-127">FILE\_ATTRIBUTE\_TEMPORARY</span></span>  | <span data-ttu-id="e98c7-128">0x00000100</span><span class="sxs-lookup"><span data-stu-id="e98c7-128">0x00000100</span></span> | <span data-ttu-id="e98c7-129">256</span><span class="sxs-lookup"><span data-stu-id="e98c7-129">256</span></span>   |
| <span data-ttu-id="e98c7-130">FILE\_ATTRIBUTE\_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="e98c7-130">FILE\_ATTRIBUTE\_COMPRESSED</span></span> | <span data-ttu-id="e98c7-131">0x00000800</span><span class="sxs-lookup"><span data-stu-id="e98c7-131">0x00000800</span></span> | <span data-ttu-id="e98c7-132">2048</span><span class="sxs-lookup"><span data-stu-id="e98c7-132">2048</span></span>  |
| <span data-ttu-id="e98c7-133">FILE\_ATTRIBUTE\_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="e98c7-133">FILE\_ATTRIBUTE\_OFFLINE</span></span>    | <span data-ttu-id="e98c7-134">0x00001000</span><span class="sxs-lookup"><span data-stu-id="e98c7-134">0x00001000</span></span> | <span data-ttu-id="e98c7-135">4096</span><span class="sxs-lookup"><span data-stu-id="e98c7-135">4096</span></span>  |



 

<span data-ttu-id="e98c7-136">Devuelve – 1 si el archivo o la carpeta no existen o no se puede obtener acceso a ellos.</span><span class="sxs-lookup"><span data-stu-id="e98c7-136">Returns –1 if the file or folder does not exist or is not accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="e98c7-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e98c7-137">Requirements</span></span>



| <span data-ttu-id="e98c7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="e98c7-138">Requirement</span></span> | <span data-ttu-id="e98c7-139">Value</span><span class="sxs-lookup"><span data-stu-id="e98c7-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e98c7-140">Versión</span><span class="sxs-lookup"><span data-stu-id="e98c7-140">Version</span></span><br/> | <span data-ttu-id="e98c7-141">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e98c7-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e98c7-142">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e98c7-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e98c7-143">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="e98c7-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e98c7-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e98c7-144">Header</span></span><br/>  | <dl> <span data-ttu-id="e98c7-145"><dt>Windows. Storage. h</dt></span><span class="sxs-lookup"><span data-stu-id="e98c7-145"><dt>Windows.storage.h</dt></span></span> </dl>                                                                                                                                                            |
| <span data-ttu-id="e98c7-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e98c7-146">DLL</span></span><br/>     | <dl> <span data-ttu-id="e98c7-147"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e98c7-147"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e98c7-148">IID</span><span class="sxs-lookup"><span data-stu-id="e98c7-148">IID</span></span><br/>     | <span data-ttu-id="e98c7-149">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e98c7-149">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




