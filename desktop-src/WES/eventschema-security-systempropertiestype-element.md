---
title: Elemento Security (SystemPropertiesType)
description: Identifica el usuario que registró el evento.
ms.assetid: f421b0c3-96ea-440c-a3b2-0ddd8f327eec
keywords:
- Elemento de seguridad EventLog
topic_type:
- apiref
api_name:
- Security
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b793193d7afdfde5fd515252a024432ed45ff8b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150991"
---
# <a name="security-systempropertiestype-element"></a><span data-ttu-id="3462e-104">Elemento Security (SystemPropertiesType)</span><span class="sxs-lookup"><span data-stu-id="3462e-104">Security (SystemPropertiesType) Element</span></span>

<span data-ttu-id="3462e-105">Identifica el usuario que registró el evento.</span><span class="sxs-lookup"><span data-stu-id="3462e-105">Identifies the user that logged the event.</span></span>

``` syntax
<xs:element name="Security">
    <xs:complexType>
        <xs:attribute name="UserID"
            type="string"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="3462e-106">El elemento de **seguridad** se define mediante el tipo complejo de [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3462e-106">The **Security** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="3462e-107">Atributos</span><span class="sxs-lookup"><span data-stu-id="3462e-107">Attributes</span></span>



| <span data-ttu-id="3462e-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="3462e-108">Name</span></span>   | <span data-ttu-id="3462e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="3462e-109">Type</span></span>   | <span data-ttu-id="3462e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="3462e-110">Description</span></span>                                                          |
|--------|--------|----------------------------------------------------------------------|
| <span data-ttu-id="3462e-111">UserID</span><span class="sxs-lookup"><span data-stu-id="3462e-111">UserID</span></span> | <span data-ttu-id="3462e-112">string</span><span class="sxs-lookup"><span data-stu-id="3462e-112">string</span></span> | <span data-ttu-id="3462e-113">El identificador de seguridad (SID) del usuario en forma de cadena.</span><span class="sxs-lookup"><span data-stu-id="3462e-113">The security identifier (SID) of the user in string form.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="3462e-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3462e-114">Requirements</span></span>



| <span data-ttu-id="3462e-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3462e-115">Requirement</span></span> | <span data-ttu-id="3462e-116">Value</span><span class="sxs-lookup"><span data-stu-id="3462e-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3462e-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3462e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3462e-118">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3462e-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3462e-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3462e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3462e-120">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3462e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3462e-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3462e-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="3462e-122">**Elemento primario**</span><span class="sxs-lookup"><span data-stu-id="3462e-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="3462e-123">**Sistema (EventType)**</span><span class="sxs-lookup"><span data-stu-id="3462e-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





