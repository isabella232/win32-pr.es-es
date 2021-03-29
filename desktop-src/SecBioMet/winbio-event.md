---
title: Estructura de WINBIO_EVENT (Winbio \_ Types. h)
description: Contiene la información de estado que se envía a la rutina de devolución de llamada cuando se produce un aviso de evento.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- Plataforma de biometría de Windows API de WINBIO_EVENT Structure
- PWINBIO_EVENT de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666059"
---
# <a name="winbio_event-structure"></a><span data-ttu-id="b58da-105">WINBIO ( \_ estructura de eventos)</span><span class="sxs-lookup"><span data-stu-id="b58da-105">WINBIO\_EVENT structure</span></span>

<span data-ttu-id="b58da-106">La estructura de **\_ eventos WINBIO** contiene la información de estado que se envía a la rutina de devolución de llamada cuando se genera un aviso de eventos.</span><span class="sxs-lookup"><span data-stu-id="b58da-106">The **WINBIO\_EVENT** structure contains status information sent to the callback routine when an event notice is raised.</span></span>

## <a name="syntax"></a><span data-ttu-id="b58da-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b58da-107">Syntax</span></span>


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a><span data-ttu-id="b58da-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="b58da-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="b58da-109">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="b58da-109">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-110">Valor que especifica el tipo de aviso de eventos del proveedor de servicios generado.</span><span class="sxs-lookup"><span data-stu-id="b58da-110">A value that specifies the type of service provider event notice raised.</span></span> <span data-ttu-id="b58da-111">El único proveedor admitido actualmente es el sensor de huellas digitales.</span><span class="sxs-lookup"><span data-stu-id="b58da-111">The only provider currently supported is the fingerprint sensor.</span></span> <span data-ttu-id="b58da-112">Este sensor admite las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="b58da-112">This sensor supports the following flags.</span></span>

<dl> <dt>

<span data-ttu-id="b58da-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENTO \_ FP no \_ reclamado** (el sensor ha detectado un dedo deslizante que no fue solicitado por la aplicación o por la ventana que actualmente tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="b58da-113"><span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="b58da-114">El Plataforma de biometría de Windows llama a la función de devolución de llamada para indicar que se ha producido un deslizamiento de dedo pero no intenta identificar la huella digital).</span><span class="sxs-lookup"><span data-stu-id="b58da-114">The Windows Biometric Framework calls into your callback function to indicate that a finger swipe has occurred but does not try to identify the fingerprint.)</span></span>
</dt> <dt>

<span data-ttu-id="b58da-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ El evento \_ FP no \_ reclamado \_ identifica** (el sensor ha detectado un dedo deslizante que no fue solicitado por la aplicación o por la ventana que actualmente tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="b58da-115"><span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO\_EVENT\_FP\_UNCLAIMED\_IDENTIFY** (The sensor detected a finger swipe that was not requested by the application or by the window that currently has focus.</span></span> <span data-ttu-id="b58da-116">El Plataforma de biometría de Windows intenta identificar la huella digital y pasa el resultado de ese proceso a la función de devolución de llamada).</span><span class="sxs-lookup"><span data-stu-id="b58da-116">The Windows Biometric Framework attempts to identify the fingerprint and passes the result of that process to your callback function.)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b58da-117">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="b58da-117">**Parameters**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b58da-118">**Reclamación**</span><span class="sxs-lookup"><span data-stu-id="b58da-118">**Unclaimed**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-119">Estructura devuelta para la captura de ejemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="b58da-119">Structure returned for biometric sample capture.</span></span>

<dl> <dt>

