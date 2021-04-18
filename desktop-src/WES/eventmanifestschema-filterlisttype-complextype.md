---
title: Tipo complejo de FilterListType
description: Define una lista de filtros que un controlador ETW puede pasar al proveedor para limitar aún más los eventos que escribe.
ms.assetid: 27f7b150-1264-4a12-858e-b0b0dff5baa7
keywords:
- FilterListType tipo complejo EventLog
topic_type:
- apiref
api_name:
- FilterListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d1071fbbb9eba6bf6ebf0d74d4caaac50e1ccce4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359841"
---
# <a name="filterlisttype-complex-type"></a><span data-ttu-id="5efce-104">Tipo complejo de FilterListType</span><span class="sxs-lookup"><span data-stu-id="5efce-104">FilterListType Complex Type</span></span>

<span data-ttu-id="5efce-105">Define una lista de filtros que un controlador ETW puede pasar al proveedor para limitar aún más los eventos que escribe.</span><span class="sxs-lookup"><span data-stu-id="5efce-105">Defines a list of filters that an ETW controller can pass to your provider to further limit the events that it writes.</span></span>

``` syntax
<xs:complexType name="FilterListType">
    <xs:sequence>
        <xs:element name="filter"
            type="FilterType"
            minOccurs="0"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5efce-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="5efce-106">Child elements</span></span>



| <span data-ttu-id="5efce-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="5efce-107">Element</span></span>    | <span data-ttu-id="5efce-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="5efce-108">Type</span></span>                                                             | <span data-ttu-id="5efce-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="5efce-109">Description</span></span>                   |
|------------|------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="5efce-110">**filter**</span><span class="sxs-lookup"><span data-stu-id="5efce-110">**filter**</span></span> | [<span data-ttu-id="5efce-111">**FilterType**</span><span class="sxs-lookup"><span data-stu-id="5efce-111">**FilterType**</span></span>](eventmanifestschema-filtertype-complextype.md) | <span data-ttu-id="5efce-112">Una lista de filtros.</span><span class="sxs-lookup"><span data-stu-id="5efce-112">A list of filters.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5efce-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5efce-113">Remarks</span></span>

<span data-ttu-id="5efce-114">Un controlador ETW es una aplicación que llama a la función [**StartTrace**](/windows/desktop/ETW/starttrace) para crear una sesión de ETW.</span><span class="sxs-lookup"><span data-stu-id="5efce-114">An ETW controller is an application that calls the [**StartTrace**](/windows/desktop/ETW/starttrace) function to create an ETW session.</span></span> <span data-ttu-id="5efce-115">Para obtener más información, vea [controlar las sesiones de seguimiento de eventos](/windows/desktop/ETW/controlling-event-tracing-sessions).</span><span class="sxs-lookup"><span data-stu-id="5efce-115">For details, see [Controlling Event Tracing Sessions](/windows/desktop/ETW/controlling-event-tracing-sessions).</span></span> <span data-ttu-id="5efce-116">El controlador puede usar la función [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) para enumerar los filtros que se definen.</span><span class="sxs-lookup"><span data-stu-id="5efce-116">The controller can use the [**TdhEnumerateProviderFilters**](/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters) function to enumerate the filters that you define.</span></span> <span data-ttu-id="5efce-117">Después, el controlador puede pasar uno o varios filtros cuando llama a la función [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) para habilitar el proveedor.</span><span class="sxs-lookup"><span data-stu-id="5efce-117">The controller can then pass one or more of the filters when it calls the [**EnableTraceEx2**](/windows/desktop/ETW/enabletraceex2) function to enable your provider.</span></span> <span data-ttu-id="5efce-118">El proveedor recibe los filtros, junto con el resto de los parámetros de habilitación, en la función de devolución de llamada [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) .</span><span class="sxs-lookup"><span data-stu-id="5efce-118">Your provider receives the filters, along with the rest of the enable parameters, in your [*EnableCallback*](/windows/desktop/api/evntprov/nc-evntprov-penablecallback) callback function.</span></span>

## <a name="requirements"></a><span data-ttu-id="5efce-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5efce-119">Requirements</span></span>



| <span data-ttu-id="5efce-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5efce-120">Requirement</span></span> | <span data-ttu-id="5efce-121">Value</span><span class="sxs-lookup"><span data-stu-id="5efce-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5efce-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5efce-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5efce-123">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5efce-123">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5efce-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5efce-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5efce-125">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5efce-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

