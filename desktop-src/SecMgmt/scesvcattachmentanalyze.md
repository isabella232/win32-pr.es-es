---
description: El motor de configuración de seguridad llama a la función SceSvcAttachmentAnalyze cuando se analiza el sistema.
ms.assetid: 8e8a39b9-c4e2-446e-8e0c-eb2113234c1a
title: Función de devolución de llamada SceSvcAttachmentAnalyze
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SceSvcAttachmentAnalyze
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 296d755a0b082b46122432936d30614019b8b9a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809307"
---
# <a name="scesvcattachmentanalyze-callback-function"></a><span data-ttu-id="5be44-103">Función de devolución de llamada SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="5be44-103">SceSvcAttachmentAnalyze callback function</span></span>

<span data-ttu-id="5be44-104">El motor de configuración de seguridad llama a la función **SceSvcAttachmentAnalyze** cuando se analiza el sistema.</span><span class="sxs-lookup"><span data-stu-id="5be44-104">The **SceSvcAttachmentAnalyze** function is called by the Security Configuration Engine when the system is analyzed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5be44-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5be44-105">Syntax</span></span>


```C++
SCESTATUS WINAPI SceSvcAttachmentAnalyze(
  _In_ PSCESVC_CALLBACK_INFO pSceCbInfo
);
```



## <a name="parameters"></a><span data-ttu-id="5be44-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5be44-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5be44-107">*pSceCbInfo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5be44-107">*pSceCbInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5be44-108">Puntero a una estructura de [**\_ \_ información de devolución de llamada SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) que contiene un identificador de base de datos opaco y punteros de función de devolución de llamada para consultar, establecer y liberar información.</span><span class="sxs-lookup"><span data-stu-id="5be44-108">Pointer to a [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure which contains an opaque database handle and callback function pointers to query, set, and free information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5be44-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5be44-109">Return value</span></span>

<span data-ttu-id="5be44-110">Si esta función se ejecuta correctamente, devuelve SCESTATUS \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5be44-110">If this function succeeds, it returns SCESTATUS\_SUCCESS.</span></span> <span data-ttu-id="5be44-111">En caso contrario, devuelve un código de error.</span><span class="sxs-lookup"><span data-stu-id="5be44-111">Otherwise it returns an error code.</span></span> <span data-ttu-id="5be44-112">Para obtener más información sobre los códigos de error de configuración de seguridad, vea [valores devueltos de datos adjuntos](management-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5be44-112">For more information about the Security Configuration error codes, see [Attachment Return Values](management-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="5be44-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5be44-113">Remarks</span></span>

<span data-ttu-id="5be44-114">La función **SceSvcAttachmentAnalyze** debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5be44-114">The **SceSvcAttachmentAnalyze** function must do the following:</span></span>

-   <span data-ttu-id="5be44-115">Consulte directamente la información de configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="5be44-115">Directly query configuration information from the service.</span></span>
-   <span data-ttu-id="5be44-116">Llame a la función de devolución de llamada a la que apunta el miembro **pfQueryInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfQueryInfo) para recuperar información de la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5be44-116">Call the callback function pointed to by the **pfQueryInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfQueryInfo) to retrieve information from the security database.</span></span>
-   <span data-ttu-id="5be44-117">Calcular las diferencias entre la información basada en el tipo y la sintaxis.</span><span class="sxs-lookup"><span data-stu-id="5be44-117">Compute the differences between the information based on type and syntax.</span></span>
-   <span data-ttu-id="5be44-118">Llame a la función de devolución de llamada a la que apunta el miembro **pfSetInfo** de la estructura de [**información de devolución de \_ llamada \_ SCESVC**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) (pSceCbInfo->pfSetInfo) para actualizar la base de datos de seguridad con la información de servicio recuperada que sea diferente.</span><span class="sxs-lookup"><span data-stu-id="5be44-118">Call the callback function pointed to by the **pfSetInfo** member of the [**SCESVC\_CALLBACK\_INFO**](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info) structure (pSceCbInfo->pfSetInfo) to update the security database with the retrieved service information that is different.</span></span>

<span data-ttu-id="5be44-119">Para obtener más información, consulte [implementación de SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span><span class="sxs-lookup"><span data-stu-id="5be44-119">For more information, see [Implementing SceSvcAttachmentAnalyze](implementing-scesvcattachmentanalyze.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5be44-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5be44-120">Requirements</span></span>



| <span data-ttu-id="5be44-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5be44-121">Requirement</span></span> | <span data-ttu-id="5be44-122">Value</span><span class="sxs-lookup"><span data-stu-id="5be44-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5be44-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5be44-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5be44-124">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="5be44-124">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5be44-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5be44-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5be44-126">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5be44-126">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5be44-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="5be44-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5be44-128">Implementación de SceSvcAttachmentAnalyze</span><span class="sxs-lookup"><span data-stu-id="5be44-128">Implementing SceSvcAttachmentAnalyze</span></span>](implementing-scesvcattachmentanalyze.md)
</dt> <dt>

[<span data-ttu-id="5be44-129">**información de devolución de llamada de SCESVC \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5be44-129">**SCESVC\_CALLBACK\_INFO**</span></span>](/windows/win32/api/scesvc/ns-scesvc-scesvc_callback_info)
</dt> <dt>

[<span data-ttu-id="5be44-130">**SceSvcAttachmentConfig**</span><span class="sxs-lookup"><span data-stu-id="5be44-130">**SceSvcAttachmentConfig**</span></span>](scesvcattachmentconfig.md)
</dt> </dl>

 

 




