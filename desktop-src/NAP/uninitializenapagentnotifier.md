---
title: Función UninitializeNapAgentNotifier (NapUtil. h)
description: Cancela la suscripción del proceso de llamada de las notificaciones de cambio de estado de NapAgent y las notificaciones de cambio de estado de cuarentena.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- UninitializeNapAgentNotifier función NAP
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422175"
---
# <a name="uninitializenapagentnotifier-function"></a><span data-ttu-id="57ba6-104">UninitializeNapAgentNotifier función)</span><span class="sxs-lookup"><span data-stu-id="57ba6-104">UninitializeNapAgentNotifier function</span></span>

> [!Note]  
> <span data-ttu-id="57ba6-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="57ba6-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="57ba6-106">La función **UninitializeNapAgentNotifier** anula la suscripción del proceso de llamada de las notificaciones de cambio de estado NapAgent y las notificaciones de cambio de estado de cuarentena.</span><span class="sxs-lookup"><span data-stu-id="57ba6-106">The **UninitializeNapAgentNotifier** function unsubscribes the calling process from NapAgent state change notifications and quarantine state change notifications.</span></span> <span data-ttu-id="57ba6-107">Estas notificaciones las proporciona el servicio NapAgent.</span><span class="sxs-lookup"><span data-stu-id="57ba6-107">These notifications are provided by the NapAgent service.</span></span>

## <a name="syntax"></a><span data-ttu-id="57ba6-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="57ba6-108">Syntax</span></span>


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a><span data-ttu-id="57ba6-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="57ba6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ba6-110">*tipo* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="57ba6-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ba6-111">Valor [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica el tipo de notificaciones de servicio del que se va a cancelar la suscripción.</span><span class="sxs-lookup"><span data-stu-id="57ba6-111">A [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) value that specifies the type of service notifications to unsubscribe from.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57ba6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="57ba6-112">Return value</span></span>

<span data-ttu-id="57ba6-113">Esta función no tiene valores devueltos.</span><span class="sxs-lookup"><span data-stu-id="57ba6-113">This function has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="57ba6-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="57ba6-114">Remarks</span></span>

<span data-ttu-id="57ba6-115">Esta función no es segura para los subprocesos.</span><span class="sxs-lookup"><span data-stu-id="57ba6-115">This function is not thread safe.</span></span>

<span data-ttu-id="57ba6-116">Cada proceso suscrito a notificaciones de servicio de NapAgent del *tipo* especificado debe llamar a **UninitializeNapAgentNotifier** para cancelar la suscripción a las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="57ba6-116">Each process subscribed to NapAgent service notifications of the specified *type* must call **UninitializeNapAgentNotifier** to unsubscribe from notifications.</span></span> <span data-ttu-id="57ba6-117">Si un proceso está suscrito a más de un tipo de notificación, debe llamar a **UninitializeNapAgentNotifier** una vez para cada tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="57ba6-117">If a process is subscribed to more than one type of notification, it must call **UninitializeNapAgentNotifier** once for each type of notification.</span></span>

<span data-ttu-id="57ba6-118">Esta función producirá un error en modo silencioso si el proceso no había llamado previamente a [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) para el tipo de notificación.</span><span class="sxs-lookup"><span data-stu-id="57ba6-118">This function will fail silently if the process had not previously called [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) for the notification type.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ba6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57ba6-119">Requirements</span></span>



| <span data-ttu-id="57ba6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="57ba6-120">Requirement</span></span> | <span data-ttu-id="57ba6-121">Value</span><span class="sxs-lookup"><span data-stu-id="57ba6-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="57ba6-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57ba6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="57ba6-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="57ba6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="57ba6-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="57ba6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="57ba6-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="57ba6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="57ba6-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="57ba6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="57ba6-127"><dt>NapUtil. h</dt></span><span class="sxs-lookup"><span data-stu-id="57ba6-127"><dt>NapUtil.h</dt></span></span> </dl> |
| <span data-ttu-id="57ba6-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="57ba6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57ba6-129"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57ba6-129"><dt>Qutil.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ba6-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="57ba6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ba6-131">**InitializeNapAgentNotifier**</span><span class="sxs-lookup"><span data-stu-id="57ba6-131">**InitializeNapAgentNotifier**</span></span>](initializenapagentnotifier.md)
</dt> </dl>

 

 





