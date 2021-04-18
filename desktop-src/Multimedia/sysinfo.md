---
title: sysinfo (comando)
description: El comando sysinfo recupera información del sistema MCI. El comando sysinfo es un comando del sistema MCI; lo interpreta directamente MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- comando de sysinfo Windows multimedia
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666075"
---
# <a name="sysinfo-command"></a><span data-ttu-id="a723d-105">sysinfo (comando)</span><span class="sxs-lookup"><span data-stu-id="a723d-105">sysinfo command</span></span>

<span data-ttu-id="a723d-106">El comando sysinfo recupera información del sistema MCI.</span><span class="sxs-lookup"><span data-stu-id="a723d-106">The sysinfo command retrieves MCI system information.</span></span> <span data-ttu-id="a723d-107">El comando sysinfo es un comando del sistema MCI; lo interpreta directamente MCI.</span><span class="sxs-lookup"><span data-stu-id="a723d-107">The sysinfo command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="a723d-108">Para enviar este comando, llame a la función [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con el parámetro *lpszCommand* establecido como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="a723d-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a723d-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a723d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a723d-110">*lpszDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a723d-110">*lpszDeviceID*</span></span> 
</dt> <dd>

<span data-ttu-id="a723d-111">Identificador de un dispositivo MCI o de un tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a723d-111">Identifier of an MCI device or device type.</span></span> <span data-ttu-id="a723d-112">Si se especifica un tipo de dispositivo, debe ser un nombre de tipo de dispositivo MCI estándar, tal y como se muestra en el material de referencia del comando [**Capability**](capability.md) .</span><span class="sxs-lookup"><span data-stu-id="a723d-112">If a device type is specified, it must be a standard MCI device-type name, as listed in the reference material for the [**capability**](capability.md) command.</span></span> <span data-ttu-id="a723d-113">Puede especificar "All" cuando la marca especificada en *lpszRequest* permite esa posibilidad.</span><span class="sxs-lookup"><span data-stu-id="a723d-113">You can specify "all" when the flag specified in *lpszRequest* allows that possibility.</span></span>

</dd> <dt>

<span data-ttu-id="a723d-114">*lpszRequest*</span><span class="sxs-lookup"><span data-stu-id="a723d-114">*lpszRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="a723d-115">Una de las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="a723d-115">One of the following flags.</span></span>



| <span data-ttu-id="a723d-116">Value</span><span class="sxs-lookup"><span data-stu-id="a723d-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="a723d-117">Significado</span><span class="sxs-lookup"><span data-stu-id="a723d-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <span data-ttu-id="a723d-118"><dt>**installname**</dt></span><span class="sxs-lookup"><span data-stu-id="a723d-118"><dt>**installname**</dt></span></span> </dl>               | <span data-ttu-id="a723d-119">Devuelve el nombre que aparece en el registro o el archivo de SYSTEM.INI que se usa para instalar el dispositivo abierto con el identificador de dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a723d-119">Returns the name listed in the registry or the SYSTEM.INI file used to install the open device with the specified device identifier.</span></span><br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <span data-ttu-id="a723d-120"><dt>**volumen**</dt></span><span class="sxs-lookup"><span data-stu-id="a723d-120"><dt>**quantity**</dt></span></span> </dl>                        | <span data-ttu-id="a723d-121">Devuelve el número de dispositivos MCI que aparecen en el registro o el archivo SYSTEM.INI del tipo especificado en el parámetro *lpszDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="a723d-121">Returns the number of MCI devices listed in the registry or the SYSTEM.INI file of the type specified in the *lpszDeviceID* parameter.</span></span> <span data-ttu-id="a723d-122">Este identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar.</span><span class="sxs-lookup"><span data-stu-id="a723d-122">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="a723d-123">Se omite cualquier dígito después del tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a723d-123">Any digits after the device type are ignored.</span></span> <span data-ttu-id="a723d-124">Si se especifica "All" para *lpszDeviceID* , se devuelve el número total de dispositivos MCI en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a723d-124">Specifying "all" for *lpszDeviceID* returns the total number of MCI devices in the system.</span></span><br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <span data-ttu-id="a723d-125"><dt>**cantidad abierta**</dt></span><span class="sxs-lookup"><span data-stu-id="a723d-125"><dt>**quantity open**</dt></span></span> </dl>         | <span data-ttu-id="a723d-126">Devuelve el número de dispositivos MCI abiertos del tipo especificado en *lpszDeviceID*.</span><span class="sxs-lookup"><span data-stu-id="a723d-126">Returns the number of open MCI devices of the type specified in *lpszDeviceID*.</span></span> <span data-ttu-id="a723d-127">Este identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar.</span><span class="sxs-lookup"><span data-stu-id="a723d-127">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="a723d-128">Si se especifica "All" para *lpszDeviceID* , se devuelve el número total de dispositivos MCI abiertos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a723d-128">Specifying "all" for *lpszDeviceID* returns the total number of open MCI devices in the system.</span></span><br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <span data-ttu-id="a723d-129"><dt>\* \* Nombre \* Índice \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a723d-129"><dt>\*\*name \*index\*\*\*</dt></span></span> </dl>                | <span data-ttu-id="a723d-130">Devuelve el nombre de un dispositivo MCI.</span><span class="sxs-lookup"><span data-stu-id="a723d-130">Returns the name of an MCI device.</span></span> <span data-ttu-id="a723d-131">El identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar.</span><span class="sxs-lookup"><span data-stu-id="a723d-131">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="a723d-132">El *Índice* va de 1 al número de dispositivos de ese tipo.</span><span class="sxs-lookup"><span data-stu-id="a723d-132">The *index* ranges from 1 to the number of devices of that type.</span></span> <span data-ttu-id="a723d-133">Si se especifica "All" para *lpszDeviceID*, *index* va de 1 al número total de dispositivos del sistema.</span><span class="sxs-lookup"><span data-stu-id="a723d-133">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of devices in the system.</span></span><br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <span data-ttu-id="a723d-134"><dt>**nombre del *Índice* abierto**</dt></span><span class="sxs-lookup"><span data-stu-id="a723d-134"><dt>**name *index* open**</dt></span></span> </dl> | <span data-ttu-id="a723d-135">Devuelve el nombre de un dispositivo MCI abierto.</span><span class="sxs-lookup"><span data-stu-id="a723d-135">Returns the name of an open MCI device.</span></span> <span data-ttu-id="a723d-136">El identificador de dispositivo debe ser un nombre de tipo de dispositivo MCI estándar.</span><span class="sxs-lookup"><span data-stu-id="a723d-136">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="a723d-137">El *Índice* va de 1 al número de dispositivos abiertos de ese tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a723d-137">The *index* ranges from 1 to the number of open devices of that device type.</span></span> <span data-ttu-id="a723d-138">Si se especifica "All" para *lpszDeviceID*, *index* va de 1 al número total de dispositivos abiertos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="a723d-138">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of open devices in the system.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="a723d-139">*lpszFlags*</span><span class="sxs-lookup"><span data-stu-id="a723d-139">*lpszFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="a723d-140">Puede ser "Wait", "Notify" o ambos.</span><span class="sxs-lookup"><span data-stu-id="a723d-140">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="a723d-141">En el caso de los dispositivos de vídeo digital y vídeo, también se puede especificar "prueba".</span><span class="sxs-lookup"><span data-stu-id="a723d-141">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="a723d-142">Para obtener más información acerca de estas marcas, vea [las marcas wait, Notify y test](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a723d-142">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a723d-143">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a723d-143">Examples</span></span>

<span data-ttu-id="a723d-144">El siguiente comando devuelve el número de dispositivos de audio de onda de onda abiertos.</span><span class="sxs-lookup"><span data-stu-id="a723d-144">The following command returns the number of open waveform-audio devices.</span></span>

``` syntax
sysinfo waveaudio quantity open
```

<span data-ttu-id="a723d-145">El siguiente comando devuelve el nombre (alias de dispositivo) del primer dispositivo de audio de onda abierto.</span><span class="sxs-lookup"><span data-stu-id="a723d-145">The following command returns the name (device alias) of the first open waveform-audio device.</span></span>

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a><span data-ttu-id="a723d-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a723d-146">Requirements</span></span>



| <span data-ttu-id="a723d-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="a723d-147">Requirement</span></span> | <span data-ttu-id="a723d-148">Value</span><span class="sxs-lookup"><span data-stu-id="a723d-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a723d-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a723d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="a723d-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a723d-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a723d-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a723d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="a723d-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a723d-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a723d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="a723d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a723d-154">MCI</span><span class="sxs-lookup"><span data-stu-id="a723d-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a723d-155">Cadenas de comandos MCI</span><span class="sxs-lookup"><span data-stu-id="a723d-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="a723d-156">**pueda**</span><span class="sxs-lookup"><span data-stu-id="a723d-156">**capability**</span></span>](capability.md)
</dt> </dl>

 

