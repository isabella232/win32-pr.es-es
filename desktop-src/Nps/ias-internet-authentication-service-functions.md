---
title: Funciones de extensiones de NPS
description: Funciones de extensiones de NPS
ms.assetid: ca217314-00f9-4f9d-a9fe-ed928b3c3b3d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a20b424b8ef5109cea7f4d00b97f1a545b89ff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685772"
---
# <a name="nps-extensions-functions"></a><span data-ttu-id="87594-103">Funciones de extensiones de NPS</span><span class="sxs-lookup"><span data-stu-id="87594-103">NPS Extensions Functions</span></span>

> [!Note]  
> <span data-ttu-id="87594-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="87594-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="87594-105">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="87594-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="87594-106">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="87594-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

## <a name="application-defined"></a><span data-ttu-id="87594-107">Aplicación definida</span><span class="sxs-lookup"><span data-stu-id="87594-107">Application Defined</span></span>

<span data-ttu-id="87594-108">La arquitectura de los archivos dll de extensión NPS admite las siguientes funciones exportadas:</span><span class="sxs-lookup"><span data-stu-id="87594-108">The architecture for NPS Extension DLLs supports the following exported functions:</span></span>

-   [<span data-ttu-id="87594-109">**RadiusExtensionFreeAttributes**</span><span class="sxs-lookup"><span data-stu-id="87594-109">**RadiusExtensionFreeAttributes**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes)
-   [<span data-ttu-id="87594-110">**RadiusExtensionInit**</span><span class="sxs-lookup"><span data-stu-id="87594-110">**RadiusExtensionInit**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_init)
-   [<span data-ttu-id="87594-111">**RadiusExtensionProcess**</span><span class="sxs-lookup"><span data-stu-id="87594-111">**RadiusExtensionProcess**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process)
-   [<span data-ttu-id="87594-112">**RadiusExtensionProcessEx**</span><span class="sxs-lookup"><span data-stu-id="87594-112">**RadiusExtensionProcessEx**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)
-   [<span data-ttu-id="87594-113">**RadiusExtensionProcess2**</span><span class="sxs-lookup"><span data-stu-id="87594-113">**RadiusExtensionProcess2**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)
-   [<span data-ttu-id="87594-114">**RadiusExtensionTerm**</span><span class="sxs-lookup"><span data-stu-id="87594-114">**RadiusExtensionTerm**</span></span>](/windows/desktop/api/authif/nc-authif-pradius_extension_term)

<span data-ttu-id="87594-115">Las funciones [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) y [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) son opcionales.</span><span class="sxs-lookup"><span data-stu-id="87594-115">The [**RadiusExtensionInit**](/windows/desktop/api/authif/nc-authif-pradius_extension_init) and [**RadiusExtensionTerm**](/windows/desktop/api/authif/nc-authif-pradius_extension_term) functions are optional.</span></span>

<span data-ttu-id="87594-116">El archivo DLL de extensión puede exportar [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) en lugar de [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) o [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span><span class="sxs-lookup"><span data-stu-id="87594-116">The Extension DLL may export [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2) instead of [**RadiusExtensionProcess**](/windows/desktop/api/authif/nc-authif-pradius_extension_process) or [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex).</span></span>

<span data-ttu-id="87594-117">Si el archivo DLL de extensión exporta [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), también debe exportar [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span><span class="sxs-lookup"><span data-stu-id="87594-117">If the Extension DLL exports [**RadiusExtensionProcessEx**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), then it must also export [**RadiusExtensionFreeAttributes**](/windows/desktop/api/authif/nc-authif-pradius_extension_free_attributes).</span></span>

## <a name="system-defined"></a><span data-ttu-id="87594-118">Definido por el sistema</span><span class="sxs-lookup"><span data-stu-id="87594-118">System Defined</span></span>

<span data-ttu-id="87594-119">Cuando NPS llama a una implementación de [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS pasa la función a un puntero a una estructura de bloque de [**control de \_ extensión \_ \_ RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) .</span><span class="sxs-lookup"><span data-stu-id="87594-119">When NPS calls an implementation of [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), NPS passes the function a pointer to a [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure.</span></span>

<span data-ttu-id="87594-120">La estructura de [**\_ bloque de \_ control \_ de extensión RADIUS**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) contiene punteros de función a las siguientes funciones proporcionadas por NPS:</span><span class="sxs-lookup"><span data-stu-id="87594-120">The [**RADIUS\_EXTENSION\_CONTROL\_BLOCK**](/windows/desktop/api/authif/ns-authif-radius_extension_control_block) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="87594-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87594-121">[**GetRequest**](/previous-versions/ms688263(v=vs.85))</span></span>
-   <span data-ttu-id="87594-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87594-122">[**GetResponse**](/previous-versions/ms688270(v=vs.85))</span></span>
-   <span data-ttu-id="87594-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87594-123">[**SetResponseType**](/previous-versions/ms688462(v=vs.85))</span></span>

<span data-ttu-id="87594-124">Las funciones [**GetRequest**](/previous-versions/ms688263(v=vs.85)) y [**GetResponse**](/previous-versions/ms688270(v=vs.85)) devuelven punteros a una estructura de tipo [**\_ \_ matriz de atributos RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span><span class="sxs-lookup"><span data-stu-id="87594-124">The functions [**GetRequest**](/previous-versions/ms688263(v=vs.85)) and [**GetResponse**](/previous-versions/ms688270(v=vs.85)) return pointers to a structure of type [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array).</span></span>

<span data-ttu-id="87594-125">La estructura de la [**\_ \_ matriz de atributos RADIUS**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) contiene punteros de función a las siguientes funciones proporcionadas por NPS:</span><span class="sxs-lookup"><span data-stu-id="87594-125">The [**RADIUS\_ATTRIBUTE\_ARRAY**](/windows/desktop/api/authif/ns-authif-radius_attribute_array) structure contains function pointers to the following functions provided by NPS:</span></span>

-   <span data-ttu-id="87594-126">[**Agréguela**](/previous-versions/ms688246(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87594-126">[**Add**](/previous-versions/ms688246(v=vs.85))</span></span>
-   <span data-ttu-id="87594-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87594-127">[**AttributeAt**](/previous-versions/ms688253(v=vs.85))</span></span>
-   <span data-ttu-id="87594-128">[**GetSize (**](/previous-versions/ms688277(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87594-128">[**GetSize**](/previous-versions/ms688277(v=vs.85))</span></span>
-   <span data-ttu-id="87594-129">[**Insertat (**](/previous-versions/ms688296(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87594-129">[**InsertAt**](/previous-versions/ms688296(v=vs.85))</span></span>
-   <span data-ttu-id="87594-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87594-130">[**RemoveAt**](/previous-versions/ms688452(v=vs.85))</span></span>
-   <span data-ttu-id="87594-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87594-131">[**SetAt**](/previous-versions/ms688456(v=vs.85))</span></span>

 

 