<span data-ttu-id="b58da-120">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="b58da-120">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-121">Unidad biométrica que generó el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b58da-121">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="b58da-122">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="b58da-122">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-123">Valor **ULong** que contiene información adicional relacionada con errores para capturar un ejemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="b58da-123">A **ULONG** value that contains additional information regarding failure to capture a biometric sample.</span></span> <span data-ttu-id="b58da-124">Si una captura se realiza correctamente, este parámetro se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="b58da-124">If a capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="b58da-125">Los siguientes valores se definen para la captura de huellas digitales:</span><span class="sxs-lookup"><span data-stu-id="b58da-125">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="b58da-126">WINBIO \_ FP \_ demasiado \_ alto</span><span class="sxs-lookup"><span data-stu-id="b58da-126">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="b58da-127">WINBIO \_ FP \_ demasiado \_ bajo</span><span class="sxs-lookup"><span data-stu-id="b58da-127">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="b58da-128">WINBIO \_ FP \_ demasiado a la \_ izquierda</span><span class="sxs-lookup"><span data-stu-id="b58da-128">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="b58da-129">WINBIO \_ FP \_ demasiado a la \_ derecha</span><span class="sxs-lookup"><span data-stu-id="b58da-129">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="b58da-130">WINBIO \_ FP \_ demasiado \_ rápido</span><span class="sxs-lookup"><span data-stu-id="b58da-130">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="b58da-131">WINBIO \_ FP \_ demasiado \_ lento</span><span class="sxs-lookup"><span data-stu-id="b58da-131">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="b58da-132">WINBIO \_ FP \_ de \_ calidad deficiente</span><span class="sxs-lookup"><span data-stu-id="b58da-132">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="b58da-133">WINBIO \_ FP \_ demasiado \_ sesgado</span><span class="sxs-lookup"><span data-stu-id="b58da-133">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="b58da-134">WINBIO \_ FP \_ demasiado \_ corto</span><span class="sxs-lookup"><span data-stu-id="b58da-134">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="b58da-135">\_error de \_ combinación de FP de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="b58da-135">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b58da-136">**UnclaimedIdentify**</span><span class="sxs-lookup"><span data-stu-id="b58da-136">**UnclaimedIdentify**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-137">Estructura devuelta para la captura e identificación biométricas.</span><span class="sxs-lookup"><span data-stu-id="b58da-137">Structure returned for biometric capture and identification.</span></span> <span data-ttu-id="b58da-138">La identificación determina si un ejemplo puede asociarse a una plantilla biométrica existente.</span><span class="sxs-lookup"><span data-stu-id="b58da-138">Identification determines whether a sample can be associated with an existing biometric template.</span></span>

<dl> <dt>

<span data-ttu-id="b58da-139">**UnitId**</span><span class="sxs-lookup"><span data-stu-id="b58da-139">**UnitId**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-140">Unidad biométrica que generó el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b58da-140">The biometric unit that generated the sample.</span></span>

</dd> <dt>

<span data-ttu-id="b58da-141">**Identidad**</span><span class="sxs-lookup"><span data-stu-id="b58da-141">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-142">Una estructura de [**\_ identidad WINBIO**](winbio-identity.md) que contiene el GUID o SID del usuario que proporciona el ejemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="b58da-142">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that contains the GUID or SID of the user providing the biometric sample.</span></span>

</dd> <dt>

<span data-ttu-id="b58da-143">**Subfactor**</span><span class="sxs-lookup"><span data-stu-id="b58da-143">**SubFactor**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-144">Valor [**de \_ \_ subtipo biométrico WINBIO**](winbio-biometric-subtype-constants.md) que especifica el subfactor asociado a un ejemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="b58da-144">A [**WINBIO\_BIOMETRIC\_SUBTYPE**](winbio-biometric-subtype-constants.md) value that specifies the sub-factor associated with a biometric sample.</span></span> <span data-ttu-id="b58da-145">Actualmente, Plataforma de biometría de Windows (WBF) solo admite la captura de huellas digitales y usa las siguientes constantes para representar la información de subtipo.</span><span class="sxs-lookup"><span data-stu-id="b58da-145">The Windows Biometric Framework (WBF) currently supports only fingerprint capture and uses the following constants to represent sub-type information.</span></span>

