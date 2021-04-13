---
title: Propiedad KeyboardHookMode de IMsRdpClientSecuredSettings
description: Especifica la configuración de redirección de teclado, que especifica cómo y cuándo aplicar el método abreviado de teclado de Windows (por ejemplo, ALT + TAB).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad KeyboardHookMode
- Propiedad KeyboardHookMode Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings, propiedad KeyboardHookMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 948069b689d8799a98805148017a204b719d7645
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422131"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a><span data-ttu-id="67f19-106">IMsRdpClientSecuredSettings:: KeyboardHookMode (propiedad)</span><span class="sxs-lookup"><span data-stu-id="67f19-106">IMsRdpClientSecuredSettings::KeyboardHookMode property</span></span>

<span data-ttu-id="67f19-107">Especifica la configuración de redirección de teclado, que especifica cómo y cuándo aplicar el método abreviado de teclado de Windows (por ejemplo, ALT + TAB).</span><span class="sxs-lookup"><span data-stu-id="67f19-107">Specifies the keyboard redirection settings, which specify how and when to apply Windows keyboard shortcut (for example, ALT+TAB).</span></span>

<span data-ttu-id="67f19-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="67f19-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f19-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="67f19-109">Syntax</span></span>


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a><span data-ttu-id="67f19-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="67f19-110">Property value</span></span>

<span data-ttu-id="67f19-111">La nueva configuración.</span><span class="sxs-lookup"><span data-stu-id="67f19-111">The new settings.</span></span> <span data-ttu-id="67f19-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="67f19-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="67f19-113">0</span><span class="sxs-lookup"><span data-stu-id="67f19-113">0</span></span>
</dt> <dd>

<span data-ttu-id="67f19-114">Aplique las combinaciones de teclas solo localmente en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="67f19-114">Apply key combinations only locally at the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="67f19-115">1</span><span class="sxs-lookup"><span data-stu-id="67f19-115">1</span></span>
</dt> <dd>

<span data-ttu-id="67f19-116">Aplique combinaciones de teclas en el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="67f19-116">Apply key combinations at the remote server.</span></span>

</dd> <dt>

<span data-ttu-id="67f19-117">2</span><span class="sxs-lookup"><span data-stu-id="67f19-117">2</span></span>
</dt> <dd>

<span data-ttu-id="67f19-118">Aplicar combinaciones de teclas al servidor remoto solo cuando el cliente se ejecuta en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="67f19-118">Apply key combinations to the remote server only when the client is running in full-screen mode.</span></span> <span data-ttu-id="67f19-119">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="67f19-119">This is the default value.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="67f19-120">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="67f19-120">Error codes</span></span>

<span data-ttu-id="67f19-121">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="67f19-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="67f19-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="67f19-122">Remarks</span></span>

<span data-ttu-id="67f19-123">Estas propiedades no se pueden establecer cuando el control está conectado.</span><span class="sxs-lookup"><span data-stu-id="67f19-123">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="67f19-124">Para obtener más información, consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="67f19-124">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="67f19-125">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="67f19-125">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="67f19-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67f19-126">Requirements</span></span>



| <span data-ttu-id="67f19-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="67f19-127">Requirement</span></span> | <span data-ttu-id="67f19-128">Value</span><span class="sxs-lookup"><span data-stu-id="67f19-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67f19-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67f19-129">Minimum supported client</span></span><br/> | <span data-ttu-id="67f19-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67f19-130">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="67f19-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="67f19-131">Minimum supported server</span></span><br/> | <span data-ttu-id="67f19-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67f19-132">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="67f19-133">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="67f19-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="67f19-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67f19-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="67f19-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="67f19-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67f19-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67f19-136"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="67f19-137">IID</span><span class="sxs-lookup"><span data-stu-id="67f19-137">IID</span></span><br/>                      | <span data-ttu-id="67f19-138">IID \_ IMsRdpClientSecuredSettings se define como 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="67f19-138">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67f19-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="67f19-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67f19-140">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="67f19-140">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





