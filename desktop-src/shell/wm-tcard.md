---
description: Se envía a una aplicación que ha iniciado una tarjeta de aprendizaje con la ayuda de Windows.
title: Mensaje de WM_TCARD (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276734"
---
# <a name="wm_tcard-message"></a><span data-ttu-id="af6de-103">Mensaje de TCARD de WM \_</span><span class="sxs-lookup"><span data-stu-id="af6de-103">WM\_TCARD message</span></span>

<span data-ttu-id="af6de-104">Se envía a una aplicación que ha iniciado una tarjeta de aprendizaje con la ayuda de Windows.</span><span class="sxs-lookup"><span data-stu-id="af6de-104">Sent to an application that has initiated a training card with Windows Help.</span></span> <span data-ttu-id="af6de-105">El mensaje informa a la aplicación cuando el usuario hace clic en un botón que se pudo crear.</span><span class="sxs-lookup"><span data-stu-id="af6de-105">The message informs the application when the user clicks an authorable button.</span></span> <span data-ttu-id="af6de-106">Una aplicación inicia una tarjeta de entrenamiento especificando el comando HELP \_ TCARD en una llamada a la función [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .</span><span class="sxs-lookup"><span data-stu-id="af6de-106">An application initiates a training card by specifying the HELP\_TCARD command in a call to the [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) function.</span></span>

## <a name="parameters"></a><span data-ttu-id="af6de-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="af6de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af6de-108">*idAction*</span><span class="sxs-lookup"><span data-stu-id="af6de-108">*idAction*</span></span> 
</dt> <dd>

<span data-ttu-id="af6de-109">Valor que indica la acción que ha realizado el usuario.</span><span class="sxs-lookup"><span data-stu-id="af6de-109">A value that indicates the action the user has taken.</span></span> <span data-ttu-id="af6de-110">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="af6de-110">This can be one of the following values.</span></span>

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span data-ttu-id="af6de-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span><span class="sxs-lookup"><span data-stu-id="af6de-111"><span id="IDABORT"></span><span id="idabort"></span>**IDABORT**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-112">El usuario hizo clic en un botón de **anulación** que se pudo crear.</span><span class="sxs-lookup"><span data-stu-id="af6de-112">The user clicked an authorable **Abort** button.</span></span>

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span data-ttu-id="af6de-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span><span class="sxs-lookup"><span data-stu-id="af6de-113"><span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-114">El usuario hizo clic en un botón **Cancelar** que se pudo crear.</span><span class="sxs-lookup"><span data-stu-id="af6de-114">The user clicked an authorable **Cancel** button.</span></span>

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span data-ttu-id="af6de-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span><span class="sxs-lookup"><span data-stu-id="af6de-115"><span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-116">El usuario cerró la tarjeta de entrenamiento.</span><span class="sxs-lookup"><span data-stu-id="af6de-116">The user closed the training card.</span></span>

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span data-ttu-id="af6de-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span><span class="sxs-lookup"><span data-stu-id="af6de-117"><span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-118">El usuario hizo clic en un botón **ayuda** de Windows autorizado.</span><span class="sxs-lookup"><span data-stu-id="af6de-118">The user clicked an authorable Windows **Help** button.</span></span>

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span data-ttu-id="af6de-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span><span class="sxs-lookup"><span data-stu-id="af6de-119"><span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-120">El usuario hizo clic en un botón para **omitir** la creación.</span><span class="sxs-lookup"><span data-stu-id="af6de-120">The user clicked an authorable **Ignore** button.</span></span>

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span data-ttu-id="af6de-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span><span class="sxs-lookup"><span data-stu-id="af6de-121"><span id="IDOK"></span><span id="idok"></span>**IDOK**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-122">El usuario hizo clic en un botón **Aceptar** que se pudo crear.</span><span class="sxs-lookup"><span data-stu-id="af6de-122">The user clicked an authorable **OK** button.</span></span>

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span data-ttu-id="af6de-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span><span class="sxs-lookup"><span data-stu-id="af6de-123"><span id="IDNO"></span><span id="idno"></span>**IDNO**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-124">El usuario hizo clic en un botón **no** autorizado.</span><span class="sxs-lookup"><span data-stu-id="af6de-124">The user clicked an authorable **No** button.</span></span>

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span data-ttu-id="af6de-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span><span class="sxs-lookup"><span data-stu-id="af6de-125"><span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-126">El usuario hizo clic en un botón de **reintento** que se pudo crear.</span><span class="sxs-lookup"><span data-stu-id="af6de-126">The user clicked an authorable **Retry** button.</span></span>

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span data-ttu-id="af6de-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**\_datos de TCARD de ayuda \_**</span><span class="sxs-lookup"><span data-stu-id="af6de-127"><span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**HELP\_TCARD\_DATA**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-128">El usuario hizo clic en un botón que se pudo crear.</span><span class="sxs-lookup"><span data-stu-id="af6de-128">The user clicked an authorable button.</span></span> <span data-ttu-id="af6de-129">El parámetro *dwActionData* contiene un entero largo especificado por el autor de la ayuda.</span><span class="sxs-lookup"><span data-stu-id="af6de-129">The *dwActionData* parameter contains a long integer specified by the Help author.</span></span>

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span data-ttu-id="af6de-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**AYUDA \_ TCARD \_ otro \_ llamador**</span><span class="sxs-lookup"><span data-stu-id="af6de-130"><span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**HELP\_TCARD\_OTHER\_CALLER**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-131">Otra aplicación ha solicitado tarjetas de entrenamiento.</span><span class="sxs-lookup"><span data-stu-id="af6de-131">Another application has requested training cards.</span></span>

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span data-ttu-id="af6de-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span><span class="sxs-lookup"><span data-stu-id="af6de-132"><span id="IDYES"></span><span id="idyes"></span>**IDYES**</span></span>


</dt> <dd>

<span data-ttu-id="af6de-133">El usuario hizo clic en un botón **sí** que se pudo crear.</span><span class="sxs-lookup"><span data-stu-id="af6de-133">The user clicked an authorable **Yes** button.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="af6de-134">*dwActionData*</span><span class="sxs-lookup"><span data-stu-id="af6de-134">*dwActionData*</span></span> 
</dt> <dd>

<span data-ttu-id="af6de-135">Si *idAction* especifica \_ \_ los datos de TCARD de ayuda, este parámetro es un **valor largo** especificado por el autor de la ayuda.</span><span class="sxs-lookup"><span data-stu-id="af6de-135">If *idAction* specifies HELP\_TCARD\_DATA, this parameter is a **long** specified by the Help author.</span></span> <span data-ttu-id="af6de-136">De lo contrario, este parámetro es cero.</span><span class="sxs-lookup"><span data-stu-id="af6de-136">Otherwise, this parameter is zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af6de-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af6de-137">Return value</span></span>

<span data-ttu-id="af6de-138">Se omite el valor devuelto; Use cero.</span><span class="sxs-lookup"><span data-stu-id="af6de-138">The return value is ignored; use zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="af6de-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af6de-139">Requirements</span></span>



| <span data-ttu-id="af6de-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="af6de-140">Requirement</span></span> | <span data-ttu-id="af6de-141">Value</span><span class="sxs-lookup"><span data-stu-id="af6de-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="af6de-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af6de-142">Minimum supported client</span></span><br/> | <span data-ttu-id="af6de-143">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="af6de-143">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="af6de-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="af6de-144">Minimum supported server</span></span><br/> | <span data-ttu-id="af6de-145">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="af6de-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="af6de-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="af6de-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="af6de-147"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="af6de-147"><dt>Winuser.h</dt></span></span> </dl> |



 

 




