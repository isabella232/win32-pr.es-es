---
title: Comando MCI_SYSINFO (mmsystem. h)
description: El comando de MCI \_ SYSINFO recupera información acerca de los dispositivos MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- Comando de MCI_SYSINFO de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996501"
---
# <a name="mci_sysinfo-command"></a><span data-ttu-id="a1e20-104">MCI \_ SYSINFO (comando)</span><span class="sxs-lookup"><span data-stu-id="a1e20-104">MCI\_SYSINFO command</span></span>

<span data-ttu-id="a1e20-105">El comando de MCI \_ SYSINFO recupera información acerca de los dispositivos MCI.</span><span class="sxs-lookup"><span data-stu-id="a1e20-105">The MCI\_SYSINFO command retrieves information about MCI devices.</span></span> <span data-ttu-id="a1e20-106">MCI admite este comando directamente en lugar de pasarlo al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1e20-106">MCI supports this command directly rather than passing it to the device.</span></span> <span data-ttu-id="a1e20-107">Cualquier aplicación MCI puede usar este comando.</span><span class="sxs-lookup"><span data-stu-id="a1e20-107">Any MCI application can use this command.</span></span> <span data-ttu-id="a1e20-108">La información de cadena se devuelve en el búfer proporcionado por la aplicación al que apunta el miembro **lpstrReturn** de la estructura identificada por *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="a1e20-108">String information is returned in the application-supplied buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span> <span data-ttu-id="a1e20-109">La información numérica se devuelve como un valor **DWORD** colocado en el búfer proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a1e20-109">Numeric information is returned as a **DWORD** value placed in the application-supplied buffer.</span></span> <span data-ttu-id="a1e20-110">El miembro **dwRetSize** especifica la longitud del búfer.</span><span class="sxs-lookup"><span data-stu-id="a1e20-110">The **dwRetSize** member specifies the buffer length.</span></span>

<span data-ttu-id="a1e20-111">Para enviar este comando, llame a la función [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) con los parámetros siguientes.</span><span class="sxs-lookup"><span data-stu-id="a1e20-111">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a1e20-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1e20-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1e20-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span><span class="sxs-lookup"><span data-stu-id="a1e20-113"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a1e20-114">Identificador de dispositivo del dispositivo MCI que va a recibir el mensaje de comando.</span><span class="sxs-lookup"><span data-stu-id="a1e20-114">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a1e20-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a1e20-115"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a1e20-116">Una o varias de las siguientes marcas estándar y específicas del comando:</span><span class="sxs-lookup"><span data-stu-id="a1e20-116">One or more of the following standard and command-specific flags:</span></span>

</dd> <dt>

<span data-ttu-id="a1e20-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI \_ SYSINFO \_ INSTALLNAME</span><span class="sxs-lookup"><span data-stu-id="a1e20-117"><span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI\_SYSINFO\_INSTALLNAME</span></span>
</dt> <dd>

<span data-ttu-id="a1e20-118">Obtiene el nombre (que aparece en el registro o en el archivo SYSTEM.INI) usado para instalar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a1e20-118">Obtains the name (listed in the registry or the SYSTEM.INI file) used to install the device.</span></span>

</dd> <dt>

<span data-ttu-id="a1e20-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>nombre de MCI \_ SYSINFO \_</span><span class="sxs-lookup"><span data-stu-id="a1e20-119"><span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>MCI\_SYSINFO\_NAME</span></span>
</dt> <dd>

<span data-ttu-id="a1e20-120">Obtiene un nombre de dispositivo correspondiente al número de dispositivo especificado en el miembro **dwNumber** de la estructura identificada por **lpSysInfo**.</span><span class="sxs-lookup"><span data-stu-id="a1e20-120">Obtains a device name corresponding to the device number specified in the **dwNumber** member of the structure identified by **lpSysInfo**.</span></span> <span data-ttu-id="a1e20-121">Si \_ \_ se establece la marca de apertura de MCI SYSINFO, MCI devuelve los nombres de los dispositivos abiertos.</span><span class="sxs-lookup"><span data-stu-id="a1e20-121">If the MCI\_SYSINFO\_OPEN flag is set, MCI returns the names of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="a1e20-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI \_ SYSINFO \_ abierto</span><span class="sxs-lookup"><span data-stu-id="a1e20-122"><span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI\_SYSINFO\_OPEN</span></span>
</dt> <dd>

