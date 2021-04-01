---
description: Función de devolución de llamada de notificación especificada con la función LdrRegisterDllNotification.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Función de devolución de llamada LdrDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906953"
---
# <a name="ldrdllnotification-callback-function"></a><span data-ttu-id="3533e-103">Función de devolución de llamada LdrDllNotification</span><span class="sxs-lookup"><span data-stu-id="3533e-103">LdrDllNotification callback function</span></span>

<span data-ttu-id="3533e-104">\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]</span><span class="sxs-lookup"><span data-stu-id="3533e-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="3533e-105">Función de devolución de llamada de notificación especificada con la función [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="3533e-105">A notification callback function specified with the [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) function.</span></span> <span data-ttu-id="3533e-106">El cargador llama a esta función cuando se carga por primera vez un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="3533e-106">The loader calls this function when a DLL is first loaded.</span></span>

<span data-ttu-id="3533e-107">**ADVERTENCIA:** No es seguro que la función de devolución de llamada de notificación llame a funciones en cualquier DLL.</span><span class="sxs-lookup"><span data-stu-id="3533e-107">**Warning:** It is unsafe for the notification callback function to call functions in any DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="3533e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3533e-108">Syntax</span></span>


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a><span data-ttu-id="3533e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3533e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3533e-110">*NotificationReason* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3533e-110">*NotificationReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3533e-111">Motivo por el que se llamó a la función de devolución de llamada de notificación.</span><span class="sxs-lookup"><span data-stu-id="3533e-111">The reason that the notification callback function was called.</span></span> <span data-ttu-id="3533e-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3533e-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3533e-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3533e-113">Value</span></span>                                                                                                                                                                                                                                                                                        | <span data-ttu-id="3533e-114">Significado</span><span class="sxs-lookup"><span data-stu-id="3533e-114">Meaning</span></span>                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <span data-ttu-id="3533e-115"><dt>**LDR \_ Motivo de notificación de DLL \_ \_ \_ cargado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3533e-115"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_LOADED**</dt> <dt>1</dt></span></span> </dl>       | <span data-ttu-id="3533e-116">Se cargó el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="3533e-116">The DLL was loaded.</span></span> <span data-ttu-id="3533e-117">El parámetro *NotificationData* apunta a una estructura de **datos de notificación de LDR \_ dll \_ cargada \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="3533e-117">The *NotificationData* parameter points to an **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <span data-ttu-id="3533e-118"><dt>**LDR \_ Motivo de notificación de DLL \_ \_ \_ descargado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3533e-118"><dt>**LDR\_DLL\_NOTIFICATION\_REASON\_UNLOADED**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="3533e-119">El archivo DLL se ha descargado.</span><span class="sxs-lookup"><span data-stu-id="3533e-119">The DLL was unloaded.</span></span> <span data-ttu-id="3533e-120">El parámetro *NotificationData* apunta a una estructura de datos de **notificación sin \_ cargar del archivo dll \_ \_ \_ LDR** .</span><span class="sxs-lookup"><span data-stu-id="3533e-120">The *NotificationData* parameter points to an **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="3533e-121">*NotificationData* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3533e-121">*NotificationData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3533e-122">Un puntero a una Unión **de \_ \_ notificaciones dll de LDR** de constante que contiene los datos de notificación.</span><span class="sxs-lookup"><span data-stu-id="3533e-122">A pointer to a constant **LDR\_DLL\_NOTIFICATION** union that contains notification data.</span></span> <span data-ttu-id="3533e-123">Esta Unión tiene la siguiente definición:</span><span class="sxs-lookup"><span data-stu-id="3533e-123">This union has the following definition:</span></span>

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

<span data-ttu-id="3533e-124">La estructura de **datos de notificación de LDR \_ dll \_ \_ \_ cargada** tiene la siguiente definición:</span><span class="sxs-lookup"><span data-stu-id="3533e-124">The **LDR\_DLL\_LOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

<span data-ttu-id="3533e-125">La estructura de datos de notificación de la **dll de LDR no \_ \_ cargada \_ \_** tiene la siguiente definición:</span><span class="sxs-lookup"><span data-stu-id="3533e-125">The **LDR\_DLL\_UNLOADED\_NOTIFICATION\_DATA** structure has the following definition:</span></span>

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

<span data-ttu-id="3533e-126">*Contexto* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="3533e-126">*Context* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="3533e-127">Un puntero a los datos de contexto de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="3533e-127">A pointer to context data for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3533e-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3533e-128">Return value</span></span>

<span data-ttu-id="3533e-129">Esta función de devolución de llamada no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="3533e-129">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3533e-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3533e-130">Remarks</span></span>

<span data-ttu-id="3533e-131">Se llama a la función de devolución de llamada de notificación antes de que tenga lugar la vinculación dinámica.</span><span class="sxs-lookup"><span data-stu-id="3533e-131">The notification callback function is called before dynamic linking takes place.</span></span>

## <a name="requirements"></a><span data-ttu-id="3533e-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3533e-132">Requirements</span></span>



| <span data-ttu-id="3533e-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3533e-133">Requirement</span></span> | <span data-ttu-id="3533e-134">Value</span><span class="sxs-lookup"><span data-stu-id="3533e-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3533e-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3533e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="3533e-136">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3533e-136">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3533e-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3533e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="3533e-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3533e-138">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3533e-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="3533e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3533e-140">**LdrRegisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="3533e-140">**LdrRegisterDllNotification**</span></span>](ldrregisterdllnotification.md)
</dt> <dt>

[<span data-ttu-id="3533e-141">**LdrUnregisterDllNotification**</span><span class="sxs-lookup"><span data-stu-id="3533e-141">**LdrUnregisterDllNotification**</span></span>](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




