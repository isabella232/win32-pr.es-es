---
description: Los complementos de configuración de seguridad llaman a la función SceSvcAttachmentUpdate para pasar los cambios de configuración a la base de datos de seguridad.
ms.assetid: 2b5b3718-8ccb-480a-97fb-c8115d8f3a5c
title: Función de devolución de llamada SceSvcAttachmentUpdate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentUpdate
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 5bc4c9426f6a085c72f2fc3d872de4d7da59156b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809301"
---
# <a name="scesvcattachmentupdate-callback-function"></a><span data-ttu-id="916d6-103">Función de devolución de llamada SceSvcAttachmentUpdate</span><span class="sxs-lookup"><span data-stu-id="916d6-103">SceSvcAttachmentUpdate callback function</span></span>

<span data-ttu-id="916d6-104">Los complementos de configuración de seguridad llaman a la función **SceSvcAttachmentUpdate** para pasar los cambios de configuración a la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="916d6-104">The **SceSvcAttachmentUpdate** function is called by the Security Configuration snap-ins to pass configuration changes to the security database.</span></span>

## <a name="syntax"></a><span data-ttu-id="916d6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="916d6-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentUpdate(
  _In_ PSCESVC_CALLBACK_INFO     pSceCbInfo,
  _In_ SCESVC_CONFIGURATION_INFO *ServiceInfo
);
```



## <a name="parameters"></a><span data-ttu-id="916d6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="916d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="916d6-107">*pSceCbInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="916d6-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="916d6-108">Puntero a una estructura de [**\_ \_ información de devolución de llamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contiene el identificador de devolución de llamada y los punteros de función a SCE.</span><span class="sxs-lookup"><span data-stu-id="916d6-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains the callback handle and function pointers to SCE.</span></span>

</dd> <dt>

<span data-ttu-id="916d6-109">*ServiceInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="916d6-109">*ServiceInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="916d6-110">Información de configuración actualizada.</span><span class="sxs-lookup"><span data-stu-id="916d6-110">Updated configuration information.</span></span> <span data-ttu-id="916d6-111">La estructura de datos usada para esta información [**es \_ \_ información de configuración de SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span><span class="sxs-lookup"><span data-stu-id="916d6-111">The data structure used for this information is [**SCESVC\_CONFIGURATION\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="916d6-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="916d6-112">Return value</span></span>

<span data-ttu-id="916d6-113">Si esta función se ejecuta correctamente, devuelve SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="916d6-113">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="916d6-114">En caso contrario, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="916d6-114">Otherwise it returns an error code.</span></span> <span data-ttu-id="916d6-115">Para obtener más información sobre los códigos de error de configuración de seguridad, vea [valores devueltos de datos adjuntos](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="916d6-115">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="916d6-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="916d6-116">Remarks</span></span>

<span data-ttu-id="916d6-117">La función **SceSvcAttachmentUpdate** debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="916d6-117">The **SceSvcAttachmentUpdate** function must do the following:</span></span>

-   <span data-ttu-id="916d6-118">Llame a la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar la información de configuración base actual de la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="916d6-118">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the current base configuration information from the security database.</span></span>
-   <span data-ttu-id="916d6-119">Llame a la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar el último conjunto de diferencias (información de análisis) de la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="916d6-119">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve the last set of differences (analysis information) from the security database.</span></span>
-   <span data-ttu-id="916d6-120">Utilice la información de servicio suministrada (vea *ServiceInfo*) para calcular la nueva configuración base.</span><span class="sxs-lookup"><span data-stu-id="916d6-120">Use the supplied service information (see *ServiceInfo*) to compute the new base configuration.</span></span>
-   <span data-ttu-id="916d6-121">Utilice la información de servicio suministrada (vea *ServiceInfo*) y el análisis para calcular la nueva información de diferencia.</span><span class="sxs-lookup"><span data-stu-id="916d6-121">Use the supplied service information (see *ServiceInfo*) and the analysis to compute the new difference information.</span></span>
-   <span data-ttu-id="916d6-122">Llame a la función de devolución de llamada a la que apunta el miembro **pfSetInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para establecer la nueva configuración base en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="916d6-122">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo)to set the new base configuration in the security database.</span></span>
-   <span data-ttu-id="916d6-123">Llame a la función de devolución de llamada a la que apunta el miembro **pfSetInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para establecer la nueva información de análisis en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="916d6-123">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to set the new analysis information in the security database.</span></span>

<span data-ttu-id="916d6-124">Para obtener más información, consulte [implementación de SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span><span class="sxs-lookup"><span data-stu-id="916d6-124">For more information, see [Implementing SceSvcAttachmentUpdate](implementing-scesvcattachmentupdate.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="916d6-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="916d6-125">Requirements</span></span>



| <span data-ttu-id="916d6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="916d6-126">Requirement</span></span> | <span data-ttu-id="916d6-127">Value</span><span class="sxs-lookup"><span data-stu-id="916d6-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="916d6-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="916d6-128">Minimum supported client</span></span><br/> | <span data-ttu-id="916d6-129">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="916d6-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="916d6-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="916d6-130">Minimum supported server</span></span><br/> | <span data-ttu-id="916d6-131">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="916d6-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="916d6-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="916d6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="916d6-133">**información de devolución de llamada de SCESVC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="916d6-133">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="916d6-134">**\_información de configuración de SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="916d6-134">**SCESVC\_CONFIGURATION\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_configuration_info)
</dt> </dl>

 

 




