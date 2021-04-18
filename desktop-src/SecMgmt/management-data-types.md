---
description: Enumera los tipos de datos utilizados por los archivos dll de datos adjuntos de configuración de seguridad y sus funciones auxiliares.
ms.assetid: 1d3bdf0d-320c-4b25-9e9b-fda134876979
title: Tipos de datos de administración de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae7efedb32ab545b903c61819042e32b7d83dbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667526"
---
# <a name="security-management-data-types"></a><span data-ttu-id="5c49c-103">Tipos de datos de administración de seguridad</span><span class="sxs-lookup"><span data-stu-id="5c49c-103">Security Management Data Types</span></span>

<span data-ttu-id="5c49c-104">Entre los tipos de datos de administración de seguridad se incluyen los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5c49c-104">The security management data types include the following:</span></span>

-   [<span data-ttu-id="5c49c-105">Tipos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5c49c-105">Attachment Data Types</span></span>](#attachment-data-types)
-   [<span data-ttu-id="5c49c-106">Tipos de datos de directiva de LSA</span><span class="sxs-lookup"><span data-stu-id="5c49c-106">LSA Policy Data Types</span></span>](#lsa-policy-data-types)

## <a name="attachment-data-types"></a><span data-ttu-id="5c49c-107">Tipos de datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="5c49c-107">Attachment Data Types</span></span>

<span data-ttu-id="5c49c-108">Los archivos dll de datos adjuntos de configuración de seguridad usan los siguientes tipos de datos y sus funciones auxiliares.</span><span class="sxs-lookup"><span data-stu-id="5c49c-108">The following data types are used by the Security Configuration attachment DLLs and their supporting functions.</span></span>



| <span data-ttu-id="5c49c-109">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5c49c-109">Data type</span></span>                                                    | <span data-ttu-id="5c49c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c49c-110">Description</span></span>                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c49c-111">**\_contexto de enumeración de SCE \_**</span><span class="sxs-lookup"><span data-stu-id="5c49c-111">**SCE\_ENUMERATION\_CONTEXT**</span></span>](sce-enumeration-context.md) | <span data-ttu-id="5c49c-112">Lo utiliza la función de [**\_ \_ información de consulta PFSCE**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) para navegar por la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5c49c-112">Used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>                                                                                                                                              |
| [<span data-ttu-id="5c49c-113">**identificador de SCE \_**</span><span class="sxs-lookup"><span data-stu-id="5c49c-113">**SCE\_HANDLE**</span></span>](sce-handle.md)                            | <span data-ttu-id="5c49c-114">Usado por [**PFSCE \_ query \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) y [**PFSCE \_ set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) para pasar información entre los datos adjuntos y la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="5c49c-114">Used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to pass information between the attachment and the security database.</span></span>                                                                                 |
| [<span data-ttu-id="5c49c-115">**SCESTATUS**</span><span class="sxs-lookup"><span data-stu-id="5c49c-115">**SCESTATUS**</span></span>](scestatus.md)                               | <span data-ttu-id="5c49c-116">El tipo de datos lo usa la API del conjunto de herramientas de configuración de seguridad para devolver información sobre los resultados de una llamada de función.</span><span class="sxs-lookup"><span data-stu-id="5c49c-116">Data type is used by the Security Configuration tool set API to return information about the results of a function call.</span></span>                                                                                                                                    |
| [<span data-ttu-id="5c49c-117">**identificador de SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="5c49c-117">**SCESVC\_HANDLE**</span></span>](scesvc-handle.md)                      | <span data-ttu-id="5c49c-118">Lo usan los métodos de las interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) y [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) para pasar información entre el complemento configuración de seguridad y la extensión del complemento.</span><span class="sxs-lookup"><span data-stu-id="5c49c-118">Used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span> |
| [<span data-ttu-id="5c49c-119">**\_tipo de información de SCESVC \_**</span><span class="sxs-lookup"><span data-stu-id="5c49c-119">**SCESVC\_INFO\_TYPE**</span></span>](/windows/desktop/api/Scesvc/ne-scesvc-scesvc_info_type)               | <span data-ttu-id="5c49c-120">La información de [**consulta de \_ PFSCE \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) y la información de conjunto de PFSCE utilizan la enumeración para indicar el tipo de información que se solicita o se pasa a la base de datos de seguridad. [**\_ \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)</span><span class="sxs-lookup"><span data-stu-id="5c49c-120">Enumeration is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) to indicate the type of information requested from or passed to the security database.</span></span>                                                 |



 

## <a name="lsa-policy-data-types"></a><span data-ttu-id="5c49c-121">Tipos de datos de directiva de LSA</span><span class="sxs-lookup"><span data-stu-id="5c49c-121">LSA Policy Data Types</span></span>

<span data-ttu-id="5c49c-122">Las funciones de administración de directivas de LSA usan los siguientes tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="5c49c-122">The following data types are used by the LSA policy management functions.</span></span>



| <span data-ttu-id="5c49c-123">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5c49c-123">Data type</span></span>                                                  | <span data-ttu-id="5c49c-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c49c-124">Description</span></span>                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="5c49c-125">**\_identificador de enumeración de LSA \_**</span><span class="sxs-lookup"><span data-stu-id="5c49c-125">**LSA\_ENUMERATION\_HANDLE**</span></span>](lsa-enumeration-handle.md) | <span data-ttu-id="5c49c-126">Se utiliza para realizar el seguimiento de las enumeraciones en las que se requieren varias llamadas a funciones.</span><span class="sxs-lookup"><span data-stu-id="5c49c-126">Used to track enumerations in which multiple function calls are required.</span></span> |
| [<span data-ttu-id="5c49c-127">**identificador de LSA \_**</span><span class="sxs-lookup"><span data-stu-id="5c49c-127">**LSA\_HANDLE**</span></span>](lsa-handle.md)                          | <span data-ttu-id="5c49c-128">Identificador de un objeto de [**Directiva**](policy-object.md) .</span><span class="sxs-lookup"><span data-stu-id="5c49c-128">Handle to a [**Policy**](policy-object.md) object.</span></span>                       |



 

 

 