<span data-ttu-id="a1e20-123">Obtiene la cantidad o el nombre de los dispositivos abiertos.</span><span class="sxs-lookup"><span data-stu-id="a1e20-123">Obtains the quantity or name of open devices.</span></span>

</dd> <dt>

<span data-ttu-id="a1e20-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>cantidad de MCI \_ SYSINFO \_</span><span class="sxs-lookup"><span data-stu-id="a1e20-124"><span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>MCI\_SYSINFO\_QUANTITY</span></span>
</dt> <dd>

<span data-ttu-id="a1e20-125">Obtiene el número de dispositivos del tipo especificado que se enumeran en el registro o en la \[ \] sección MCI del archivo de SYSTEM.INI.</span><span class="sxs-lookup"><span data-stu-id="a1e20-125">Obtains the number of devices of the specified type that are listed in the registry or the \[mci\] section of the SYSTEM.INI file.</span></span> <span data-ttu-id="a1e20-126">Si \_ \_ se establece la marca de apertura de MCI SYSINFO, se devuelve el número de dispositivos abiertos.</span><span class="sxs-lookup"><span data-stu-id="a1e20-126">If the MCI\_SYSINFO\_OPEN flag is set, the number of open devices is returned.</span></span>

</dd> <dt>

<span data-ttu-id="a1e20-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span><span class="sxs-lookup"><span data-stu-id="a1e20-127"><span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*</span></span>
</dt> <dd>

<span data-ttu-id="a1e20-128">Puntero a una [**estructura \_ \_ parms de MCI SYSINFO**](mci-sysinfo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a1e20-128">Pointer to an [**MCI\_SYSINFO\_PARMS**](mci-sysinfo-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1e20-129">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1e20-129">Return Value</span></span>

<span data-ttu-id="a1e20-130">Devuelve cero si es correcto o un error en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="a1e20-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1e20-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1e20-131">Remarks</span></span>

<span data-ttu-id="a1e20-132">El miembro **wDeviceType** de la estructura identificada por *lpSysInfo* se usa para indicar el tipo de dispositivo de la consulta.</span><span class="sxs-lookup"><span data-stu-id="a1e20-132">The **wDeviceType** member of the structure identified by *lpSysInfo* is used to indicate the device type of the query.</span></span> <span data-ttu-id="a1e20-133">Si el parámetro *wDeviceID* se establece en MCI \_ All \_ Device \_ ID, invalida el valor de **wDeviceType**.</span><span class="sxs-lookup"><span data-stu-id="a1e20-133">If the *wDeviceID* parameter is set to MCI\_ALL\_DEVICE\_ID, it overrides the value of **wDeviceType**.</span></span> <span data-ttu-id="a1e20-134">Para obtener una lista de tipos de dispositivos, consulte [tipos de dispositivos MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="a1e20-134">For a list of device types, see [MCI Device Types](mci-device-types.md).</span></span>

<span data-ttu-id="a1e20-135">Los valores devueltos de tipo entero son valores **DWORD** devueltos en el búfer señalado por el miembro **lpstrReturn** de la estructura identificada por *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="a1e20-135">Integer return values are **DWORD** values returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

<span data-ttu-id="a1e20-136">Los valores devueltos de cadena son cadenas terminadas en NULL devueltas en el búfer señalado por el miembro **lpstrReturn** de la estructura identificada por *lpSysInfo*.</span><span class="sxs-lookup"><span data-stu-id="a1e20-136">String return values are null-terminated strings returned in the buffer pointed to by the **lpstrReturn** member of the structure identified by *lpSysInfo*.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1e20-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1e20-137">Requirements</span></span>



| <span data-ttu-id="a1e20-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1e20-138">Requirement</span></span> | <span data-ttu-id="a1e20-139">Value</span><span class="sxs-lookup"><span data-stu-id="a1e20-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1e20-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1e20-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a1e20-141">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a1e20-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a1e20-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1e20-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a1e20-143">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1e20-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a1e20-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1e20-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1e20-145"><dt>Mmsystem. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1e20-145"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1e20-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1e20-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1e20-147">MCI</span><span class="sxs-lookup"><span data-stu-id="a1e20-147">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a1e20-148">Comandos MCI</span><span class="sxs-lookup"><span data-stu-id="a1e20-148">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

