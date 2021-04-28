---
description: 'SPFILENOTIFY_STARTREGISTRATION mensaje: al usar la directiva REGISTERDlls INF para registrar automáticamente archivos DLL, los llamadores de SetupInstallFromInfSection pueden recibir notificaciones en cada archivo a medida que se registra o se anula el registro.'
ms.assetid: 0faf277c-7805-478f-9cec-0dd7b6acdb0e
title: SPFILENOTIFY_STARTREGISTRATION mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47e71a884d079515436f296faf515a83a985311e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094503"
---
# <a name="spfilenotify_startregistration-message"></a><span data-ttu-id="c6df4-103">Mensaje DE SPFILENOTIFY \_ STARTREGISTRATION</span><span class="sxs-lookup"><span data-stu-id="c6df4-103">SPFILENOTIFY\_STARTREGISTRATION message</span></span>

<span data-ttu-id="c6df4-104">Al usar la **directiva REGISTERDlls** INF para registrar automáticamente archivos DLL, los llamadores de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) pueden recibir notificaciones en cada archivo a medida que se registra o se anula el registro.</span><span class="sxs-lookup"><span data-stu-id="c6df4-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="c6df4-105">Para enviar una notificación **SPFILENOTIFY \_ STARTREGISTRATION** a la rutina de devolución de llamada una vez antes de registrar un archivo, incluya SPINST \_ REGISTERCALLBACKAWARE más SPINST REGSVR en el parámetro \_ *Flags* de **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="c6df4-105">To send a **SPFILENOTIFY\_STARTREGISTRATION** notification to the callback routine once before registering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="c6df4-106">Para enviar una notificación de anulación del registro, incluya SPINST \_ REGISTERCALLBACKAWARE más SPINST UNREGSVR en el \_ *parámetro Flags.*</span><span class="sxs-lookup"><span data-stu-id="c6df4-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="c6df4-107">La rutina de devolución de llamada especificada por el parámetro *MsgHandler* de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) debe ser del tipo [PSP FILE \_ \_ CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="c6df4-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="c6df4-108">Establezca el *parámetro Context* en el mismo *contexto* especificado en **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="c6df4-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="c6df4-109">Establezca el *parámetro Notification* **en SPFILENOTIFY \_ STARTREGISTRATION**.</span><span class="sxs-lookup"><span data-stu-id="c6df4-109">Set the *Notification* parameter to **SPFILENOTIFY\_STARTREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_STARTREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="c6df4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c6df4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6df4-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="c6df4-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="c6df4-112">Puntero a una [**estructura SP REGISTER CONTROL \_ \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) que contiene información sobre el archivo que se está registrando o anulando el registro.</span><span class="sxs-lookup"><span data-stu-id="c6df4-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="c6df4-113">El **cbsize del** miembro debe establecerse en el tamaño de la estructura .</span><span class="sxs-lookup"><span data-stu-id="c6df4-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="c6df4-114">El **miembro FileName** debe establecerse en la ruta de acceso completa del archivo que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="c6df4-114">The **FileName** member should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="c6df4-115">**Win32Error** no se usa y debe establecerse en NO \_ ERROR.</span><span class="sxs-lookup"><span data-stu-id="c6df4-115">**Win32Error** is not used and should be set to NO\_ERROR.</span></span> <span data-ttu-id="c6df4-116">**FailureCode** no se usa y debe establecerse en SPREG \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="c6df4-116">**FailureCode** is not used and should be set to SPREG\_SUCCESS.</span></span>

</dd> <dt>

<span data-ttu-id="c6df4-117">*Param2*</span><span class="sxs-lookup"><span data-stu-id="c6df4-117">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="c6df4-118">Si el archivo se está registrando, *Param2* debe establecerse en un puntero a un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="c6df4-118">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="c6df4-119">Si se anula el registro del archivo, *Param2* debe establecerse en un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="c6df4-119">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6df4-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c6df4-120">Return value</span></span>

<span data-ttu-id="c6df4-121">Después de recibir la notificación, la función de devolución de llamada puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c6df4-121">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="c6df4-122">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c6df4-122">Return code</span></span>                                                                                  | <span data-ttu-id="c6df4-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6df4-123">Description</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c6df4-124"><dt>**FILEOP \_ ABORT**</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-124"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="c6df4-125">No registre ni desinscriba el archivo y detenga el procesamiento de la sección INF.</span><span class="sxs-lookup"><span data-stu-id="c6df4-125">Do not register or unregister the file and stop processing the INF section.</span></span><br/>             |
| <dl> <span data-ttu-id="c6df4-126"><dt>**FILEOP \_ DOIT**</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-126"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="c6df4-127">Registre o anula el registro del archivo y continúe procesando la sección INF.</span><span class="sxs-lookup"><span data-stu-id="c6df4-127">Register or unregister the file and continue processing the INF section.</span></span><br/>                |
| <dl> <span data-ttu-id="c6df4-128"><dt>**FILE \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-128"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="c6df4-129">Omitir el registro o la anulación del registro del archivo, pero continuar procesando la sección INF</span><span class="sxs-lookup"><span data-stu-id="c6df4-129">Skip registration or unregistration of the file but continue processing the INF section</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c6df4-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6df4-130">Requirements</span></span>



| <span data-ttu-id="c6df4-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6df4-131">Requirement</span></span> | <span data-ttu-id="c6df4-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c6df4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c6df4-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6df4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c6df4-134">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c6df4-134">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c6df4-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c6df4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c6df4-136">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="c6df4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c6df4-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6df4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6df4-138"><dt>Setupapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="c6df4-138"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6df4-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6df4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6df4-140">Información general</span><span class="sxs-lookup"><span data-stu-id="c6df4-140">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="c6df4-141">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="c6df4-141">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="c6df4-142">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="c6df4-142">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="c6df4-143">**SPFILENOTIFY \_ ENDREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="c6df4-143">**SPFILENOTIFY\_ENDREGISTRATION**</span></span>](spfilenotify-endregistration.md)
</dt> </dl>

 

