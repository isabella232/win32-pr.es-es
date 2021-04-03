---
description: Registra la notificación cuando se carga por primera vez un archivo DLL. Esta notificación se produce antes de que tenga lugar la vinculación dinámica.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: LdrRegisterDllNotification función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080109"
---
# <a name="ldrregisterdllnotification-function"></a><span data-ttu-id="c2449-104">LdrRegisterDllNotification función)</span><span class="sxs-lookup"><span data-stu-id="c2449-104">LdrRegisterDllNotification function</span></span>

<span data-ttu-id="c2449-105">\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]</span><span class="sxs-lookup"><span data-stu-id="c2449-105">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="c2449-106">Registra la notificación cuando se carga por primera vez un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="c2449-106">Registers for notification when a DLL is first loaded.</span></span> <span data-ttu-id="c2449-107">Esta notificación se produce antes de que tenga lugar la vinculación dinámica.</span><span class="sxs-lookup"><span data-stu-id="c2449-107">This notification occurs before dynamic linking takes place.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2449-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c2449-108">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="c2449-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c2449-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2449-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c2449-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2449-111">Este parámetro debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="c2449-111">This parameter must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c2449-112">*NotificationFunction* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="c2449-112">*NotificationFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2449-113">Puntero a una función de devolución de llamada de notificación [*LdrDllNotification*](ldrdllnotification.md) que se va a llamar cuando se cargue el archivo dll.</span><span class="sxs-lookup"><span data-stu-id="c2449-113">A pointer to an [*LdrDllNotification*](ldrdllnotification.md) notification callback function to call when the DLL is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="c2449-114">*Contexto* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c2449-114">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c2449-115">Un puntero a los datos de contexto de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c2449-115">A pointer to context data for the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="c2449-116">*Cookie* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="c2449-116">*Cookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2449-117">Un puntero a una variable para recibir un identificador de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="c2449-117">A pointer to a variable to receive an identifier for the callback function.</span></span> <span data-ttu-id="c2449-118">Este identificador se usa para anular el registro de la función de devolución de llamada de notificación.</span><span class="sxs-lookup"><span data-stu-id="c2449-118">This identifier is used to unregister the notification callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2449-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2449-119">Return value</span></span>

<span data-ttu-id="c2449-120">Si la función se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="c2449-120">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="c2449-121">Los formularios y la importancia de los códigos de error de **NTSTATUS** se enumeran en el archivo de encabezado NTSTATUS. h disponible en el WDK y se describen en la documentación de WDK.</span><span class="sxs-lookup"><span data-stu-id="c2449-121">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2449-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c2449-122">Remarks</span></span>

<span data-ttu-id="c2449-123">Esta función no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="c2449-123">This function has no associated header file.</span></span> <span data-ttu-id="c2449-124">La biblioteca de importación asociada, ntdll. lib, está disponible en el WDK.</span><span class="sxs-lookup"><span data-stu-id="c2449-124">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="c2449-125">También puede utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="c2449-125">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2449-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2449-126">Requirements</span></span>



| <span data-ttu-id="c2449-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2449-127">Requirement</span></span> | <span data-ttu-id="c2449-128">Value</span><span class="sxs-lookup"><span data-stu-id="c2449-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c2449-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2449-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c2449-130">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="c2449-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c2449-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c2449-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c2449-132">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="c2449-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c2449-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c2449-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2449-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2449-134"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2449-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="c2449-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2449-136">*LdrDllNotification*</span><span class="sxs-lookup"><span data-stu-id="c2449-136">*LdrDllNotification*</span></span>](ldrdllnotification.md)
</dt> <dt>

[<span data-ttu-id="c2449-137">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="c2449-137">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