-   <span data-ttu-id="b58da-146">WINBIO \_ ANSI \_ 381 \_ pos \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="b58da-146">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="b58da-147">\_Thumb WINBIO ANSI \_ 381 \_ pos \_ RH \_</span><span class="sxs-lookup"><span data-stu-id="b58da-147">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="b58da-148">\_Dedo de \_ \_ \_ \_ índice RH \_ de WINBIO ANSI 381 pos</span><span class="sxs-lookup"><span data-stu-id="b58da-148">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="b58da-149">\_Dedo central de WINBIO ANSI \_ 381 \_ pos \_ dcha \_ \_</span><span class="sxs-lookup"><span data-stu-id="b58da-149">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="b58da-150">\_Dedo de \_ \_ \_ \_ anillo RH \_ de WINBIO ANSI 381 pos</span><span class="sxs-lookup"><span data-stu-id="b58da-150">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="b58da-151">\_ \_ \_ \_ \_ Pequeño \_ dedo de WINBIO ANSI 381 pos</span><span class="sxs-lookup"><span data-stu-id="b58da-151">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="b58da-152">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Thumb</span><span class="sxs-lookup"><span data-stu-id="b58da-152">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="b58da-153">WINBIO \_ de \_ Índice de LH de pdv ANSI 381 \_ pos \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b58da-153">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="b58da-154">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ central \_</span><span class="sxs-lookup"><span data-stu-id="b58da-154">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="b58da-155">WINBIO \_ el \_ \_ dedo de \_ anillo de LH ANSI 381 pos \_ \_</span><span class="sxs-lookup"><span data-stu-id="b58da-155">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="b58da-156">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger</span><span class="sxs-lookup"><span data-stu-id="b58da-156">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="b58da-157">WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ cuatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="b58da-157">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="b58da-158">WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ cuatro \_ dedos</span><span class="sxs-lookup"><span data-stu-id="b58da-158">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="b58da-159">WINBIO \_ ANSI \_ 381 \_ pos \_ dos \_ Thumbs</span><span class="sxs-lookup"><span data-stu-id="b58da-159">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="b58da-160">No intente validar el valor proporcionado para el valor del *subfactor* .</span><span class="sxs-lookup"><span data-stu-id="b58da-160">Do not attempt to validate the value supplied for the *SubFactor* value.</span></span> <span data-ttu-id="b58da-161">El servicio biométrico de Windows validará el valor proporcionado antes de pasarlo a su implementación.</span><span class="sxs-lookup"><span data-stu-id="b58da-161">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="b58da-162">Si el valor es **WINBIO \_ SubType \_ no \_ Information** o **WINBIO \_ SubType \_ any**, valide cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="b58da-162">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

</dd> <dt>

<span data-ttu-id="b58da-163">**RejectDetail**</span><span class="sxs-lookup"><span data-stu-id="b58da-163">**RejectDetail**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-164">Valor **ULong** que contiene información adicional sobre el error para capturar un ejemplo biométrico.</span><span class="sxs-lookup"><span data-stu-id="b58da-164">A **ULONG** value that contains additional information about the failure to capture a biometric sample.</span></span> <span data-ttu-id="b58da-165">Si la captura se realiza correctamente, este parámetro se establece en cero.</span><span class="sxs-lookup"><span data-stu-id="b58da-165">If the capture succeeded, this parameter is set to zero.</span></span> <span data-ttu-id="b58da-166">Los siguientes valores se definen para la captura de huellas digitales:</span><span class="sxs-lookup"><span data-stu-id="b58da-166">The following values are defined for fingerprint capture:</span></span>

