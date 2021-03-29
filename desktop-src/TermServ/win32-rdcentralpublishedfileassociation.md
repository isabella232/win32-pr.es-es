---
title: Win32_RDCentralPublishedFileAssociation (clase)
description: Información de una extensión de archivo asociada a una aplicación.
ms.assetid: ba12d933-572c-48d3-bf0f-1c99de61457d
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFileAssociation clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDCentralPublishedFileAssociation de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFileAssociation
- Win32_RDCentralPublishedFileAssociation.ExtName
- Win32_RDCentralPublishedFileAssociation.AppAlias
- Win32_RDCentralPublishedFileAssociation.FarmAlias
- Win32_RDCentralPublishedFileAssociation.ProgIdHint
- Win32_RDCentralPublishedFileAssociation.IconContents
- Win32_RDCentralPublishedFileAssociation.PrimaryHandler
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65a0f1c9bf7905504ee3aa2ba6fff7e9804f4747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492742"
---
# <a name="win32_rdcentralpublishedfileassociation-class"></a><span data-ttu-id="5395e-105">\_Clase Win32 RDCentralPublishedFileAssociation</span><span class="sxs-lookup"><span data-stu-id="5395e-105">Win32\_RDCentralPublishedFileAssociation class</span></span>

<span data-ttu-id="5395e-106">Información de una extensión de archivo asociada a una aplicación</span><span class="sxs-lookup"><span data-stu-id="5395e-106">Info for a file extension associated with an application</span></span>

<span data-ttu-id="5395e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5395e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5395e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5395e-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedFileAssociation
{
  string  ExtName;
  string  AppAlias;
  string  FarmAlias;
  string  ProgIdHint;
  uint8   IconContents[];
  boolean PrimaryHandler;
};
```

## <a name="members"></a><span data-ttu-id="5395e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="5395e-109">Members</span></span>

<span data-ttu-id="5395e-110">La **clase \_ RDCentralPublishedFileAssociation de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5395e-110">The **Win32\_RDCentralPublishedFileAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="5395e-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5395e-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5395e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5395e-112">Properties</span></span>

<span data-ttu-id="5395e-113">La **clase \_ RDCentralPublishedFileAssociation de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5395e-113">The **Win32\_RDCentralPublishedFileAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5395e-114">**AppAlias**</span><span class="sxs-lookup"><span data-stu-id="5395e-114">**AppAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5395e-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5395e-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5395e-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5395e-116">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5395e-117">Alias del RemoteApp de la Asociación de archivo.</span><span class="sxs-lookup"><span data-stu-id="5395e-117">Alias of the file association's RemoteApp.</span></span>

</dd> <dt>

<span data-ttu-id="5395e-118">**ExtName**</span><span class="sxs-lookup"><span data-stu-id="5395e-118">**ExtName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5395e-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5395e-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5395e-120">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5395e-120">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5395e-121">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5395e-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5395e-122">Nombre de la extensión (por ejemplo,. txt).</span><span class="sxs-lookup"><span data-stu-id="5395e-122">Name of the extension (e.g. .txt).</span></span>

</dd> <dt>

<span data-ttu-id="5395e-123">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="5395e-123">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5395e-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5395e-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5395e-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5395e-125">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5395e-126">Alias de la granja de RemoteApp's de la Asociación de archivo</span><span class="sxs-lookup"><span data-stu-id="5395e-126">Alias of the file association's RemoteApp's Farm</span></span>

</dd> <dt>

<span data-ttu-id="5395e-127">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="5395e-127">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5395e-128">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="5395e-128">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="5395e-129">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5395e-129">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5395e-130">Contenido del icono para esta asociación de archivo.</span><span class="sxs-lookup"><span data-stu-id="5395e-130">Contents of the icon for this file association.</span></span>

</dd> <dt>

<span data-ttu-id="5395e-131">**PrimaryHandler**</span><span class="sxs-lookup"><span data-stu-id="5395e-131">**PrimaryHandler**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5395e-132">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="5395e-132">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5395e-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5395e-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5395e-134">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="5395e-134">Reserved for future use.</span></span> <span data-ttu-id="5395e-135">Siempre será **true**.</span><span class="sxs-lookup"><span data-stu-id="5395e-135">Will always be **true**.</span></span>

</dd> <dt>

<span data-ttu-id="5395e-136">**ProgIdHint**</span><span class="sxs-lookup"><span data-stu-id="5395e-136">**ProgIdHint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5395e-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5395e-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5395e-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5395e-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5395e-139">Sugerencia para ayudar a abrir documentos con esta asociación de archivo.</span><span class="sxs-lookup"><span data-stu-id="5395e-139">Hint to help open documents with this file association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5395e-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5395e-140">Requirements</span></span>



| <span data-ttu-id="5395e-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="5395e-141">Requirement</span></span> | <span data-ttu-id="5395e-142">Value</span><span class="sxs-lookup"><span data-stu-id="5395e-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5395e-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5395e-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5395e-144">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5395e-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="5395e-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5395e-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5395e-146">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5395e-146">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="5395e-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5395e-147">Namespace</span></span><br/>                | <span data-ttu-id="5395e-148">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5395e-148">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="5395e-149">MOF</span><span class="sxs-lookup"><span data-stu-id="5395e-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5395e-150"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5395e-150"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="5395e-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5395e-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5395e-152"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5395e-152"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

