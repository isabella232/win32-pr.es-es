---
title: Mensaje de HKM_SETRULES (commctrl. h)
description: Define las combinaciones no válidas y la combinación de modificadores predeterminados para un control de tecla de acceso rápido.
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES controles de mensajes de Windows
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491188"
---
# <a name="hkm_setrules-message"></a><span data-ttu-id="3a15d-104">HKM \_ SETRULES</span><span class="sxs-lookup"><span data-stu-id="3a15d-104">HKM\_SETRULES message</span></span>

<span data-ttu-id="3a15d-105">Define las combinaciones no válidas y la combinación de modificadores predeterminados para un control de tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="3a15d-105">Defines the invalid combinations and the default modifier combination for a hot key control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a15d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a15d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a15d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a15d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a15d-108">Matriz de marcas que especifican combinaciones de teclas no válidas.</span><span class="sxs-lookup"><span data-stu-id="3a15d-108">An array of flags that specify invalid key combinations.</span></span> <span data-ttu-id="3a15d-109">Este parámetro puede ser una combinación de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="3a15d-109">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="3a15d-110">Value</span><span class="sxs-lookup"><span data-stu-id="3a15d-110">Value</span></span>                                                                                                                                                   | <span data-ttu-id="3a15d-111">Significado</span><span class="sxs-lookup"><span data-stu-id="3a15d-111">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <span data-ttu-id="3a15d-112"><dt>**HKCOMB \_ A**</dt></span><span class="sxs-lookup"><span data-stu-id="3a15d-112"><dt>**HKCOMB\_A**</dt></span></span> </dl>          | <span data-ttu-id="3a15d-113">ALT</span><span class="sxs-lookup"><span data-stu-id="3a15d-113">ALT</span></span><br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <span data-ttu-id="3a15d-114"><dt>**HKCOMB \_ C**</dt></span><span class="sxs-lookup"><span data-stu-id="3a15d-114"><dt>**HKCOMB\_C**</dt></span></span> </dl>          | <span data-ttu-id="3a15d-115">CTRL</span><span class="sxs-lookup"><span data-stu-id="3a15d-115">CTRL</span></span><br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <span data-ttu-id="3a15d-116"><dt>**HKCOMB \_ CA**</dt></span><span class="sxs-lookup"><span data-stu-id="3a15d-116"><dt>**HKCOMB\_CA**</dt></span></span> </dl>       | <span data-ttu-id="3a15d-117">CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="3a15d-117">CTRL+ALT</span></span><br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <span data-ttu-id="3a15d-118"><dt>**HKCOMB \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="3a15d-118"><dt>**HKCOMB\_NONE**</dt></span></span> </dl> | <span data-ttu-id="3a15d-119">Claves sin modificar</span><span class="sxs-lookup"><span data-stu-id="3a15d-119">Unmodified keys</span></span><br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <span data-ttu-id="3a15d-120"><dt>**HKCOMB \_ S**</dt></span><span class="sxs-lookup"><span data-stu-id="3a15d-120"><dt>**HKCOMB\_S**</dt></span></span> </dl>          | <span data-ttu-id="3a15d-121">Mayús</span><span class="sxs-lookup"><span data-stu-id="3a15d-121">SHIFT</span></span><br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <span data-ttu-id="3a15d-122"><dt>**SA de HKCOMB \_**</dt></span><span class="sxs-lookup"><span data-stu-id="3a15d-122"><dt>**HKCOMB\_SA**</dt></span></span> </dl>       | <span data-ttu-id="3a15d-123">MAYÚS+ALT</span><span class="sxs-lookup"><span data-stu-id="3a15d-123">SHIFT+ALT</span></span><br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <span data-ttu-id="3a15d-124"><dt>**HKCOMB \_ SC**</dt></span><span class="sxs-lookup"><span data-stu-id="3a15d-124"><dt>**HKCOMB\_SC**</dt></span></span> </dl>       | <span data-ttu-id="3a15d-125">MAYÚS + CTRL</span><span class="sxs-lookup"><span data-stu-id="3a15d-125">SHIFT+CTRL</span></span><br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <span data-ttu-id="3a15d-126"><dt>**HKCOMB \_ SCA**</dt></span><span class="sxs-lookup"><span data-stu-id="3a15d-126"><dt>**HKCOMB\_SCA**</dt></span></span> </dl>    | <span data-ttu-id="3a15d-127">MAYÚS + CTRL + ALT</span><span class="sxs-lookup"><span data-stu-id="3a15d-127">SHIFT+CTRL+ALT</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="3a15d-128">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a15d-128">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3a15d-129">Matriz de marcas que especifican la combinación de teclas que se va a usar cuando el usuario especifica una combinación no válida.</span><span class="sxs-lookup"><span data-stu-id="3a15d-129">An array of flags that specify the key combination to use when the user enters an invalid combination.</span></span> <span data-ttu-id="3a15d-130">Para obtener una lista de valores de marcador de modificador, vea la descripción del mensaje [**\_ GETHOTKEY de HKM**](hkm-gethotkey.md) .</span><span class="sxs-lookup"><span data-stu-id="3a15d-130">For a list of modifier flag values, see the description of the [**HKM\_GETHOTKEY**](hkm-gethotkey.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a15d-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a15d-131">Return value</span></span>

<span data-ttu-id="3a15d-132">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3a15d-132">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a15d-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a15d-133">Remarks</span></span>

<span data-ttu-id="3a15d-134">Cuando un usuario especifica una combinación de teclas no válida, tal y como se define en las marcas especificadas en *wParam*, el sistema utiliza el operador OR bit a bit para combinar las claves especificadas por el usuario con las marcas especificadas en *lParam*.</span><span class="sxs-lookup"><span data-stu-id="3a15d-134">When a user enters an invalid key combination, as defined by flags specified in *wParam*, the system uses the bitwise-OR operator to combine the keys entered by the user with the flags specified in *lParam*.</span></span> <span data-ttu-id="3a15d-135">La combinación de teclas resultante se convierte en una cadena y, a continuación, se muestra en el control de tecla de acceso rápido.</span><span class="sxs-lookup"><span data-stu-id="3a15d-135">The resulting key combination is converted into a string and then displayed in the hot key control.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a15d-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a15d-136">Requirements</span></span>



| <span data-ttu-id="3a15d-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a15d-137">Requirement</span></span> | <span data-ttu-id="3a15d-138">Value</span><span class="sxs-lookup"><span data-stu-id="3a15d-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a15d-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a15d-139">Minimum supported client</span></span><br/> | <span data-ttu-id="3a15d-140">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3a15d-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a15d-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a15d-141">Minimum supported server</span></span><br/> | <span data-ttu-id="3a15d-142">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a15d-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a15d-143">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a15d-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a15d-144"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a15d-144"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