-   <span data-ttu-id="b58da-167">WINBIO \_ FP \_ demasiado \_ alto</span><span class="sxs-lookup"><span data-stu-id="b58da-167">WINBIO\_FP\_TOO\_HIGH</span></span>
-   <span data-ttu-id="b58da-168">WINBIO \_ FP \_ demasiado \_ bajo</span><span class="sxs-lookup"><span data-stu-id="b58da-168">WINBIO\_FP\_TOO\_LOW</span></span>
-   <span data-ttu-id="b58da-169">WINBIO \_ FP \_ demasiado a la \_ izquierda</span><span class="sxs-lookup"><span data-stu-id="b58da-169">WINBIO\_FP\_TOO\_LEFT</span></span>
-   <span data-ttu-id="b58da-170">WINBIO \_ FP \_ demasiado a la \_ derecha</span><span class="sxs-lookup"><span data-stu-id="b58da-170">WINBIO\_FP\_TOO\_RIGHT</span></span>
-   <span data-ttu-id="b58da-171">WINBIO \_ FP \_ demasiado \_ rápido</span><span class="sxs-lookup"><span data-stu-id="b58da-171">WINBIO\_FP\_TOO\_FAST</span></span>
-   <span data-ttu-id="b58da-172">WINBIO \_ FP \_ demasiado \_ lento</span><span class="sxs-lookup"><span data-stu-id="b58da-172">WINBIO\_FP\_TOO\_SLOW</span></span>
-   <span data-ttu-id="b58da-173">WINBIO \_ FP \_ de \_ calidad deficiente</span><span class="sxs-lookup"><span data-stu-id="b58da-173">WINBIO\_FP\_POOR\_QUALITY</span></span>
-   <span data-ttu-id="b58da-174">WINBIO \_ FP \_ demasiado \_ sesgado</span><span class="sxs-lookup"><span data-stu-id="b58da-174">WINBIO\_FP\_TOO\_SKEWED</span></span>
-   <span data-ttu-id="b58da-175">WINBIO \_ FP \_ demasiado \_ corto</span><span class="sxs-lookup"><span data-stu-id="b58da-175">WINBIO\_FP\_TOO\_SHORT</span></span>
-   <span data-ttu-id="b58da-176">\_error de \_ combinación de FP de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="b58da-176">WINBIO\_FP\_MERGE\_FAILURE</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b58da-177">**Error**</span><span class="sxs-lookup"><span data-stu-id="b58da-177">**Error**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-178">Estructura que identifica el éxito o el error de la operación que se está supervisando.</span><span class="sxs-lookup"><span data-stu-id="b58da-178">Structure that identifies the success or failure of the operation being monitored.</span></span>

<dl> <dt>

<span data-ttu-id="b58da-179">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="b58da-179">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="b58da-180">Valor **HRESULT** que contiene \_ un código de error o que es correcto debido a los cálculos realizados por el plataforma de biometría de Windows.</span><span class="sxs-lookup"><span data-stu-id="b58da-180">**HRESULT** value that contains S\_OK or an error code that resulted from computations performed by the Windows Biometric Framework.</span></span>

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b58da-181">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b58da-181">Remarks</span></span>

<span data-ttu-id="b58da-182">Llame a la función [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para registrar una rutina de devolución de llamada con el fin de recibir notificaciones de eventos del plataforma de biometría de Windows.</span><span class="sxs-lookup"><span data-stu-id="b58da-182">Call the [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) function to register a callback routine to receive event notifications from the Windows Biometric Framework.</span></span> <span data-ttu-id="b58da-183">La devolución de llamada es una función personalizada que debe definir para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b58da-183">The callback is a custom function that you must define for your application.</span></span>

## <a name="requirements"></a><span data-ttu-id="b58da-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b58da-184">Requirements</span></span>



| <span data-ttu-id="b58da-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="b58da-185">Requirement</span></span> | <span data-ttu-id="b58da-186">Value</span><span class="sxs-lookup"><span data-stu-id="b58da-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b58da-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b58da-187">Minimum supported client</span></span><br/> | <span data-ttu-id="b58da-188">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="b58da-188">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="b58da-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b58da-189">Minimum supported server</span></span><br/> | <span data-ttu-id="b58da-190">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="b58da-190">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="b58da-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b58da-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="b58da-192"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b58da-192"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b58da-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="b58da-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b58da-194">Estructuras de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="b58da-194">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="b58da-195">**WinBioRegisterEventMonitor**</span><span class="sxs-lookup"><span data-stu-id="b58da-195">**WinBioRegisterEventMonitor**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





