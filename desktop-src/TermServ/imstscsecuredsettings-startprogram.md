---
title: Propiedad StartProgram de IMsTscSecuredSettings
description: Especifica el programa que se va a iniciar en el servidor remoto en el momento de la conexión.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad StartProgram
- Propiedad StartProgram Servicios de Escritorio remoto, interfaz IMsTscSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsTscSecuredSettings, propiedad StartProgram
- Propiedad StartProgram Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings, propiedad StartProgram
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686210"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a><span data-ttu-id="2099d-108">IMsTscSecuredSettings:: StartProgram (propiedad)</span><span class="sxs-lookup"><span data-stu-id="2099d-108">IMsTscSecuredSettings::StartProgram property</span></span>

<span data-ttu-id="2099d-109">Especifica el programa que se va a iniciar en el servidor remoto en el momento de la conexión.</span><span class="sxs-lookup"><span data-stu-id="2099d-109">Specifies the program to be started on the remote server upon connection.</span></span>

<span data-ttu-id="2099d-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="2099d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2099d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2099d-111">Syntax</span></span>


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a><span data-ttu-id="2099d-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="2099d-112">Property value</span></span>

<span data-ttu-id="2099d-113">Nombre del nuevo programa de inicio.</span><span class="sxs-lookup"><span data-stu-id="2099d-113">The name of the new start program.</span></span> <span data-ttu-id="2099d-114">La longitud máxima de esta cadena es **la \_ ruta de acceso Max**-1 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2099d-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2099d-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="2099d-115">Error codes</span></span>

<span data-ttu-id="2099d-116">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="2099d-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="2099d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2099d-117">Remarks</span></span>

<span data-ttu-id="2099d-118">Si no se establece el valor de esta propiedad, se ejecutará el comando de Shell del usuario de la sesión.</span><span class="sxs-lookup"><span data-stu-id="2099d-118">If the value of this property is not set, the session user's shell command will be run.</span></span> <span data-ttu-id="2099d-119">El comando de Shell se leerá desde el siguiente valor del registro en el servidor:</span><span class="sxs-lookup"><span data-stu-id="2099d-119">The shell command will be read from the following registry value on the server:</span></span>

<span data-ttu-id="2099d-120">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Shell**</span><span class="sxs-lookup"><span data-stu-id="2099d-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**WinLogon**\\**Shell**</span></span>

<span data-ttu-id="2099d-121">Para obtener más información, consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="2099d-121">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="2099d-122">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2099d-122">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2099d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2099d-123">Requirements</span></span>



| <span data-ttu-id="2099d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2099d-124">Requirement</span></span> | <span data-ttu-id="2099d-125">Value</span><span class="sxs-lookup"><span data-stu-id="2099d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2099d-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2099d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2099d-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2099d-127">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="2099d-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2099d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2099d-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2099d-129">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="2099d-130">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2099d-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="2099d-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2099d-131"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2099d-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2099d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2099d-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2099d-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="2099d-134">IID</span><span class="sxs-lookup"><span data-stu-id="2099d-134">IID</span></span><br/>                      | <span data-ttu-id="2099d-135">IID \_ IMsTscSecuredSettings se define como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="2099d-135">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2099d-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="2099d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2099d-137">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="2099d-137">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="2099d-138">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="2099d-138">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





