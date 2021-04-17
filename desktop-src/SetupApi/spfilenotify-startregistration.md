---
description: Cuando se usa la Directiva RegisterDlls INF para registrar automáticamente los archivos dll, los autores de la llamada de SetupInstallFromInfSection pueden recibir notificaciones en cada archivo a medida que se registra o se anula su registro.
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: Mensaje de SPFILENOTIFY_STARTREGISTRATION (setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe795af38c21c17bf4e81692985d4bfe50dc8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668171"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="1ee51-103">SPFILENOTIFY \_ STARTREGISTRATION</span><span class="sxs-lookup"><span data-stu-id="1ee51-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="1ee51-104">Cuando se usa la directiva **RegisterDlls** inf para registrar automáticamente los archivos dll, los autores de la llamada de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) pueden recibir notificaciones en cada archivo a medida que se registra o se anula su registro.</span><span class="sxs-lookup"><span data-stu-id="1ee51-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="1ee51-105">Para enviar una notificación de **SPFILENOTIFY \_ STARTREGISTRATION** a la rutina de devolución de llamada una vez antes de registrar un archivo, incluya \_ el bloque REGISTERCALLBACKAWARE más el marcador de giro \_ en el parámetro *Flags* de **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="1ee51-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="1ee51-106">Para enviar una notificación de anulación del registro, incluya \_ REGISTERCALLBACKAWARE más \_ de UNREGSVRs en el parámetro *Flags* .</span><span class="sxs-lookup"><span data-stu-id="1ee51-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="1ee51-107">La rutina de devolución de llamada especificada por el parámetro *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) debe ser el tipo de [devolución de \_ \_ llamada de archivo PSP](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="1ee51-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="1ee51-108">Establezca el parámetro de *contexto* en el mismo *contexto* especificado en **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="1ee51-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="1ee51-109">Establezca el parámetro de *notificación* en **SPFILENOTIFY \_ STARTREGISTRATION**.</span><span class="sxs-lookup"><span data-stu-id="1ee51-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="1ee51-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ee51-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee51-111">*Parámetro1*</span><span class="sxs-lookup"><span data-stu-id="1ee51-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee51-112">Puntero a una estructura de estado de control de registro de SP que contiene información sobre el archivo que se va a registrar o cuya registro se va a anular. [**\_ \_ \_**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa)</span><span class="sxs-lookup"><span data-stu-id="1ee51-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="1ee51-113">El miembro **cbsize** debe establecerse en el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="1ee51-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="1ee51-114">El miembro **filename** debe establecerse en la ruta de acceso completa del archivo que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="1ee51-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="1ee51-115">**Win32Error** no se utiliza y debe establecerse en ningún \_ error.</span><span class="sxs-lookup"><span data-stu-id="1ee51-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="1ee51-116">**FailureCode** no se utiliza y debe establecerse en SPREG \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1ee51-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="1ee51-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="1ee51-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee51-118">Si el archivo se está registrando, *parám2* debe establecerse en un puntero a un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="1ee51-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="1ee51-119">Si se va a anular el registro del archivo, *parám2* debe establecerse en un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="1ee51-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee51-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ee51-120">Return value</span></span>

<span data-ttu-id="1ee51-121">Después de recibir la notificación, la función de devolución de llamada puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1ee51-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="1ee51-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1ee51-122">Return code</span></span>                                                                                  | <span data-ttu-id="1ee51-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ee51-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ee51-124"><dt>**\_anulación de FILEOP**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee51-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="1ee51-125">No registre ni anule el registro del archivo y detenga el procesamiento de la sección INF.</span><span class="sxs-lookup"><span data-stu-id="1ee51-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="1ee51-126"><dt>**FILEOP \_ Doit**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee51-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="1ee51-127">Registre o anule el registro del archivo y continúe procesando la sección INF.</span><span class="sxs-lookup"><span data-stu-id="1ee51-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="1ee51-128"><dt>**\_Omitir archivo**</dt></span><span class="sxs-lookup"><span data-stu-id="1ee51-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="1ee51-129">Omitir el registro o anular el registro del archivo, pero continuar procesando la sección INF</span><span class="sxs-lookup"><span data-stu-id="1ee51-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1ee51-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ee51-130">Requirements</span></span>



| <span data-ttu-id="1ee51-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ee51-131">Requirement</span></span> | <span data-ttu-id="1ee51-132">Value</span><span class="sxs-lookup"><span data-stu-id="1ee51-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ee51-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ee51-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1ee51-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1ee51-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1ee51-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1ee51-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1ee51-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1ee51-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1ee51-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1ee51-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ee51-138"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ee51-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ee51-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ee51-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee51-140">Información general</span><span class="sxs-lookup"><span data-stu-id="1ee51-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="1ee51-141">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="1ee51-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="1ee51-142">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="1ee51-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="1ee51-143">**SPFILENOTIFY \_ ENDREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="1ee51-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

