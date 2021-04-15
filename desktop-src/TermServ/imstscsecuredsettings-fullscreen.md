---
title: Propiedad IMsTscSecuredSettings Fullscreen
description: Especifica el estado de pantalla completa del control de cliente.
ms.assetid: f65c2fa3-b2d0-4e64-bf1e-08394c91eda8
ms.tgt_platform: multiple
keywords:
- Propiedad fullScreen Servicios de Escritorio remoto
- Propiedad fullScreen Servicios de Escritorio remoto, interfaz IMsTscSecuredSettings
- Interfaz IMsTscSecuredSettings Servicios de Escritorio remoto, propiedad fullScreen
- Propiedad fullScreen Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings
- Interfaz IMsRdpClientSecuredSettings Servicios de Escritorio remoto, propiedad fullScreen
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.Fullscreen
- IMsTscSecuredSettings.get_Fullscreen
- IMsTscSecuredSettings.put_Fullscreen
- IMsRdpClientSecuredSettings.Fullscreen
- IMsRdpClientSecuredSettings.get_Fullscreen
- IMsRdpClientSecuredSettings.put_Fullscreen
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c3b3208edf3476fcd110d7729d97d9817cb929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676927"
---
# <a name="imstscsecuredsettingsfullscreen-property"></a><span data-ttu-id="d6554-108">IMsTscSecuredSettings:: Fullscreen (propiedad)</span><span class="sxs-lookup"><span data-stu-id="d6554-108">IMsTscSecuredSettings::Fullscreen property</span></span>

<span data-ttu-id="d6554-109">Especifica el estado de pantalla completa del control de cliente.</span><span class="sxs-lookup"><span data-stu-id="d6554-109">Specifies the full-screen state of the client control.</span></span>

<span data-ttu-id="d6554-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d6554-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6554-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d6554-111">Syntax</span></span>


```C++
HRESULT put_Fullscreen(
  [in]  BOOL fFullScreen
);

HRESULT get_Fullscreen(
  [out] BOOL *pfFullScreen
);
```



## <a name="property-value"></a><span data-ttu-id="d6554-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d6554-112">Property value</span></span>

<span data-ttu-id="d6554-113">Establezca este parámetro en **true** si el control debe usar el modo de pantalla completa y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="d6554-113">Set this parameter to **TRUE** if the control should use full-screen mode and **FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d6554-114">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="d6554-114">Error codes</span></span>

<span data-ttu-id="d6554-115">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="d6554-115">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6554-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d6554-116">Remarks</span></span>

<span data-ttu-id="d6554-117">Para obtener más información acerca de este método, consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md).</span><span class="sxs-lookup"><span data-stu-id="d6554-117">For more information about this method, see [Providing for RDP Client Security](providing-for-rdp-client-security.md).</span></span>

<span data-ttu-id="d6554-118">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="d6554-118">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

<span data-ttu-id="d6554-119">Tenga en cuenta que aunque el uso de esta propiedad está restringido a las zonas de seguridad de direcciones URL permitidas de Internet Explorer, un usuario siempre puede cambiar al modo de pantalla completa después de que se haya establecido la conexión presionando la combinación de [teclas de método abreviado](terminal-services-shortcut-keys.md) del modo de pantalla completa (Ctrl + Alt + inter).</span><span class="sxs-lookup"><span data-stu-id="d6554-119">Note that although the use of this property is restricted to the allowed Internet Explorer URL security zones, a user can always change to full-screen mode after the connection has been established by pressing the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

<span data-ttu-id="d6554-120">Se puede llamar a este método mientras se establece la conexión de cliente.</span><span class="sxs-lookup"><span data-stu-id="d6554-120">This method can be called while the client connection is established.</span></span>

<span data-ttu-id="d6554-121">Debe llamar al método [**IMsRdpClientNonScriptable3::p UT \_ ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) antes de llamar al método de **\_ pantalla completa IMsTscSecuredSettings::p UT** o al método de [**\_ pantalla completa IMsRdpClient::p UT**](imsrdpclient-fullscreen.md) .</span><span class="sxs-lookup"><span data-stu-id="d6554-121">You must call the [**IMsRdpClientNonScriptable3::put\_ConnectionBarText**](imsrdpclientnonscriptable3-connectionbartext.md) method before you call the **IMsTscSecuredSettings::put\_Fullscreen** method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6554-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6554-122">Requirements</span></span>



| <span data-ttu-id="d6554-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6554-123">Requirement</span></span> | <span data-ttu-id="d6554-124">Value</span><span class="sxs-lookup"><span data-stu-id="d6554-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6554-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6554-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d6554-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d6554-126">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d6554-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6554-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d6554-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d6554-128">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d6554-129">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d6554-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="d6554-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6554-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="d6554-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d6554-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6554-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d6554-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="d6554-133">IID</span><span class="sxs-lookup"><span data-stu-id="d6554-133">IID</span></span><br/>                      | <span data-ttu-id="d6554-134">IID \_ IMsTscSecuredSettings se define como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="d6554-134">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d6554-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="d6554-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6554-136">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="d6554-136">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="d6554-137">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="d6554-137">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





