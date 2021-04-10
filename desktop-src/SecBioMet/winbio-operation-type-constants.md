---
title: Constantes de WINBIO_OPERATION_TYPE (Winbio \_ Types. h)
description: Especifique el tipo de operación asincrónica que se va a realizar.
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151224"
---
# <a name="winbio_operation_type-constants"></a><span data-ttu-id="1184c-103">Constantes de tipo de \_ operación WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="1184c-103">WINBIO\_OPERATION\_TYPE Constants</span></span>

<span data-ttu-id="1184c-104">Las siguientes constantes pueden ser devueltas por el Plataforma de biometría de Windows en [**un \_ \_ resultado asincrónico de WINBIO**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) para especificar el tipo de operación asincrónica que se va a realizar.</span><span class="sxs-lookup"><span data-stu-id="1184c-104">The following constants can be returned by the Windows Biometric Framework in a [**WINBIO\_ASYNC\_RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) to specify the type of asynchronous operation being performed.</span></span>

<dl> <dt>

<span data-ttu-id="1184c-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**operación de WINBIO \_ \_ ninguna**</span><span class="sxs-lookup"><span data-stu-id="1184c-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**WINBIO\_OPERATION\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-106">0</span><span class="sxs-lookup"><span data-stu-id="1184c-106">0</span></span>
</dt> <dt>



<span data-ttu-id="1184c-107">No se ha identificado ninguna operación.</span><span class="sxs-lookup"><span data-stu-id="1184c-107">No operation has been identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**\_operación WINBIO \_ abierta**</span><span class="sxs-lookup"><span data-stu-id="1184c-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO\_OPERATION\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-109">1</span><span class="sxs-lookup"><span data-stu-id="1184c-109">1</span></span>
</dt> <dt>



