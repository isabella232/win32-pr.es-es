---
title: Propiedad WorkDir de IMsTscSecuredSettings
description: Especifica el directorio de trabajo del programa de inicio.
ms.assetid: e67f7274-be47-42c4-9267-a05bb93e6725
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad WorkDir
- Propiedad WorkDir Servicios de Escritorio remoto, interfaz IMsTscSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsTscSecuredSettings, propiedad WorkDir
- Propiedad WorkDir Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings, propiedad WorkDir
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.WorkDir
- IMsTscSecuredSettings.get_WorkDir
- IMsTscSecuredSettings.put_WorkDir
- IMsRdpClientSecuredSettings.WorkDir
- IMsRdpClientSecuredSettings.get_WorkDir
- IMsRdpClientSecuredSettings.put_WorkDir
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a0a80b35ba682012150b4277d800bc4a3582e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676975"
---
# <a name="imstscsecuredsettingsworkdir-property"></a><span data-ttu-id="86c5d-108">IMsTscSecuredSettings:: WorkDir (propiedad)</span><span class="sxs-lookup"><span data-stu-id="86c5d-108">IMsTscSecuredSettings::WorkDir property</span></span>

<span data-ttu-id="86c5d-109">Especifica el directorio de trabajo del programa de inicio.</span><span class="sxs-lookup"><span data-stu-id="86c5d-109">Specifies the working directory of the start program.</span></span>

<span data-ttu-id="86c5d-110">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="86c5d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="86c5d-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="86c5d-111">Syntax</span></span>


```C++
HRESULT put_WorkDir(
  [in]  BSTR newVal
);

HRESULT get_WorkDir(
  [out] BSTR *pWorkDir
);
```



## <a name="property-value"></a><span data-ttu-id="86c5d-112">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="86c5d-112">Property value</span></span>

<span data-ttu-id="86c5d-113">Nuevo directorio de trabajo.</span><span class="sxs-lookup"><span data-stu-id="86c5d-113">The new working directory.</span></span> <span data-ttu-id="86c5d-114">La longitud máxima de esta cadena es **la \_ ruta de acceso Max**-1 caracteres.</span><span class="sxs-lookup"><span data-stu-id="86c5d-114">The maximum length of this string is **MAX\_PATH**-1 characters.</span></span>

## <a name="error-codes"></a><span data-ttu-id="86c5d-115">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="86c5d-115">Error codes</span></span>

<span data-ttu-id="86c5d-116">Devuelve **S \_ correcto** si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="86c5d-116">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="86c5d-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86c5d-117">Remarks</span></span>

<span data-ttu-id="86c5d-118">Para obtener más información, consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="86c5d-118">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information.</span></span>

<span data-ttu-id="86c5d-119">Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="86c5d-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86c5d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86c5d-120">Requirements</span></span>



| <span data-ttu-id="86c5d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="86c5d-121">Requirement</span></span> | <span data-ttu-id="86c5d-122">Value</span><span class="sxs-lookup"><span data-stu-id="86c5d-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="86c5d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86c5d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="86c5d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="86c5d-124">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="86c5d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86c5d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="86c5d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="86c5d-126">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="86c5d-127">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="86c5d-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="86c5d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c5d-128"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="86c5d-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="86c5d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86c5d-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86c5d-130"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="86c5d-131">IID</span><span class="sxs-lookup"><span data-stu-id="86c5d-131">IID</span></span><br/>                      | <span data-ttu-id="86c5d-132">IID \_ IMsTscSecuredSettings se define como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span><span class="sxs-lookup"><span data-stu-id="86c5d-132">IID\_IMsTscSecuredSettings is defined as c9d65442-a0f9-45b2-8f73-d61d2db8cbb6</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="86c5d-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="86c5d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86c5d-134">**IMsRdpClientSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="86c5d-134">**IMsRdpClientSecuredSettings**</span></span>](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="86c5d-135">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="86c5d-135">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





