---
title: Constantes de HTTP_RESPONSE_FLAG_ (http. h)
description: Defina las opciones para configurar las respuestas en la API del servidor HTTP.
ms.assetid: bcb59457-fd22-4166-8a72-ba85209ec8c7
topic_type:
- apiref
api_name:
- HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE
api_location:
- http.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96b7c34d453c1b9bbe45cf2c85ad268b414f3439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665959"
---
# <a name="http_response_flag_-constants"></a><span data-ttu-id="152c6-103">Constantes de la \_ marca de respuesta HTTP \_ \_</span><span class="sxs-lookup"><span data-stu-id="152c6-103">HTTP\_RESPONSE\_FLAG\_ Constants</span></span>

<span data-ttu-id="152c6-104">Las constantes de la **\_ \_ \_ marca de respuesta http** definen las opciones para configurar las respuestas en la API del servidor http.</span><span class="sxs-lookup"><span data-stu-id="152c6-104">The **HTTP\_RESPONSE\_FLAG\_** constants define options to configure responses in the HTTP Server API.</span></span>

<span data-ttu-id="152c6-105">Estas constantes se utilizan en el miembro **Flags** de la estructura [**http \_ Response \_ v1**](/windows/desktop/api/Http/ns-http-http_response_v1) .</span><span class="sxs-lookup"><span data-stu-id="152c6-105">These constants are used in the **Flags** member of the [**HTTP\_RESPONSE\_V1**](/windows/desktop/api/Http/ns-http-http_response_v1) structure.</span></span>

<dl> <dt>

<span data-ttu-id="152c6-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**\_marca de respuesta HTTP \_ \_ varias \_ codificaciones \_ disponibles**</span><span class="sxs-lookup"><span data-stu-id="152c6-106"><span id="HTTP_RESPONSE_FLAG_MULTIPLE_ENCODINGS_AVAILABLE"></span><span id="http_response_flag_multiple_encodings_available"></span>**HTTP\_RESPONSE\_FLAG\_MULTIPLE\_ENCODINGS\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="152c6-107">Las codificaciones que no sean el formulario de identidad están disponibles para este recurso.</span><span class="sxs-lookup"><span data-stu-id="152c6-107">Encodings other than identity form are available for this resource.</span></span> <span data-ttu-id="152c6-108">Esta marca se omite si la aplicación no ha solicitado que se almacene en caché la respuesta.</span><span class="sxs-lookup"><span data-stu-id="152c6-108">This flag is ignored if the application has not asked for the response to be cached.</span></span> <span data-ttu-id="152c6-109">Se usa como una sugerencia a la API del servidor HTTP para la negociación de contenido cuando atiende desde la caché de respuesta del kernel.</span><span class="sxs-lookup"><span data-stu-id="152c6-109">It's used as a hint to the HTTP Server API for content negotiation when serving from the kernel response cache.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="152c6-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="152c6-110">Requirements</span></span>



| <span data-ttu-id="152c6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="152c6-111">Requirement</span></span> | <span data-ttu-id="152c6-112">Value</span><span class="sxs-lookup"><span data-stu-id="152c6-112">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="152c6-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="152c6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="152c6-114">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="152c6-114">Windows 7 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="152c6-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="152c6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="152c6-116">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="152c6-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="152c6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="152c6-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="152c6-118"><dt>Http. h</dt></span><span class="sxs-lookup"><span data-stu-id="152c6-118"><dt>Http.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="152c6-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="152c6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="152c6-120">API del servidor HTTP versión 2,0 constantes</span><span class="sxs-lookup"><span data-stu-id="152c6-120">HTTP Server API Version 2.0 Constants</span></span>](http-server-api-version-2-0-constants.md)
</dt> <dt>

[<span data-ttu-id="152c6-121">**\_Respuesta HTTP \_ v1**</span><span class="sxs-lookup"><span data-stu-id="152c6-121">**HTTP\_RESPONSE\_V1**</span></span>](/windows/desktop/api/Http/ns-http-http_response_v1)
</dt> </dl>

 

 