<span data-ttu-id="1184c-110">Se abrió una sesión biométrica.</span><span class="sxs-lookup"><span data-stu-id="1184c-110">A biometric session was opened.</span></span> <span data-ttu-id="1184c-111">Para obtener más información, consulte [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span><span class="sxs-lookup"><span data-stu-id="1184c-111">For more information see [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**cierre de la \_ operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO\_OPERATION\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-113">2</span><span class="sxs-lookup"><span data-stu-id="1184c-113">2</span></span>
</dt> <dt>



<span data-ttu-id="1184c-114">Se cerró una sesión biométrica.</span><span class="sxs-lookup"><span data-stu-id="1184c-114">A biometric session was closed.</span></span> <span data-ttu-id="1184c-115">Para obtener más información, vea [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span><span class="sxs-lookup"><span data-stu-id="1184c-115">For more information, see [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**comprobación de la \_ operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO\_OPERATION\_VERIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-117">3</span><span class="sxs-lookup"><span data-stu-id="1184c-117">3</span></span>
</dt> <dt>



<span data-ttu-id="1184c-118">Se ha comprobado un ejemplo biométrico con respecto a una identidad de usuario.</span><span class="sxs-lookup"><span data-stu-id="1184c-118">A biometric sample was verified against a user identity.</span></span> <span data-ttu-id="1184c-119">Para obtener más información, vea [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span><span class="sxs-lookup"><span data-stu-id="1184c-119">For more information, see [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**identificación de la \_ operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO\_OPERATION\_IDENTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-121">4</span><span class="sxs-lookup"><span data-stu-id="1184c-121">4</span></span>
</dt> <dt>



<span data-ttu-id="1184c-122">Se capturó un ejemplo biométrico y se comparaba con una plantilla existente.</span><span class="sxs-lookup"><span data-stu-id="1184c-122">A biometric sample was captured and compared to an existing template.</span></span> <span data-ttu-id="1184c-123">Para obtener más información, vea [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span><span class="sxs-lookup"><span data-stu-id="1184c-123">For more information, see [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**\_operación WINBIO \_ Buscar \_ sensor**</span><span class="sxs-lookup"><span data-stu-id="1184c-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO\_OPERATION\_LOCATE\_SENSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-125">5</span><span class="sxs-lookup"><span data-stu-id="1184c-125">5</span></span>
</dt> <dt>



<span data-ttu-id="1184c-126">Se recuperó el número de identificación de una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1184c-126">The ID number of a biometric unit was retrieved.</span></span> <span data-ttu-id="1184c-127">Para obtener más información, vea [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span><span class="sxs-lookup"><span data-stu-id="1184c-127">For more information, see [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**Inicio de la operación de WINBIO \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO\_OPERATION\_ENROLL\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-129">6</span><span class="sxs-lookup"><span data-stu-id="1184c-129">6</span></span>
</dt> <dt>



<span data-ttu-id="1184c-130">Se inició una secuencia de inscripción biométrica.</span><span class="sxs-lookup"><span data-stu-id="1184c-130">A biometric enrollment sequence was initiated.</span></span> <span data-ttu-id="1184c-131">Para obtener más información, vea [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span><span class="sxs-lookup"><span data-stu-id="1184c-131">For more information, see [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**captura de la operación de WINBIO de \_ \_ inscripción \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO\_OPERATION\_ENROLL\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-133">7</span><span class="sxs-lookup"><span data-stu-id="1184c-133">7</span></span>
</dt> <dt>



<span data-ttu-id="1184c-134">Se ha capturado una muestra biométrica y se ha agregado a la plantilla.</span><span class="sxs-lookup"><span data-stu-id="1184c-134">A biometric sample was captured and added to the template.</span></span> <span data-ttu-id="1184c-135">Para obtener más información, vea [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span><span class="sxs-lookup"><span data-stu-id="1184c-135">For more information, see [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**operación de inscripción de WINBIO de \_ \_ \_ confirmación**</span><span class="sxs-lookup"><span data-stu-id="1184c-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO\_OPERATION\_ENROLL\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-137">8</span><span class="sxs-lookup"><span data-stu-id="1184c-137">8</span></span>
</dt> <dt>



<span data-ttu-id="1184c-138">Se finalizó una plantilla biométrica pendiente.</span><span class="sxs-lookup"><span data-stu-id="1184c-138">A pending biometric template was finalized.</span></span> <span data-ttu-id="1184c-139">Para obtener más información, vea [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span><span class="sxs-lookup"><span data-stu-id="1184c-139">For more information, see [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**descartar la operación de WINBIO \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**WINBIO\_OPERATION\_ENROLL\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-141">9</span><span class="sxs-lookup"><span data-stu-id="1184c-141">9</span></span>
</dt> <dt>



<span data-ttu-id="1184c-142">Se descartó una plantilla biométrica pendiente.</span><span class="sxs-lookup"><span data-stu-id="1184c-142">A pending biometric template was discarded.</span></span> <span data-ttu-id="1184c-143">Para obtener más información, vea [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span><span class="sxs-lookup"><span data-stu-id="1184c-143">For more information, see [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**\_ \_ inscripciones de enumeración de operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**WINBIO\_OPERATION\_ENUM\_ENROLLMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-145">10</span><span class="sxs-lookup"><span data-stu-id="1184c-145">10</span></span>
</dt> <dt>



<span data-ttu-id="1184c-146">Se enumeraron los subfactores de una plantilla determinada.</span><span class="sxs-lookup"><span data-stu-id="1184c-146">The sub-factors for a given template were enumerated.</span></span> <span data-ttu-id="1184c-147">Para obtener más información, vea [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span><span class="sxs-lookup"><span data-stu-id="1184c-147">For more information, see [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO \_ operación \_ eliminar \_ plantilla**</span><span class="sxs-lookup"><span data-stu-id="1184c-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO\_OPERATION\_DELETE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-149">11</span><span class="sxs-lookup"><span data-stu-id="1184c-149">11</span></span>
</dt> <dt>



<span data-ttu-id="1184c-150">Se eliminó una plantilla biométrica del almacén.</span><span class="sxs-lookup"><span data-stu-id="1184c-150">A biometric template was deleted from the store.</span></span> <span data-ttu-id="1184c-151">Para obtener más información, vea [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span><span class="sxs-lookup"><span data-stu-id="1184c-151">For more information, see [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**\_ejemplo de \_ captura de operación de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**WINBIO\_OPERATION\_CAPTURE\_SAMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-153">12</span><span class="sxs-lookup"><span data-stu-id="1184c-153">12</span></span>
</dt> <dt>



<span data-ttu-id="1184c-154">Se capturó un ejemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="1184c-154">A biometric sample was captured.</span></span> <span data-ttu-id="1184c-155">Para obtener más información, vea [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span><span class="sxs-lookup"><span data-stu-id="1184c-155">For more information, see [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**\_propiedad de operación \_ Get \_ de WINBIO**</span><span class="sxs-lookup"><span data-stu-id="1184c-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO\_OPERATION\_GET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-157">13</span><span class="sxs-lookup"><span data-stu-id="1184c-157">13</span></span>
</dt> <dt>



<span data-ttu-id="1184c-158">Se recuperó una sesión biométrica, una unidad o una propiedad de plantilla.</span><span class="sxs-lookup"><span data-stu-id="1184c-158">A biometric session, unit, or template property was retrieved.</span></span> <span data-ttu-id="1184c-159">Para obtener más información, vea [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span><span class="sxs-lookup"><span data-stu-id="1184c-159">For more information, see [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**\_propiedad de \_ conjunto de operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO\_OPERATION\_SET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-161">14</span><span class="sxs-lookup"><span data-stu-id="1184c-161">14</span></span>
</dt> <dt>



<span data-ttu-id="1184c-162">Se estableció una sesión biométrica, una unidad, una plantilla o una propiedad de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="1184c-162">A biometric session, unit, template, or account property was set.</span></span> <span data-ttu-id="1184c-163">Para obtener más información, vea [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span><span class="sxs-lookup"><span data-stu-id="1184c-163">For more information, see [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**\_ \_ evento get de operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO\_OPERATION\_GET\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-165">15</span><span class="sxs-lookup"><span data-stu-id="1184c-165">15</span></span>
</dt> <dt>



<span data-ttu-id="1184c-166">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1184c-166">Not used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**\_unidad de \_ bloqueo de operación de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO\_OPERATION\_LOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-168">16</span><span class="sxs-lookup"><span data-stu-id="1184c-168">16</span></span>
</dt> <dt>



<span data-ttu-id="1184c-169">Una unidad biométrica se bloqueó para uso exclusivo de una sesión.</span><span class="sxs-lookup"><span data-stu-id="1184c-169">A biometric unit was locked for exclusive use by a session.</span></span> <span data-ttu-id="1184c-170">Para obtener más información, vea [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span><span class="sxs-lookup"><span data-stu-id="1184c-170">For more information, see [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**\_unidad de \_ desbloqueo de operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO\_OPERATION\_UNLOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-172">17</span><span class="sxs-lookup"><span data-stu-id="1184c-172">17</span></span>
</dt> <dt>



<span data-ttu-id="1184c-173">Se liberó el bloqueo de sesión en una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1184c-173">The session lock on a biometric unit was released.</span></span> <span data-ttu-id="1184c-174">Para obtener más información, vea [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span><span class="sxs-lookup"><span data-stu-id="1184c-174">For more information, see [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**\_unidad de \_ control de operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-176">18</span><span class="sxs-lookup"><span data-stu-id="1184c-176">18</span></span>
</dt> <dt>



<span data-ttu-id="1184c-177">Las operaciones definidas por el proveedor se realizaron en una unidad de control.</span><span class="sxs-lookup"><span data-stu-id="1184c-177">Vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="1184c-178">Para obtener más información, vea [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span><span class="sxs-lookup"><span data-stu-id="1184c-178">For more information, see [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**\_privilegio de \_ unidad de control de operación WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-180">19</span><span class="sxs-lookup"><span data-stu-id="1184c-180">19</span></span>
</dt> <dt>



<span data-ttu-id="1184c-181">Las operaciones definidas por el proveedor con privilegios se realizaron en una unidad de control.</span><span class="sxs-lookup"><span data-stu-id="1184c-181">Privileged vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="1184c-182">Para obtener más información, vea [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span><span class="sxs-lookup"><span data-stu-id="1184c-182">For more information, see [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**\_ \_ marco abierto de la operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO\_OPERATION\_OPEN\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-184">20</span><span class="sxs-lookup"><span data-stu-id="1184c-184">20</span></span>
</dt> <dt>



<span data-ttu-id="1184c-185">Se abrió un identificador del marco biométrico.</span><span class="sxs-lookup"><span data-stu-id="1184c-185">A handle to the biometric framework was opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**marco de cierre de la \_ operación WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO\_OPERATION\_CLOSE\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-187">21</span><span class="sxs-lookup"><span data-stu-id="1184c-187">21</span></span>
</dt> <dt>



<span data-ttu-id="1184c-188">Se cerró un identificador del marco biométrico.</span><span class="sxs-lookup"><span data-stu-id="1184c-188">A handle to the biometric framework was closed.</span></span> <span data-ttu-id="1184c-189">Para obtener más información, vea [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span><span class="sxs-lookup"><span data-stu-id="1184c-189">For more information, see [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**\_proveedores de \_ servicios de enumeración de operaciones WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**WINBIO\_OPERATION\_ENUM\_SERVICE\_PROVIDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-191">22</span><span class="sxs-lookup"><span data-stu-id="1184c-191">22</span></span>
</dt> <dt>



<span data-ttu-id="1184c-192">Se enumeraron los proveedores de servicios biométricos instalados.</span><span class="sxs-lookup"><span data-stu-id="1184c-192">The installed biometric service providers were enumerated.</span></span> <span data-ttu-id="1184c-193">Para obtener más información, vea [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span><span class="sxs-lookup"><span data-stu-id="1184c-193">For more information, see [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO de \_ operación de \_ enumeración de \_ unidades biométricas \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO\_OPERATION\_ENUM\_BIOMETRIC\_UNITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-195">23</span><span class="sxs-lookup"><span data-stu-id="1184c-195">23</span></span>
</dt> <dt>



<span data-ttu-id="1184c-196">Se enumeraron las unidades biométricas conectadas.</span><span class="sxs-lookup"><span data-stu-id="1184c-196">The attached biometric units were enumerated.</span></span> <span data-ttu-id="1184c-197">Para obtener más información, vea [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span><span class="sxs-lookup"><span data-stu-id="1184c-197">For more information, see [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**\_bases de \_ datos de enumeración de la operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**WINBIO\_OPERATION\_ENUM\_DATABASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-199">24</span><span class="sxs-lookup"><span data-stu-id="1184c-199">24</span></span>
</dt> <dt>



<span data-ttu-id="1184c-200">Se enumeraron las bases de datos registradas.</span><span class="sxs-lookup"><span data-stu-id="1184c-200">The registered databases were enumerated.</span></span> <span data-ttu-id="1184c-201">Para obtener más información, vea [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span><span class="sxs-lookup"><span data-stu-id="1184c-201">For more information, see [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**llegada de la \_ unidad de operación WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO\_OPERATION\_UNIT\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-203">25</span><span class="sxs-lookup"><span data-stu-id="1184c-203">25</span></span>
</dt> <dt>



<span data-ttu-id="1184c-204">Se creó una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1184c-204">A biometric unit was created.</span></span> <span data-ttu-id="1184c-205">Para obtener más información, vea [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="1184c-205">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**eliminación de la \_ unidad de operación WINBIO \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**WINBIO\_OPERATION\_UNIT\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-207">26</span><span class="sxs-lookup"><span data-stu-id="1184c-207">26</span></span>
</dt> <dt>



<span data-ttu-id="1184c-208">Se eliminó una unidad biométrica.</span><span class="sxs-lookup"><span data-stu-id="1184c-208">A biometric unit was deleted.</span></span> <span data-ttu-id="1184c-209">Para obtener más información, vea [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span><span class="sxs-lookup"><span data-stu-id="1184c-209">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**\_identificación de la operación WINBIO \_ y el \_ \_ vale de versión \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO\_OPERATION\_IDENTIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-211">27</span><span class="sxs-lookup"><span data-stu-id="1184c-211">27</span></span>
</dt> <dt>



<span data-ttu-id="1184c-212">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1184c-212">Reserved.</span></span> <span data-ttu-id="1184c-213">Este valor se admite a partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1184c-213">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**\_ \_ comprobación de operación \_ de WINBIO y \_ vale de versión \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO\_OPERATION\_VERIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-215">28</span><span class="sxs-lookup"><span data-stu-id="1184c-215">28</span></span>
</dt> <dt>



<span data-ttu-id="1184c-216">Reservado.</span><span class="sxs-lookup"><span data-stu-id="1184c-216">Reserved.</span></span> <span data-ttu-id="1184c-217">Este valor se admite a partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1184c-217">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**\_presencia del \_ monitor de operación WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**WINBIO\_OPERATION\_MONITOR\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-219">29</span><span class="sxs-lookup"><span data-stu-id="1184c-219">29</span></span>
</dt> <dt>



<span data-ttu-id="1184c-220">Se activó el mecanismo de reconocimiento facial o de supervisión de iris.</span><span class="sxs-lookup"><span data-stu-id="1184c-220">The facial recognition or iris monitoring mechanism was turned on.</span></span> <span data-ttu-id="1184c-221">Para obtener más información, vea [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span><span class="sxs-lookup"><span data-stu-id="1184c-221">For more information, see [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span></span> <span data-ttu-id="1184c-222">Este valor se admite a partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1184c-222">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1184c-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**\_operación de \_ inscripción de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="1184c-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO\_OPERATION\_ENROLL\_SELECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1184c-224">30</span><span class="sxs-lookup"><span data-stu-id="1184c-224">30</span></span>
</dt> <dt>



<span data-ttu-id="1184c-225">Un individuo de un grupo de individuos que están representados por los datos del búfer de ejemplo se ha especificado como el individuo que se va a inscribir.</span><span class="sxs-lookup"><span data-stu-id="1184c-225">An individual from a group of individuals that are represented by data in the sample buffer was specified as the individual to enroll.</span></span> <span data-ttu-id="1184c-226">Para obtener más información, vea [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span><span class="sxs-lookup"><span data-stu-id="1184c-226">For more information, see [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span></span> <span data-ttu-id="1184c-227">Este valor se admite a partir de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="1184c-227">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1184c-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1184c-228">Requirements</span></span>



| <span data-ttu-id="1184c-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="1184c-229">Requirement</span></span> | <span data-ttu-id="1184c-230">Value</span><span class="sxs-lookup"><span data-stu-id="1184c-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1184c-231">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1184c-231">Minimum supported client</span></span><br/> | <span data-ttu-id="1184c-232">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1184c-232">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="1184c-233">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1184c-233">Minimum supported server</span></span><br/> | <span data-ttu-id="1184c-234">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1184c-234">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="1184c-235">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1184c-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="1184c-236"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="1184c-236"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1184c-237">Vea también</span><span class="sxs-lookup"><span data-stu-id="1184c-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1184c-238">Constantes de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="1184c-238">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





