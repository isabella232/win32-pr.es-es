---
title: Win32_TSVmMetadataAssociation (clase)
description: Representa una asociación entre un Escritorio remoto máquina virtual y sus propiedades de metadatos.
ms.assetid: 374b1a29-78de-45fd-97b3-c5a5b724e66b
ms.tgt_platform: multiple
keywords:
- Win32_TSVmMetadataAssociation clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSVmMetadataAssociation de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSVmMetadataAssociation
- Win32_TSVmMetadataAssociation.TSVm
- Win32_TSVmMetadataAssociation.MetadataItem
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db3a68c20553eaf52903471d19df9df169ecde21
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676574"
---
# <a name="win32_tsvmmetadataassociation-class"></a><span data-ttu-id="cf771-105">\_Clase Win32 TSVmMetadataAssociation</span><span class="sxs-lookup"><span data-stu-id="cf771-105">Win32\_TSVmMetadataAssociation class</span></span>

<span data-ttu-id="cf771-106">Representa una asociación entre un Escritorio remoto máquina virtual y sus propiedades de metadatos.</span><span class="sxs-lookup"><span data-stu-id="cf771-106">Represents an association between a Remote Desktop virtual machine and its metadata properties.</span></span>

<span data-ttu-id="cf771-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="cf771-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf771-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cf771-108">Syntax</span></span>

``` syntax
[dynamic, Association, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVmMetadataAssociation
{
  Win32_TSVm             REF TSVm;
  Win32_TSVmMetadataItem REF MetadataItem;
};
```

## <a name="members"></a><span data-ttu-id="cf771-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="cf771-109">Members</span></span>

<span data-ttu-id="cf771-110">La **clase \_ TSVmMetadataAssociation de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="cf771-110">The **Win32\_TSVmMetadataAssociation** class has these types of members:</span></span>

-   [<span data-ttu-id="cf771-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf771-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cf771-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cf771-112">Properties</span></span>

<span data-ttu-id="cf771-113">La **clase \_ TSVmMetadataAssociation de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="cf771-113">The **Win32\_TSVmMetadataAssociation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cf771-114">**MetadataItem**</span><span class="sxs-lookup"><span data-stu-id="cf771-114">**MetadataItem**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf771-115">Tipo de datos: **[ **Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span><span class="sxs-lookup"><span data-stu-id="cf771-115">Data type: **[**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cf771-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cf771-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="cf771-117">Instancia de la clase [**Win32 \_ TSVmMetadataItem**](win32-tsvmmetadataitem.md) que representa los metadatos de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cf771-117">An instance of the [**Win32\_TSVmMetadataItem**](win32-tsvmmetadataitem.md) class that represents the metadata for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="cf771-118">**TSVm**</span><span class="sxs-lookup"><span data-stu-id="cf771-118">**TSVm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cf771-119">Tipo de datos: **[ **Win32 \_ TSVm**](win32-tsvm.md)**</span><span class="sxs-lookup"><span data-stu-id="cf771-119">Data type: **[**Win32\_TSVm**](win32-tsvm.md)**</span></span>
</dt> <dt>

<span data-ttu-id="cf771-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="cf771-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cf771-121">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="cf771-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="cf771-122">Instancia de la clase [**Win32 \_ TSVm**](win32-tsvm.md) que representa la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="cf771-122">An instance of the [**Win32\_TSVm**](win32-tsvm.md) class that represents the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf771-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf771-123">Requirements</span></span>



| <span data-ttu-id="cf771-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf771-124">Requirement</span></span> | <span data-ttu-id="cf771-125">Value</span><span class="sxs-lookup"><span data-stu-id="cf771-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf771-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf771-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cf771-127">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="cf771-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="cf771-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cf771-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cf771-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cf771-129">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="cf771-130">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="cf771-130">Namespace</span></span><br/>                | <span data-ttu-id="cf771-131">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cf771-131">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="cf771-132">MOF</span><span class="sxs-lookup"><span data-stu-id="cf771-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf771-133"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cf771-133"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="cf771-134">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="cf771-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf771-135"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf771-135"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

