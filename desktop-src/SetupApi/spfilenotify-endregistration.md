---
description: 'SPFILENOTIFY_ENDREGISTRATION mensaje: al usar la directiva REGISTERDlls INF para registrar automáticamente los archivos DLL, los autores de la llamada de SetupInstallFromInfSection pueden recibir notificaciones en cada archivo a medida que se registran o anulan el registro.'
ms.assetid: 6304f406-c9f8-41cc-a7b7-5ef606f62efb
title: SPFILENOTIFY_ENDREGISTRATION mensaje (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec341c26f9f88390ff1b807e6e932b3b381cd57
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094513"
---
# <a name="spfilenotify_endregistration-message"></a><span data-ttu-id="6e243-103">Mensaje SPFILENOTIFY \_ ENDREGISTRATION</span><span class="sxs-lookup"><span data-stu-id="6e243-103">SPFILENOTIFY\_ENDREGISTRATION message</span></span>

<span data-ttu-id="6e243-104">Cuando se usa la directiva **REGISTERDlls** INF para registrar automáticamente los archivos DLL, los autores de la llamada de [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) pueden recibir notificaciones en cada archivo a medida que se registran o anulan el registro.</span><span class="sxs-lookup"><span data-stu-id="6e243-104">When using the **RegisterDlls** INF directive to self-register DLLs, callers of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) may receive notifications on each file as it is registered or unregistered.</span></span> <span data-ttu-id="6e243-105">Para enviar una notificación **SPFILENOTIFY \_ ENDREGISTRATION** a una rutina de devolución de llamada una vez después de registrar o anular el registro de un archivo, incluya SPINST \_ REGISTERCALLBACKAWARE más SPINST REGSVR en el parámetro \_ *Flags* de **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="6e243-105">To send a **SPFILENOTIFY\_ENDREGISTRATION** notification to a callback routine once after registering or unregistering a file, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_REGSVR in the *Flags* parameter of **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="6e243-106">Para enviar una notificación de anulación del registro, incluya SPINST \_ REGISTERCALLBACKAWARE más SPINST \_ UNREGSVR en el *parámetro Flags.*</span><span class="sxs-lookup"><span data-stu-id="6e243-106">To send notification of unregistration, include SPINST\_REGISTERCALLBACKAWARE plus SPINST\_UNREGSVR in the *Flags* parameter.</span></span>

