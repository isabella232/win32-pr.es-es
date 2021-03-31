---
title: Win32_RDAllowListFileAssociation (clase)
description: Describe una asociación de tipo de archivo publicada con RemoteApp.
ms.assetid: 80cc8f5e-a7f0-458c-b05b-7822306f839a
ms.tgt_platform: multiple
keywords:
- Win32_RDAllowListFileAssociation clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDAllowListFileAssociation de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDAllowListFileAssociation
- Win32_RDAllowListFileAssociation.ExtName
- Win32_RDAllowListFileAssociation.AppAlias
- Win32_RDAllowListFileAssociation.ProgIdHint
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4acbc74b5b0dab228a5c625863b4fcd0574b5f96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490589"
---
# <a name="win32_rdallowlistfileassociation-class"></a><span data-ttu-id="44407-105">\_Clase Win32 RDAllowListFileAssociation</span><span class="sxs-lookup"><span data-stu-id="44407-105">Win32\_RDAllowListFileAssociation class</span></span>

<span data-ttu-id="44407-106">Describe una asociación de tipo de archivo publicada con RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="44407-106">Describes a published file type association with a RemoteApp.</span></span>

<span data-ttu-id="44407-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="44407-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="44407-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44407-108">Syntax</span></span>

``` syntax
class Win32_RDAllowListFileAssociation
{
  string ExtName;
  string AppAlias;
  string ProgIdHint;
};
```

## <a name="members"></a><span data-ttu-id="44407-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="44407-109">Members</span></span>

<span data-ttu-id="44407-110">La **clase \_ RDAllowListFileAssociation de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="44407-110">The **Win32\_RDAllowListFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="44407-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44407-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="44407-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="44407-112">Properties</span></span>

<span data-ttu-id="44407-113">La **clase \_ RDAllowListFileAssociation de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="44407-113">The **Win32\_RDAllowListFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="44407-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="44407-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44407-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44407-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44407-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44407-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="44407-117">Alias del RemoteApp asociado a la extensión.</span><span class="sxs-lookup"><span data-stu-id="44407-117">Alias of the RemoteApp associated with the extension.</span></span>

</dd> <dt>

<span data-ttu-id="44407-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="44407-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44407-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44407-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44407-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44407-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="44407-121">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="44407-121">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="44407-122">Nombre de la extensión, por ejemplo,. txt.</span><span class="sxs-lookup"><span data-stu-id="44407-122">Name of the extension, for example .txt.</span></span>

</dd> <dt>

<span data-ttu-id="44407-123">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="44407-123">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="44407-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="44407-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="44407-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="44407-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="44407-126">Sugerencia para ayudar a abrir documentos con esta asociación de archivos</span><span class="sxs-lookup"><span data-stu-id="44407-126">Hint to help open documents with this file association</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="44407-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44407-127">Requirements</span></span>



| <span data-ttu-id="44407-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="44407-128">Requirement</span></span> | <span data-ttu-id="44407-129">Value</span><span class="sxs-lookup"><span data-stu-id="44407-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44407-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44407-130">Minimum supported client</span></span><br/> | <span data-ttu-id="44407-131">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="44407-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="44407-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="44407-132">Minimum supported server</span></span><br/> | <span data-ttu-id="44407-133">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="44407-133">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="44407-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="44407-134">Namespace</span></span><br/>                | <span data-ttu-id="44407-135">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="44407-135">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="44407-136">MOF</span><span class="sxs-lookup"><span data-stu-id="44407-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="44407-137"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="44407-137"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="44407-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="44407-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44407-139"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44407-139"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

 





