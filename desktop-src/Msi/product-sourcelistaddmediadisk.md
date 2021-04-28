---
description: 'Método Product.SourceListAddMediaDisk: el método SourceListAddMediaDisk agrega un disco al conjunto de discos registrados. Acepta Diskid, VolumeLabel y DiskPrompt como parámetros. Este método llama a en MsiSourceListAddMediaDisk.'
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Método Product.SourceListAddMediaDisk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4cf5fac906b048930b47a07acb2c04c7243d5bbf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113583"
---
# <a name="productsourcelistaddmediadisk-method"></a><span data-ttu-id="34b34-105">Método Product.SourceListAddMediaDisk</span><span class="sxs-lookup"><span data-stu-id="34b34-105">Product.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="34b34-106">El **método SourceListAddMediaDisk** agrega un disco al conjunto de discos registrados.</span><span class="sxs-lookup"><span data-stu-id="34b34-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="34b34-107">Acepta *Diskid,* *VolumeLabel* y *DiskPrompt como* parámetros.</span><span class="sxs-lookup"><span data-stu-id="34b34-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="34b34-108">Este método llama a [**en MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span><span class="sxs-lookup"><span data-stu-id="34b34-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="34b34-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34b34-109">Syntax</span></span>


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="34b34-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="34b34-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34b34-111">*Diskid*</span><span class="sxs-lookup"><span data-stu-id="34b34-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="34b34-112">Este parámetro proporciona el identificador del disco que se va a agregar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="34b34-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="34b34-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="34b34-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="34b34-114">Este parámetro proporciona la etiqueta del disco que se va a agregar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="34b34-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="34b34-115">Una actualización sobrescribe la etiqueta de volumen existente en el Registro.</span><span class="sxs-lookup"><span data-stu-id="34b34-115">An update overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="34b34-116">Para cambiar solo el símbolo del sistema del disco, obtenga la etiqueta de volumen registrada existente y proséntala junto con el nuevo símbolo del sistema del disco.</span><span class="sxs-lookup"><span data-stu-id="34b34-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="34b34-117">Una cadena vacía para este parámetro registra una cadena vacía (0 bytes de longitud) como etiqueta de volumen.</span><span class="sxs-lookup"><span data-stu-id="34b34-117">An empty string for this parameter registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="34b34-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="34b34-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="34b34-119">Este parámetro proporciona el símbolo del sistema del disco que se va a agregar o actualizar.</span><span class="sxs-lookup"><span data-stu-id="34b34-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="34b34-120">Una actualización sobrescribe el mensaje de disco existente en el Registro.</span><span class="sxs-lookup"><span data-stu-id="34b34-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="34b34-121">Para cambiar solo la etiqueta de volumen, obtenga el mensaje de disco existente del registro y proporcione la nueva etiqueta de volumen.</span><span class="sxs-lookup"><span data-stu-id="34b34-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="34b34-122">Una cadena vacía para este parámetro registra una cadena vacía (0 bytes de longitud) como el símbolo del sistema del disco.</span><span class="sxs-lookup"><span data-stu-id="34b34-122">An empty string for this parameter registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34b34-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="34b34-123">Return value</span></span>

<span data-ttu-id="34b34-124">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="34b34-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="34b34-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34b34-125">Requirements</span></span>



| <span data-ttu-id="34b34-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="34b34-126">Requirement</span></span> | <span data-ttu-id="34b34-127">Valor</span><span class="sxs-lookup"><span data-stu-id="34b34-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34b34-128">Versión</span><span class="sxs-lookup"><span data-stu-id="34b34-128">Version</span></span><br/> | <span data-ttu-id="34b34-129">Windows Installer 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34b34-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="34b34-130">Windows Installer 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="34b34-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="34b34-131">Windows Installer 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000</span><span class="sxs-lookup"><span data-stu-id="34b34-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="34b34-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="34b34-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="34b34-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="34b34-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="34b34-134">IID</span><span class="sxs-lookup"><span data-stu-id="34b34-134">IID</span></span><br/>     | <span data-ttu-id="34b34-135">IID IProduct se define como \_ 000C10A0-0000-0000-C000-00000000046</span><span class="sxs-lookup"><span data-stu-id="34b34-135">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="34b34-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="34b34-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b34-137">**Producto**</span><span class="sxs-lookup"><span data-stu-id="34b34-137">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="34b34-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="34b34-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="34b34-139">No se admite en Windows Installer 2.0 y versiones anteriores</span><span class="sxs-lookup"><span data-stu-id="34b34-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




