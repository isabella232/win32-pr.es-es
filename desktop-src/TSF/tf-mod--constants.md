---
title: Constantes de TF_MOD_ (msctf. h)
description: Las \_ constantes TF mod \_ \ especifican modificadores de clave en la \_ estructura TF PRESERVEDKEY.
ms.assetid: 4642ef17-34bd-4482-a9e9-0fbed7b574b1
topic_type:
- apiref
api_name:
- TF_MOD_ALT
- TF_MOD_CONTROL
- TF_MOD_SHIFT
- TF_MOD_RALT
- TF_MOD_RCONTROL
- TF_MOD_RSHIFT
- TF_MOD_LALT
- TF_MOD_LCONTROL
- TF_MOD_LSHIFT
- TF_MOD_ON_KEYUP
- TF_MOD_IGNORE_ALL_MODIFIER
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e67e081d9a0f8714410861c7c36f9f751bad8d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079333"
---
# <a name="tf_mod_-constants"></a><span data-ttu-id="32065-103">TF \_ mod ( \_ \* constantes)</span><span class="sxs-lookup"><span data-stu-id="32065-103">TF\_MOD\_\* Constants</span></span>

<span data-ttu-id="32065-104">Las \_ constantes TF mod \_ \* especifican modificadores de clave en la estructura [TF \_ PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) .</span><span class="sxs-lookup"><span data-stu-id="32065-104">The TF\_MOD\_\* constants specify key modifiers in the [TF\_PRESERVEDKEY](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey) structure.</span></span>



