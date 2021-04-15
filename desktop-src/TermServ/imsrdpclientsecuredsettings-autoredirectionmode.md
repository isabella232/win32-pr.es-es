---
title: Propiedad AudioRedirectionMode de IMsRdpClientSecuredSettings
description: Especifica la configuración de redirección de audio, que especifica si se deben redirigir sonidos o reproducir sonidos en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 6aa63a50-a714-4a9b-a4ec-c0551920467a
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad AudioRedirectionMode
- Propiedad AudioRedirectionMode Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings, propiedad AudioRedirectionMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.AudioRedirectionMode
- IMsRdpClientSecuredSettings.get_AudioRedirectionMode
- IMsRdpClientSecuredSettings.put_AudioRedirectionMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 858342811ec97def95031ebed0605b5a81cf80fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535571"
---
# <a name="imsrdpclientsecuredsettingsaudioredirectionmode-property"></a><span data-ttu-id="1ec7d-106">IMsRdpClientSecuredSettings:: AudioRedirectionMode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1ec7d-106">IMsRdpClientSecuredSettings::AudioRedirectionMode property</span></span>

<span data-ttu-id="1ec7d-107">Especifica la configuración de redirección de audio, que especifica si se deben redirigir sonidos o reproducir sonidos en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="1ec7d-107">Specifies the audio redirection settings, which specify whether to redirect sounds or play sounds at the Remote Desktop Session Host (RD Session Host) server.</span></span>

<span data-ttu-id="1ec7d-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1ec7d-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ec7d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ec7d-109">Syntax</span></span>


```C++
HRESULT put_AudioRedirectionMode(
  [in]  LONG audioRedirectionMode
);

HRESULT get_AudioRedirectionMode(
  [out] LONG *paudioRedirectionMode
);
```



## <a name="property-value"></a><span data-ttu-id="1ec7d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1ec7d-110">Property value</span></span>

<span data-ttu-id="1ec7d-111">La nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="1ec7d-111">The new settings.</span></span> <span data-ttu-id="1ec7d-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1ec7d-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="1ec7d-113">0</span><span class="sxs-lookup"><span data-stu-id="1ec7d-113">0</span></span>
</dt> <dd>

<span data-ttu-id="1ec7d-114">Redirigir sonidos al cliente.</span><span class="sxs-lookup"><span data-stu-id="1ec7d-114">Redirect sounds to the client.</span></span> <span data-ttu-id="1ec7d-115">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="1ec7d-115">This is the default value.</span></span>

</dd> <dt>

<span data-ttu-id="1ec7d-116">1</span><span class="sxs-lookup"><span data-stu-id="1ec7d-116">1</span></span>
</dt> <dd>

<span data-ttu-id="1ec7d-117">Reproducir sonidos en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="1ec7d-117">Play sounds at the remote computer.</span></span>

</dd> <dt>

<span data-ttu-id="1ec7d-118">2</span><span class="sxs-lookup"><span data-stu-id="1ec7d-118">2</span></span>
</dt> <dd>

<span data-ttu-id="1ec7d-119">Deshabilitar el redireccionamiento de sonido; no reproducir sonidos en el servidor.</span><span class="sxs-lookup"><span data-stu-id="1ec7d-119">Disable sound redirection; do not play sounds at the server.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="1ec7d-120">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="1ec7d-120">Error codes</span></span>

<span data-ttu-id="1ec7d-121">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="1ec7d-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ec7d-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ec7d-122">Remarks</span></span>

<span data-ttu-id="1ec7d-123">Estas propiedades no se pueden establecer cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="1ec7d-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="1ec7d-124">Para obtener más información, consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="1ec7d-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="1ec7d-125">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="1ec7d-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ec7d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ec7d-126">Requirements</span></span>



| <span data-ttu-id="1ec7d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ec7d-127">Requirement</span></span> | <span data-ttu-id="1ec7d-128">Value</span><span class="sxs-lookup"><span data-stu-id="1ec7d-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ec7d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ec7d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="1ec7d-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1ec7d-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="1ec7d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ec7d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="1ec7d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ec7d-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="1ec7d-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1ec7d-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="1ec7d-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ec7d-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="1ec7d-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1ec7d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ec7d-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ec7d-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="1ec7d-137">IID</span><span class="sxs-lookup"><span data-stu-id="1ec7d-137">IID</span></span><br/>                      | <span data-ttu-id="1ec7d-138">IID \_ IMsRdpClientSecuredSettings se define como 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="1ec7d-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ec7d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ec7d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ec7d-140">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="1ec7d-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





