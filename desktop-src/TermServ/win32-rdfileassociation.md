---
title: Win32_RDFileAssociation (clase)
description: Representa una asociación de tipo de archivo para RemoteApp.
ms.assetid: 9ecf6fa5-36f0-4b37-9d59-781b41c1d90c
ms.tgt_platform: multiple
keywords:
- Win32_RDFileAssociation clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDFileAssociation de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDFileAssociation
- Win32_RDFileAssociation.ExtName
- Win32_RDFileAssociation.ProgIdHint
- Win32_RDFileAssociation.IconPath
- Win32_RDFileAssociation.IconIndex
- Win32_RDFileAssociation.IconContents
- Win32_RDFileAssociation.PrimaryHandler
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac64cd38bdad748c64fe6f52cb7a6da8d8220cba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996255"
---
# <a name="win32_rdfileassociation-class"></a><span data-ttu-id="fbf73-105">\_Clase Win32 RDFileAssociation</span><span class="sxs-lookup"><span data-stu-id="fbf73-105">Win32\_RDFileAssociation class</span></span>

<span data-ttu-id="fbf73-106">Representa una asociación de tipo de archivo para RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="fbf73-106">Represents a file type association for a RemoteApp.</span></span>

<span data-ttu-id="fbf73-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fbf73-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf73-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbf73-108">Syntax</span></span>

``` syntax
class Win32_RDFileAssociation
{
  string  ExtName;
  string  ProgIdHint;
  string  IconPath;
  sint32  IconIndex;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="fbf73-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fbf73-109">Members</span></span>

<span data-ttu-id="fbf73-110">La **clase \_ RDFileAssociation de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fbf73-110">The **Win32\_RDFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="fbf73-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbf73-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fbf73-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbf73-112">Properties</span></span>

<span data-ttu-id="fbf73-113">La **clase \_ RDFileAssociation de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fbf73-113">The **Win32\_RDFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fbf73-114">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="fbf73-114">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf73-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf73-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf73-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf73-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf73-117">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="fbf73-117">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fbf73-118">Nombre de la extensión de nombre de archivo, por ejemplo,. txt.</span><span class="sxs-lookup"><span data-stu-id="fbf73-118">The name of the file name extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="fbf73-119">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="fbf73-119">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf73-120">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="fbf73-120">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf73-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf73-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf73-122">Contenido del icono para esta asociación de archivo.</span><span class="sxs-lookup"><span data-stu-id="fbf73-122">The contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="fbf73-123">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="fbf73-123">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf73-124">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="fbf73-124">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="fbf73-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf73-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf73-126">Índice del icono del archivo.</span><span class="sxs-lookup"><span data-stu-id="fbf73-126">The index of the icon in the file.</span></span>

</dd> <dt>

<span data-ttu-id="fbf73-127">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="fbf73-127">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf73-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf73-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf73-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf73-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf73-130">Ruta de acceso del archivo al icono de esta asociación de archivo.</span><span class="sxs-lookup"><span data-stu-id="fbf73-130">The file path to the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="fbf73-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="fbf73-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf73-132">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fbf73-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbf73-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf73-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf73-134">Indica si esta asociación es para un controlador principal.</span><span class="sxs-lookup"><span data-stu-id="fbf73-134">Indicates whether this association is for a primary handler.</span></span>

</dd> <dt>

<span data-ttu-id="fbf73-135">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="fbf73-135">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf73-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf73-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf73-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf73-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf73-138">La sugerencia para ayudar a abrir documentos con esta asociación de archivo.</span><span class="sxs-lookup"><span data-stu-id="fbf73-138">The Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbf73-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbf73-139">Requirements</span></span>



| <span data-ttu-id="fbf73-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbf73-140">Requirement</span></span> | <span data-ttu-id="fbf73-141">Value</span><span class="sxs-lookup"><span data-stu-id="fbf73-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf73-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbf73-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf73-143">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="fbf73-143">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fbf73-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbf73-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf73-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fbf73-145">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="fbf73-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fbf73-146">Namespace</span></span><br/>                | <span data-ttu-id="fbf73-147">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fbf73-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fbf73-148">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf73-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf73-149"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbf73-149"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="fbf73-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fbf73-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf73-151"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbf73-151"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





