---
title: Tipo complejo de headerFieldsType
description: Define los elementos que especifican los campos de un encabezado de correo electrónico.
ms.assetid: 1ad1b62d-5aca-4be4-b956-6f8c64761b2b
keywords:
- tipo complejo de headerFieldsType Programador de tareas
topic_type:
- apiref
api_name:
- headerFieldsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edb783972217d0455eb2ee25fed31cf20e5b774b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489856"
---
# <a name="headerfieldstype-complex-type"></a><span data-ttu-id="cb7ef-104">Tipo complejo de headerFieldsType</span><span class="sxs-lookup"><span data-stu-id="cb7ef-104">headerFieldsType Complex Type</span></span>

<span data-ttu-id="cb7ef-105">Define los elementos que especifican los campos de un encabezado de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cb7ef-105">Defines the elements that specify the fields for an email header.</span></span>

``` syntax
<xs:complexType name="headerFieldsType">
    <xs:sequence>
        <xs:element name="HeaderField"
            type="headerFieldType"
            minOccurs="0"
            maxOccurs="32"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="cb7ef-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="cb7ef-106">Child elements</span></span>



| <span data-ttu-id="cb7ef-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="cb7ef-107">Element</span></span>                                                                         | <span data-ttu-id="cb7ef-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb7ef-108">Type</span></span>                                                                       | <span data-ttu-id="cb7ef-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb7ef-109">Description</span></span>                                       |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="cb7ef-110">**HeaderField**</span><span class="sxs-lookup"><span data-stu-id="cb7ef-110">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="cb7ef-111">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="cb7ef-111">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="cb7ef-112">Especifica un campo en un encabezado de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="cb7ef-112">Specifies a field in an email header.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="cb7ef-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb7ef-113">Requirements</span></span>



| <span data-ttu-id="cb7ef-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb7ef-114">Requirement</span></span> | <span data-ttu-id="cb7ef-115">Value</span><span class="sxs-lookup"><span data-stu-id="cb7ef-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb7ef-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb7ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cb7ef-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cb7ef-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cb7ef-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cb7ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cb7ef-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="cb7ef-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





