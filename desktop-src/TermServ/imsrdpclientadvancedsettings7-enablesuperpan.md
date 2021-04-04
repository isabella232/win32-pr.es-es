---
title: Propiedad EnableSuperPan de IMsRdpClientAdvancedSettings7
description: Especifica o recupera un valor booleano que indica si SuperPan está habilitado o deshabilitado.
ms.assetid: 0d0ef89e-75f5-460a-ad55-01f8d9478df5
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad EnableSuperPan
- Propiedad EnableSuperPan Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad EnableSuperPan
- Propiedad EnableSuperPan Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad EnableSuperPan
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7.EnableSuperPan
- IMsRdpClientAdvancedSettings7.get_EnableSuperPan
- IMsRdpClientAdvancedSettings7.put_EnableSuperPan
- IMsRdpClientAdvancedSettings8.EnableSuperPan
- IMsRdpClientAdvancedSettings8.get_EnableSuperPan
- IMsRdpClientAdvancedSettings8.put_EnableSuperPan
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ac0664b99dc0533d3e26840445ef22c8c08385
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802750"
---
# <a name="imsrdpclientadvancedsettings7enablesuperpan-property"></a><span data-ttu-id="b77c8-108">IMsRdpClientAdvancedSettings7:: EnableSuperPan (propiedad)</span><span class="sxs-lookup"><span data-stu-id="b77c8-108">IMsRdpClientAdvancedSettings7::EnableSuperPan property</span></span>

<span data-ttu-id="b77c8-109">Especifica o recupera un valor booleano que indica si SuperPan está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="b77c8-109">Specifies or retrieves a Boolean value that indicates whether SuperPan is enabled or disabled.</span></span> <span data-ttu-id="b77c8-110">SuperPan es una característica que permite a los usuarios navegar con facilidad por un escritorio remoto en modo de pantalla completa, cuando las dimensiones del escritorio remoto son mayores que las dimensiones de la ventana del cliente actual.</span><span class="sxs-lookup"><span data-stu-id="b77c8-110">SuperPan is a feature that allows a user to easily navigate a remote desktop in full-screen mode, when the dimensions of the remote desktop are larger than the dimensions of the current client window.</span></span> <span data-ttu-id="b77c8-111">En lugar de usar barras de desplazamiento para navegar por el escritorio, el usuario puede apuntar al borde de la ventana y el escritorio remoto se desplazará automáticamente en esa dirección.</span><span class="sxs-lookup"><span data-stu-id="b77c8-111">Instead of using scroll bars to navigate the desktop, the user can point to the window border, and the remote desktop will scroll automatically in that direction.</span></span> <span data-ttu-id="b77c8-112">SuperPan no admite más de un monitor.</span><span class="sxs-lookup"><span data-stu-id="b77c8-112">SuperPan does not support more than one monitor.</span></span>

<span data-ttu-id="b77c8-113">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b77c8-113">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b77c8-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b77c8-114">Syntax</span></span>


```C++
HRESULT put_EnableSuperPan(
  [in]          VARIANT_BOOL fEnableSuperPan
);

HRESULT get_EnableSuperPan(
  [out, retval] VARIANT_BOOL *pfEnableSuperPan
);
```



## <a name="property-value"></a><span data-ttu-id="b77c8-115">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b77c8-115">Property value</span></span>

<span data-ttu-id="b77c8-116">Un **valor \_ booleano Variant** que especifica si SuperPan está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b77c8-116">A **VARIANT\_BOOL** value that specifies whether SuperPan is enabled.</span></span> <span data-ttu-id="b77c8-117">Un valor de **Variant \_ true** especifica que SuperPan está habilitado.</span><span class="sxs-lookup"><span data-stu-id="b77c8-117">A value of **VARIANT\_TRUE** specifies that SuperPan is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="b77c8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b77c8-118">Requirements</span></span>



| <span data-ttu-id="b77c8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="b77c8-119">Requirement</span></span> | <span data-ttu-id="b77c8-120">Value</span><span class="sxs-lookup"><span data-stu-id="b77c8-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b77c8-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b77c8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b77c8-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b77c8-122">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="b77c8-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b77c8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b77c8-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b77c8-124">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="b77c8-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b77c8-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="b77c8-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b77c8-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b77c8-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b77c8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b77c8-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b77c8-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b77c8-129">IID</span><span class="sxs-lookup"><span data-stu-id="b77c8-129">IID</span></span><br/>                      | <span data-ttu-id="b77c8-130">IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="b77c8-130">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b77c8-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="b77c8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b77c8-132">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="b77c8-132">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="b77c8-133">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="b77c8-133">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> </dl>

 

 





