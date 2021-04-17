---
description: Recupera el número de veces que se ha suspendido BitLocker.
ms.assetid: B8C87352-62BA-4E5D-A273-CE74F3E1A7A8
title: Método GetSuspendCount de la clase Win32_EncryptableVolume (Activdbg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_EncryptableVolume.GetSuspendCount
api_type:
- COM
api_location:
- Root\CIMV2\Security\MicrosoftVolumeEncryption
ms.openlocfilehash: eb28f019674f39946674399f8931fb63421ef982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688151"
---
# <a name="getsuspendcount-method-of-the-win32_encryptablevolume-class"></a><span data-ttu-id="211ec-103">Método GetSuspendCount de la \_ clase EncryptableVolume de Win32</span><span class="sxs-lookup"><span data-stu-id="211ec-103">GetSuspendCount method of the Win32\_EncryptableVolume class</span></span>

<span data-ttu-id="211ec-104">El método **GetSuspendCount** de la [**clase \_ EncryptableVolume de Win32**](win32-encryptablevolume.md) recupera el número de reinicios antes de que se reanude la protección.</span><span class="sxs-lookup"><span data-stu-id="211ec-104">The **GetSuspendCount** method of the [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) class retrieves the number of reboots before protection will automatically be resumed.</span></span>

## <a name="syntax"></a><span data-ttu-id="211ec-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="211ec-105">Syntax</span></span>


```mof
uint32 GetSuspendCount(
   uint32 SuspendCount
);
```



## <a name="parameters"></a><span data-ttu-id="211ec-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="211ec-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="211ec-107">*SuspendCount*</span><span class="sxs-lookup"><span data-stu-id="211ec-107">*SuspendCount*</span></span> 
</dt> <dd>

<span data-ttu-id="211ec-108">Valor entero comprendido entre 0 y 15.</span><span class="sxs-lookup"><span data-stu-id="211ec-108">An integer value from 0 to 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="211ec-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="211ec-109">Return value</span></span>

<span data-ttu-id="211ec-110">Este método devuelve uno de los siguientes códigos u otro código de error si se produce un error.</span><span class="sxs-lookup"><span data-stu-id="211ec-110">This method returns one of the following codes or another error code if it fails.</span></span>



| <span data-ttu-id="211ec-111">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="211ec-111">Return code</span></span>                                                                                          | <span data-ttu-id="211ec-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="211ec-112">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="211ec-113"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="211ec-113"><dt>**S\_OK**</dt></span></span> </dl>                 | <span data-ttu-id="211ec-114">Método realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="211ec-114">The method was successful.</span></span><br/>                                      |
| <dl> <span data-ttu-id="211ec-115"><dt>**ERROR \_ no \_ admitido**</dt></span><span class="sxs-lookup"><span data-stu-id="211ec-115"><dt>**ERROR\_NOT\_SUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="211ec-116">Se devuelve si el volumen no está suspendido o no es un volumen del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="211ec-116">Returned if the volume is not suspended or is not an OS volume.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="211ec-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="211ec-117">Remarks</span></span>

<span data-ttu-id="211ec-118">Este método solo se aplica al volumen del sistema operativo y solo si realmente se suspende en ese momento.</span><span class="sxs-lookup"><span data-stu-id="211ec-118">This method only applies to the OS volume, and only if it is actually suspended at the time.</span></span> <span data-ttu-id="211ec-119">Si el volumen no está suspendido o no es un volumen del sistema operativo, se devolverá un **error \_ no \_ admitido** .</span><span class="sxs-lookup"><span data-stu-id="211ec-119">If the volume is not suspended or is not an OS volume, **ERROR\_NOT\_SUPPORTED** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="211ec-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="211ec-120">Requirements</span></span>



| <span data-ttu-id="211ec-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="211ec-121">Requirement</span></span> | <span data-ttu-id="211ec-122">Value</span><span class="sxs-lookup"><span data-stu-id="211ec-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="211ec-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="211ec-123">Minimum supported client</span></span><br/> | <span data-ttu-id="211ec-124">Solo aplicaciones Windows 8 Enterprise, Windows 8 Pro \[ Desktop\]</span><span class="sxs-lookup"><span data-stu-id="211ec-124">Windows 8 Enterprise, Windows 8 Pro \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="211ec-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="211ec-125">Minimum supported server</span></span><br/> | <span data-ttu-id="211ec-126">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="211ec-126">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="211ec-127">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="211ec-127">Namespace</span></span><br/>                | <span data-ttu-id="211ec-128">\\MicrosoftVolumeEncryption de \\ seguridad de cimv2 raíz \\</span><span class="sxs-lookup"><span data-stu-id="211ec-128">Root\\CIMV2\\Security\\MicrosoftVolumeEncryption</span></span><br/>                                             |
| <span data-ttu-id="211ec-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="211ec-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="211ec-130"><dt>Activdbg. h</dt></span><span class="sxs-lookup"><span data-stu-id="211ec-130"><dt>Activdbg.h</dt></span></span> </dl>                   |
| <span data-ttu-id="211ec-131">MOF</span><span class="sxs-lookup"><span data-stu-id="211ec-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="211ec-132"><dt>Win32 \_ encryptablevolume. mof</dt></span><span class="sxs-lookup"><span data-stu-id="211ec-132"><dt>Win32\_encryptablevolume.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="211ec-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="211ec-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="211ec-134">**Win32 \_ EncryptableVolume**</span><span class="sxs-lookup"><span data-stu-id="211ec-134">**Win32\_EncryptableVolume**</span></span>](win32-encryptablevolume.md)
</dt> </dl>

 

 




