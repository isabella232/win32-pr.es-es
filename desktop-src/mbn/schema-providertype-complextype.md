---
description: Especifica información acerca de una red de telefonía móvil.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: Tipo complejo de providerType (banda ancha móvil)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666505"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="a3613-103">Tipo complejo de providerType</span><span class="sxs-lookup"><span data-stu-id="a3613-103">providerType Complex Type</span></span>

<span data-ttu-id="a3613-104">El tipo complejo de **providerType** especifica información sobre una red de telefonía móvil.</span><span class="sxs-lookup"><span data-stu-id="a3613-104">The **providerType** complex type specifies information about a cellular network.</span></span>

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a3613-105">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a3613-105">Child elements</span></span>



| <span data-ttu-id="a3613-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="a3613-106">Element</span></span>                                                          | <span data-ttu-id="a3613-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3613-107">Type</span></span>                                                           | <span data-ttu-id="a3613-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3613-108">Description</span></span>               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="a3613-109">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="a3613-109">**ProviderID**</span></span>](schema-providerid-providertype-element.md)     | [<span data-ttu-id="a3613-110">**providerIdType**</span><span class="sxs-lookup"><span data-stu-id="a3613-110">**providerIdType**</span></span>](schema-provideridtype-simpletype.md)     | <span data-ttu-id="a3613-111">IDENTIFICADOR del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a3613-111">Provider ID.</span></span><br/>   |
| [<span data-ttu-id="a3613-112">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="a3613-112">**ProviderName**</span></span>](schema-providername-providertype-element.md) | [<span data-ttu-id="a3613-113">**providerNameType**</span><span class="sxs-lookup"><span data-stu-id="a3613-113">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="a3613-114">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="a3613-114">Provider name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a3613-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3613-115">Requirements</span></span>



| <span data-ttu-id="a3613-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3613-116">Requirement</span></span> | <span data-ttu-id="a3613-117">Value</span><span class="sxs-lookup"><span data-stu-id="a3613-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="a3613-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3613-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a3613-119">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="a3613-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="a3613-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3613-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a3613-121">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a3613-121">None supported</span></span><br/>                         |



 

 




