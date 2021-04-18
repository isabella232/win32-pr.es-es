---
description: Cancela la notificación de carga de DLL que se registró anteriormente mediante una llamada a la función LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: LdrUnregisterDllNotification función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423191"
---
# <a name="ldrunregisterdllnotification-function"></a><span data-ttu-id="ddb35-103">LdrUnregisterDllNotification función)</span><span class="sxs-lookup"><span data-stu-id="ddb35-103">LdrUnregisterDllNotification function</span></span>

<span data-ttu-id="ddb35-104">\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]</span><span class="sxs-lookup"><span data-stu-id="ddb35-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="ddb35-105">Cancela la notificación de carga de DLL que se registró anteriormente mediante una llamada a la función [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb35-105">Cancels DLL load notification previously registered by calling the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb35-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ddb35-106">Syntax</span></span>


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a><span data-ttu-id="ddb35-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ddb35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddb35-108">*Cookie* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ddb35-108">*Cookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ddb35-109">Un puntero al identificador de devolución de llamada recibido de la llamada [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) que se registró para la notificación.</span><span class="sxs-lookup"><span data-stu-id="ddb35-109">A pointer to the callback identifier received from the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) call that registered for notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddb35-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddb35-110">Return value</span></span>

<span data-ttu-id="ddb35-111">Devuelve un código de error **NTSTATUS** o.</span><span class="sxs-lookup"><span data-stu-id="ddb35-111">Returns an **NTSTATUS** or error code.</span></span>

<span data-ttu-id="ddb35-112">Si la función se ejecuta correctamente, devuelve el **estado \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="ddb35-112">If the function succeeds, it returns **STATUS\_SUCCESS**.</span></span>

<span data-ttu-id="ddb35-113">Si no se encuentra la función de devolución de llamada, la función devuelve el **estado \_ dll \_ no \_ encontrado**.</span><span class="sxs-lookup"><span data-stu-id="ddb35-113">If the callback function is not found, the function returns **STATUS\_DLL\_NOT\_FOUND**.</span></span>

<span data-ttu-id="ddb35-114">Los formularios y la importancia de los códigos de error de **NTSTATUS** se enumeran en el archivo de encabezado NTSTATUS. h disponible en el WDK y se describen en la documentación de WDK.</span><span class="sxs-lookup"><span data-stu-id="ddb35-114">The forms and significance of **NTSTATUS** error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb35-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ddb35-115">Remarks</span></span>

<span data-ttu-id="ddb35-116">Esta función no tiene ningún archivo de encabezado asociado.</span><span class="sxs-lookup"><span data-stu-id="ddb35-116">This function has no associated header file.</span></span> <span data-ttu-id="ddb35-117">La biblioteca de importación asociada, ntdll. lib, está disponible en el WDK.</span><span class="sxs-lookup"><span data-stu-id="ddb35-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="ddb35-118">También puede utilizar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="ddb35-118">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddb35-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddb35-119">Requirements</span></span>



| <span data-ttu-id="ddb35-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddb35-120">Requirement</span></span> | <span data-ttu-id="ddb35-121">Value</span><span class="sxs-lookup"><span data-stu-id="ddb35-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb35-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddb35-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ddb35-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ddb35-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ddb35-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ddb35-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ddb35-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ddb35-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ddb35-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ddb35-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddb35-127"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ddb35-127"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb35-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="ddb35-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb35-129">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="ddb35-129">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> </dl>

 

 