<span data-ttu-id="6e243-107">La rutina de devolución de llamada especificada por el parámetro *MsgHandler* [**de SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) debe ser del tipo [PSP FILE \_ \_ CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span><span class="sxs-lookup"><span data-stu-id="6e243-107">The callback routine specified by the *MsgHandler* parameter of [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) must be the type [PSP\_FILE\_CALLBACK](/windows/win32/api/setupapi/nc-setupapi-psp_file_callback_a).</span></span> <span data-ttu-id="6e243-108">Establezca el *parámetro Context* en el mismo *contexto* especificado en **SetupInstallFromInfSection**.</span><span class="sxs-lookup"><span data-stu-id="6e243-108">Set the *Context* parameter to the same *Context* specified in **SetupInstallFromInfSection**.</span></span> <span data-ttu-id="6e243-109">Establezca el *parámetro Notification* en **SPFILENOTIFY \_ ENDREGISTRATION**.</span><span class="sxs-lookup"><span data-stu-id="6e243-109">Set the *Notification* parameter to **SPFILENOTIFY\_ENDREGISTRATION**.</span></span>


```C++
SPFILENOTIFY_ENDREGISTRATION
  Param1 = (UINT_PTR) pointer to file information;
  Param2 = (UINT_PTR) file registration or unregistration;
            
```



## <a name="parameters"></a><span data-ttu-id="6e243-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6e243-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e243-111">*Param1*</span><span class="sxs-lookup"><span data-stu-id="6e243-111">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="6e243-112">Puntero a una [**estructura SP REGISTER CONTROL \_ \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) que contiene información sobre el archivo que se está registrando o anulando el registro.</span><span class="sxs-lookup"><span data-stu-id="6e243-112">Pointer to a [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa) structure containing information about the file being registered or unregistered.</span></span> <span data-ttu-id="6e243-113">El **cbsize del** miembro debe establecerse en el tamaño de la estructura.</span><span class="sxs-lookup"><span data-stu-id="6e243-113">The member **cbsize** should be set to the size of the structure.</span></span> <span data-ttu-id="6e243-114">**FileName** debe establecerse en la ruta de acceso completa del archivo que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="6e243-114">**FileName** should be set to the fully qualified path of the file being registered.</span></span> <span data-ttu-id="6e243-115">**Win32Error debe** establecerse en un código [de error del sistema](/windows/desktop/Debug/system-error-codes) que indique un código de error extendido.</span><span class="sxs-lookup"><span data-stu-id="6e243-115">**Win32Error** should be set to a [system error code](/windows/desktop/Debug/system-error-codes) indicating an extended error code.</span></span> <span data-ttu-id="6e243-116">**FailureCode** debe establecerse en uno de los códigos de error válidos que indican el resultado del registro.</span><span class="sxs-lookup"><span data-stu-id="6e243-116">**FailureCode** should be set to one of the valid failure codes indicating the outcome of the registration.</span></span> <span data-ttu-id="6e243-117">Para obtener códigos de error válidos, [**vea SP REGISTER CONTROL \_ \_ \_ STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span><span class="sxs-lookup"><span data-stu-id="6e243-117">For valid failure codes see [**SP\_REGISTER\_CONTROL\_STATUS**](/windows/desktop/api/Setupapi/ns-setupapi-sp_register_control_statusa).</span></span>

</dd> <dt>

<span data-ttu-id="6e243-118">*Param2*</span><span class="sxs-lookup"><span data-stu-id="6e243-118">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="6e243-119">Si el archivo se está registrando, *Param2* debe establecerse en un puntero a un valor distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="6e243-119">If the file is being registered, *Param2* should be set to a pointer to a nonzero value.</span></span> <span data-ttu-id="6e243-120">Si se anula el registro del archivo, *Param2* debe establecerse en un puntero a cero.</span><span class="sxs-lookup"><span data-stu-id="6e243-120">If the file is being unregistered, *Param2* should be set to a pointer to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e243-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e243-121">Return value</span></span>

<span data-ttu-id="6e243-122">Después de recibir la notificación, la función de devolución de llamada puede devolver uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6e243-122">After receiving notification, the callback function may return one of the following values.</span></span>



| <span data-ttu-id="6e243-123">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="6e243-123">Return code</span></span>                                                                                  | <span data-ttu-id="6e243-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e243-124">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="6e243-125"><dt>**FILEOP \_ ABORT**</dt></span><span class="sxs-lookup"><span data-stu-id="6e243-125"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="6e243-126">Detenga el procesamiento de la sección INF.</span><span class="sxs-lookup"><span data-stu-id="6e243-126">Stop processing the INF section.</span></span><br/>     |
| <dl> <span data-ttu-id="6e243-127"><dt>**FILEOP \_ DOIT**</dt></span><span class="sxs-lookup"><span data-stu-id="6e243-127"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="6e243-128">Continúe procesando la sección INF.</span><span class="sxs-lookup"><span data-stu-id="6e243-128">Continue processing the INF section.</span></span><br/> |
| <dl> <span data-ttu-id="6e243-129"><dt>**FILE \_ SKIP**</dt></span><span class="sxs-lookup"><span data-stu-id="6e243-129"><dt>**FILE\_SKIP**</dt></span></span> </dl>    | <span data-ttu-id="6e243-130">Continuar procesando la sección INF</span><span class="sxs-lookup"><span data-stu-id="6e243-130">Continue processing the INF section</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="6e243-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e243-131">Requirements</span></span>



| <span data-ttu-id="6e243-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e243-132">Requirement</span></span> | <span data-ttu-id="6e243-133">Valor</span><span class="sxs-lookup"><span data-stu-id="6e243-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6e243-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e243-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6e243-135">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6e243-135">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6e243-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6e243-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6e243-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6e243-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6e243-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6e243-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e243-139"><dt>Setupapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="6e243-139"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e243-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6e243-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e243-141">Información general</span><span class="sxs-lookup"><span data-stu-id="6e243-141">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="6e243-142">Notificaciones</span><span class="sxs-lookup"><span data-stu-id="6e243-142">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="6e243-143">**SetupInstallFromInfSection**</span><span class="sxs-lookup"><span data-stu-id="6e243-143">**SetupInstallFromInfSection**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> <dt>

[<span data-ttu-id="6e243-144">**SPFILENOTIFY \_ STARTREGISTRATION**</span><span class="sxs-lookup"><span data-stu-id="6e243-144">**SPFILENOTIFY\_STARTREGISTRATION**</span></span>](spfilenotify-startregistration.md)
</dt> </dl>

 

