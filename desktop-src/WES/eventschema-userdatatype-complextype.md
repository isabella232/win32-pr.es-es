---
title: Tipo complejo de UserDataType
description: Define un fragmento XML que especifica el diseño de los datos de evento.
ms.assetid: 25147ace-cc36-43cc-ad85-6a1714f43dbe
keywords:
- UserDataType tipo complejo EventLog
topic_type:
- apiref
api_name:
- UserDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31186fbcc833219b6523f1fdeb986532984eb7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695872"
---
# <a name="userdatatype-complex-type"></a><span data-ttu-id="3ac17-104">Tipo complejo de UserDataType</span><span class="sxs-lookup"><span data-stu-id="3ac17-104">UserDataType Complex Type</span></span>

<span data-ttu-id="3ac17-105">Define un fragmento XML que especifica el diseño de los datos de evento.</span><span class="sxs-lookup"><span data-stu-id="3ac17-105">Defines an XML fragment that specifies the layout of the event data.</span></span>

``` syntax
<xs:complexType name="UserDataType">
    <xs:sequence>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="requirements"></a><span data-ttu-id="3ac17-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ac17-106">Requirements</span></span>



| <span data-ttu-id="3ac17-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ac17-107">Requirement</span></span> | <span data-ttu-id="3ac17-108">Value</span><span class="sxs-lookup"><span data-stu-id="3ac17-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3ac17-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ac17-109">Minimum supported client</span></span><br/> | <span data-ttu-id="3ac17-110">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3ac17-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3ac17-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ac17-111">Minimum supported server</span></span><br/> | <span data-ttu-id="3ac17-112">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ac17-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





