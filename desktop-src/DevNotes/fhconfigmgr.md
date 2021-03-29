---
description: Representa la configuración del historial de archivos del usuario en el que se crea el objeto FhConfigMgr. Todas las operaciones de configuración se realizan mediante una llamada a los métodos de la interfaz IFhConfigMgr.
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: Clase FhConfigMgr (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 083ce344e44035b5872d91ad14465659defc8229
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907204"
---
# <a name="fhconfigmgr-class"></a><span data-ttu-id="9b996-104">Clase FhConfigMgr</span><span class="sxs-lookup"><span data-stu-id="9b996-104">FhConfigMgr class</span></span>

<span data-ttu-id="9b996-105">Representa la configuración del historial de archivos del usuario en el que se crea el objeto **FhConfigMgr** .</span><span class="sxs-lookup"><span data-stu-id="9b996-105">Represents the File History configuration of the user under which the **FhConfigMgr** object is created.</span></span> <span data-ttu-id="9b996-106">Todas las operaciones de configuración se realizan mediante una llamada a los métodos de la interfaz [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) .</span><span class="sxs-lookup"><span data-stu-id="9b996-106">All configuration operations are performed by calling the methods of the [**IFhConfigMgr**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) interface.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="9b996-107">Cuándo implementar</span><span class="sxs-lookup"><span data-stu-id="9b996-107">When to implement</span></span>

<span data-ttu-id="9b996-108">La API del historial de archivos implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9b996-108">The File History API implements this class.</span></span> <span data-ttu-id="9b996-109">Para crear una instancia de esta clase, use la función [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .</span><span class="sxs-lookup"><span data-stu-id="9b996-109">To create an instance of this class, use the [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b996-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b996-110">Requirements</span></span>



| <span data-ttu-id="9b996-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b996-111">Requirement</span></span> | <span data-ttu-id="9b996-112">Value</span><span class="sxs-lookup"><span data-stu-id="9b996-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9b996-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b996-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9b996-114">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b996-114">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9b996-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b996-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9b996-116">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b996-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9b996-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b996-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b996-118"><dt>Fhcfg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b996-118"><dt>Fhcfg.h</dt></span></span> </dl>   |
| <span data-ttu-id="9b996-119">IDL</span><span class="sxs-lookup"><span data-stu-id="9b996-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9b996-120"><dt>Fhcfg. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9b996-120"><dt>Fhcfg.idl</dt></span></span> </dl> |



 

 