| <span data-ttu-id="32065-105">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="32065-105">Constant/value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="32065-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="32065-106">Description</span></span>                                                                                                                                                                          |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_MOD_ALT"></span><span id="tf_mod_alt"></span><dl> <span data-ttu-id="32065-107"><dt>**TF \_ MOD \_ Alt**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="32065-107"><dt>**TF\_MOD\_ALT**</dt> <dt>0x0001</dt></span></span> </dl>                                                   | <span data-ttu-id="32065-108">Se presionó cualquiera de las teclas ALT</span><span class="sxs-lookup"><span data-stu-id="32065-108">Either of the ALT keys is pressed</span></span><br/>                                                                                                                                         |
| <span id="TF_MOD_CONTROL"></span><span id="tf_mod_control"></span><dl> <span data-ttu-id="32065-109"><dt>**TF \_ \_Control mod**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="32065-109"><dt>**TF\_MOD\_CONTROL**</dt> <dt>0x0002</dt></span></span> </dl>                                       | <span data-ttu-id="32065-110">Se presionó cualquiera de las teclas CTRL</span><span class="sxs-lookup"><span data-stu-id="32065-110">Either of the CTRL keys is pressed</span></span><br/>                                                                                                                                        |
| <span id="TF_MOD_SHIFT"></span><span id="tf_mod_shift"></span><dl> <span data-ttu-id="32065-111"><dt>**TF \_ MOD \_ Shift**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="32065-111"><dt>**TF\_MOD\_SHIFT**</dt> <dt>0x0004</dt></span></span> </dl>                                             | <span data-ttu-id="32065-112">Se presionó cualquiera de las teclas Mayús</span><span class="sxs-lookup"><span data-stu-id="32065-112">Either of the SHIFT keys is pressed</span></span><br/>                                                                                                                                       |
| <span id="TF_MOD_RALT"></span><span id="tf_mod_ralt"></span><dl> <span data-ttu-id="32065-113"><dt>**TF \_ MOD \_ Ralt**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="32065-113"><dt>**TF\_MOD\_RALT**</dt> <dt>0x0008</dt></span></span> </dl>                                                | <span data-ttu-id="32065-114">Se presiona la tecla ALT derecha</span><span class="sxs-lookup"><span data-stu-id="32065-114">The right ALT key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_RCONTROL"></span><span id="tf_mod_rcontrol"></span><dl> <span data-ttu-id="32065-115"><dt>**TF \_ MOD \_ RCONTROL**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="32065-115"><dt>**TF\_MOD\_RCONTROL**</dt> <dt>0x0010</dt></span></span> </dl>                                    | <span data-ttu-id="32065-116">Se presiona la tecla CTRL derecha</span><span class="sxs-lookup"><span data-stu-id="32065-116">The right CTRL key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_RSHIFT"></span><span id="tf_mod_rshift"></span><dl> <span data-ttu-id="32065-117"><dt>**TF \_ MOD \_ RSHIFT**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="32065-117"><dt>**TF\_MOD\_RSHIFT**</dt> <dt>0x0020</dt></span></span> </dl>                                          | <span data-ttu-id="32065-118">Se presiona la tecla Mayús derecha</span><span class="sxs-lookup"><span data-stu-id="32065-118">The right SHIFT key is pressed</span></span><br/>                                                                                                                                            |
| <span id="TF_MOD_LALT"></span><span id="tf_mod_lalt"></span><dl> <span data-ttu-id="32065-119"><dt>**TF \_ MOD \_ LALT**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="32065-119"><dt>**TF\_MOD\_LALT**</dt> <dt>0x0040</dt></span></span> </dl>                                                | <span data-ttu-id="32065-120">Se presiona la tecla ALT izquierda</span><span class="sxs-lookup"><span data-stu-id="32065-120">The left ALT key is pressed</span></span><br/>                                                                                                                                               |
| <span id="TF_MOD_LCONTROL"></span><span id="tf_mod_lcontrol"></span><dl> <span data-ttu-id="32065-121"><dt>**TF \_ MOD \_ LCONTROL**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="32065-121"><dt>**TF\_MOD\_LCONTROL**</dt> <dt>0x0080</dt></span></span> </dl>                                    | <span data-ttu-id="32065-122">Se presiona la tecla CTRL izquierda</span><span class="sxs-lookup"><span data-stu-id="32065-122">The left CTRL key is pressed</span></span><br/>                                                                                                                                              |
| <span id="TF_MOD_LSHIFT"></span><span id="tf_mod_lshift"></span><dl> <span data-ttu-id="32065-123"><dt>**TF \_ MOD \_ LSHIFT**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="32065-123"><dt>**TF\_MOD\_LSHIFT**</dt> <dt>0x0100</dt></span></span> </dl>                                          | <span data-ttu-id="32065-124">Se presiona la tecla Mayús izquierda</span><span class="sxs-lookup"><span data-stu-id="32065-124">The left SHIFT key is pressed</span></span><br/>                                                                                                                                             |
| <span id="TF_MOD_ON_KEYUP"></span><span id="tf_mod_on_keyup"></span><dl> <span data-ttu-id="32065-125"><dt>**TF \_ MOD \_ en \_ KEYUP**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="32065-125"><dt>**TF\_MOD\_ON\_KEYUP**</dt> <dt>0x0200</dt></span></span> </dl>                                   | <span data-ttu-id="32065-126">El evento se desencadenará cuando se libere la tecla.</span><span class="sxs-lookup"><span data-stu-id="32065-126">The event will be fired when the key is released.</span></span> <span data-ttu-id="32065-127">Sin esta marca, el evento se desencadena cuando se presiona la tecla.</span><span class="sxs-lookup"><span data-stu-id="32065-127">Without this flag, the event is fired when the key is pressed.</span></span><br/>                                                          |
| <span id="TF_MOD_IGNORE_ALL_MODIFIER"></span><span id="tf_mod_ignore_all_modifier"></span><dl> <span data-ttu-id="32065-128"><dt>**TF \_ MOD \_ omitir \_ todos los \_ Modificadores**</dt> <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="32065-128"><dt>**TF\_MOD\_IGNORE\_ALL\_MODIFIER**</dt> <dt>0x0400</dt></span></span> </dl> | <span data-ttu-id="32065-129">Se omite el estado de las teclas ALT, CTRL y Mayús.</span><span class="sxs-lookup"><span data-stu-id="32065-129">The state of the ALT, CTRL, and SHIFT keys is ignored.</span></span> <span data-ttu-id="32065-130">Esto significa que el evento se desencadenará cuando se presione la tecla virtual, independientemente de las teclas modificadoras que se presionen.</span><span class="sxs-lookup"><span data-stu-id="32065-130">This means the event will be fired when the virtual key is pressed, regardless of which modifier keys are pressed.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="32065-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32065-131">Requirements</span></span>



| <span data-ttu-id="32065-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="32065-132">Requirement</span></span> | <span data-ttu-id="32065-133">Value</span><span class="sxs-lookup"><span data-stu-id="32065-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="32065-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32065-134">Minimum supported client</span></span><br/> | <span data-ttu-id="32065-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="32065-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="32065-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32065-136">Minimum supported server</span></span><br/> | <span data-ttu-id="32065-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="32065-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="32065-138">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="32065-138">Redistributable</span></span><br/>          | <span data-ttu-id="32065-139">TSF 1,0 en Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="32065-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="32065-140">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32065-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="32065-141"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="32065-141"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="32065-142">IDL</span><span class="sxs-lookup"><span data-stu-id="32065-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32065-143"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32065-143"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32065-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="32065-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32065-145">TF \_ PRESERVEDKEY</span><span class="sxs-lookup"><span data-stu-id="32065-145">TF\_PRESERVEDKEY</span></span>](/windows/desktop/api/Msctf/ns-msctf-tf_preservedkey)
</dt> </dl>

 

 





