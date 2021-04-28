---
description: 'Método Patch.SourceListAddMediaDisk: el método SourceListAddMediaDisk agrega un disco al conjunto de discos registrados. Acepta Diskid, VolumeLabel y DiskPrompt como parámetros. Este método llama a en MsiSourceListAddMediaDisk.'
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Método Patch.SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 052831befb95976358b53d989db36d5b2fa43efe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084383"
---
# <a name="patchsourcelistaddmediadisk-method"></a><span data-ttu-id="243c4-105">Método Patch.SourceListAddMediaDisk</span><span class="sxs-lookup"><span data-stu-id="243c4-105">Patch.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="243c4-106">El **método SourceListAddMediaDisk** agrega un disco al conjunto de discos registrados.</span><span class="sxs-lookup"><span data-stu-id="243c4-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="243c4-107">Acepta *Diskid,* *VolumeLabel* y *DiskPrompt como* parámetros.</span><span class="sxs-lookup"><span data-stu-id="243c4-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="243c4-108">Este método llama a [**en MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span><span class="sxs-lookup"><span data-stu-id="243c4-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="243c4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="243c4-109">Syntax</span></span>


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="243c4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="243c4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="243c4-111">*Diskid*</span><span class="sxs-lookup"><span data-stu-id="243c4-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="243c4-112">Este parámetro proporciona el identificador del disco que se va a agregar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="243c4-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="243c4-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="243c4-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="243c4-114">Este parámetro proporciona la etiqueta del disco que se va a agregar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="243c4-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="243c4-115">Una actualización sobrescribe la etiqueta de volumen existente en el Registro.</span><span class="sxs-lookup"><span data-stu-id="243c4-115">An update, overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="243c4-116">Para cambiar solo el símbolo del sistema del disco, obtenga la etiqueta de volumen registrada existente y proséntala junto con el nuevo símbolo del sistema del disco.</span><span class="sxs-lookup"><span data-stu-id="243c4-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="243c4-117">Una cadena NULL o vacía registra una cadena vacía (0 bytes de longitud) como etiqueta de volumen.</span><span class="sxs-lookup"><span data-stu-id="243c4-117">A NULL or empty string registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="243c4-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="243c4-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="243c4-119">Este parámetro proporciona el símbolo del sistema del disco que se va a agregar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="243c4-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="243c4-120">Una actualización sobrescribe el mensaje de disco existente en el Registro.</span><span class="sxs-lookup"><span data-stu-id="243c4-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="243c4-121">Para cambiar solo la etiqueta de volumen, obtenga el mensaje de disco existente del registro y proporcione la nueva etiqueta de volumen.</span><span class="sxs-lookup"><span data-stu-id="243c4-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="243c4-122">Una cadena NULL o vacía registra una cadena vacía (0 bytes de longitud) como símbolo del sistema del disco.</span><span class="sxs-lookup"><span data-stu-id="243c4-122">A NULL or empty string registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="243c4-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="243c4-123">Return value</span></span>

<span data-ttu-id="243c4-124">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="243c4-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="243c4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="243c4-125">Requirements</span></span>



| <span data-ttu-id="243c4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="243c4-126">Requirement</span></span> | <span data-ttu-id="243c4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="243c4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="243c4-128">Versión</span><span class="sxs-lookup"><span data-stu-id="243c4-128">Version</span></span><br/> | <span data-ttu-id="243c4-129">Windows Installer 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="243c4-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="243c4-130">Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="243c4-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="243c4-131">Windows Installer 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="243c4-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="243c4-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="243c4-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="243c4-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="243c4-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="243c4-134">IID</span><span class="sxs-lookup"><span data-stu-id="243c4-134">IID</span></span><br/>     | <span data-ttu-id="243c4-135">IID IPatch se define como \_ 000C10A1-0000-0000-C000-00000000046</span><span class="sxs-lookup"><span data-stu-id="243c4-135">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="243c4-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="243c4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="243c4-137">**Parche**</span><span class="sxs-lookup"><span data-stu-id="243c4-137">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="243c4-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="243c4-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="243c4-139">No se admite en Windows Installer 2.0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="243c4-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




