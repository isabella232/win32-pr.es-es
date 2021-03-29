---
description: El motor de configuración de seguridad llama a la función SceSvcAttachmentConfig cuando el sistema está configurado.
ms.assetid: ad20649a-2391-421b-a08c-a4ea6a882abc
title: Función de devolución de llamada SceSvcAttachmentConfig
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentConfig
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: c78caa3b8e08ade9c674a11d113a8b91b8f5fad1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809302"
---
# <a name="scesvcattachmentconfig-callback-function"></a><span data-ttu-id="3f94e-103">Función de devolución de llamada SceSvcAttachmentConfig</span><span class="sxs-lookup"><span data-stu-id="3f94e-103">SceSvcAttachmentConfig callback function</span></span>

<span data-ttu-id="3f94e-104">El motor de configuración de seguridad llama a la función **SceSvcAttachmentConfig** cuando el sistema está configurado.</span><span class="sxs-lookup"><span data-stu-id="3f94e-104">The **SceSvcAttachmentConfig** function is called by the Security Configuration Engine when the system is configured.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f94e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f94e-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentConfig(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3f94e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f94e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f94e-107">*pSceCbInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f94e-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f94e-108">Puntero a una estructura de [**\_ \_ información de devolución de llamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contiene el identificador de base de datos y las funciones de devolución de llamada para consultar, establecer y liberar información.</span><span class="sxs-lookup"><span data-stu-id="3f94e-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure that contains the database handle and the callback functions to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f94e-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f94e-109">Return value</span></span>

<span data-ttu-id="3f94e-110">Si esta función se ejecuta correctamente, devuelve SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3f94e-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="3f94e-111">En caso contrario, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="3f94e-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="3f94e-112">Para obtener más información sobre los códigos de error de configuración de seguridad, vea [valores devueltos de datos adjuntos](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3f94e-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3f94e-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f94e-113">Remarks</span></span>

<span data-ttu-id="3f94e-114">Al implementar esta función, use la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar la información de configuración.</span><span class="sxs-lookup"><span data-stu-id="3f94e-114">When implementing this function, use the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve configuration information.</span></span> <span data-ttu-id="3f94e-115">A continuación, configure el servicio con la información devuelta.</span><span class="sxs-lookup"><span data-stu-id="3f94e-115">Then configure the service using the returned information.</span></span>

<span data-ttu-id="3f94e-116">Esta función debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="3f94e-116">This function must do the following:</span></span>

-   <span data-ttu-id="3f94e-117">Consulte la información de configuración del conjunto de herramientas de configuración de seguridad con la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo).</span><span class="sxs-lookup"><span data-stu-id="3f94e-117">Query configuration information from the Security Configuration tool set using the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo).</span></span>
-   <span data-ttu-id="3f94e-118">Configure el servicio con la información de configuración.</span><span class="sxs-lookup"><span data-stu-id="3f94e-118">Configure the service using the configuration information.</span></span>

<span data-ttu-id="3f94e-119">Para obtener más información, consulte [implementación de SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span><span class="sxs-lookup"><span data-stu-id="3f94e-119">For more information, see [Implementing SceSvcAttachmentConfig](implementing-scesvcattachmentconfig.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="3f94e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f94e-120">Requirements</span></span>



| <span data-ttu-id="3f94e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f94e-121">Requirement</span></span> | <span data-ttu-id="3f94e-122">Value</span><span class="sxs-lookup"><span data-stu-id="3f94e-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3f94e-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f94e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3f94e-124">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="3f94e-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3f94e-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f94e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3f94e-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3f94e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3f94e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f94e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f94e-128">**información de devolución de llamada de SCESVC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3f94e-128">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="3f94e-129">**SceSvcAttachmentAnalyze**</span><span class="sxs-lookup"><span data-stu-id="3f94e-129">**SceSvcAttachmentAnalyze**</span></span>](scesvcattachmentanalyze.md)
</dt> </dl>

 

 




