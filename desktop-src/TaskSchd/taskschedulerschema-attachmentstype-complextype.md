---
title: Tipo complejo de attachmentsType
description: Define los elementos utilizados para especificar los datos adjuntos enviados con un mensaje de correo electrónico.
ms.assetid: b13d9346-a28d-4362-bcfc-dc11869fb8eb
keywords:
- tipo complejo de attachmentsType Programador de tareas
topic_type:
- apiref
api_name:
- attachmentsType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce5bc25b74221112b487be58a729bffa47b8688d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686104"
---
# <a name="attachmentstype-complex-type"></a><span data-ttu-id="ec1a1-104">Tipo complejo de attachmentsType</span><span class="sxs-lookup"><span data-stu-id="ec1a1-104">attachmentsType Complex Type</span></span>

<span data-ttu-id="ec1a1-105">Define los elementos utilizados para especificar los datos adjuntos enviados con un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ec1a1-105">Defines the elements used to specify an attachment sent with an email message.</span></span>

``` syntax
<xs:complexType name="attachmentsType">
    <xs:sequence>
        <xs:element name="File"
            type="nonEmptyString"
            minOccurs="0"
            maxOccurs="8"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="ec1a1-106">Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ec1a1-106">Child elements</span></span>



| <span data-ttu-id="ec1a1-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="ec1a1-107">Element</span></span>                                                          | <span data-ttu-id="ec1a1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec1a1-108">Type</span></span>                                                                    | <span data-ttu-id="ec1a1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec1a1-109">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec1a1-110">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ec1a1-110">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="ec1a1-111">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="ec1a1-111">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="ec1a1-112">Especifica la ruta de acceso a un archivo que se envía como datos adjuntos en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="ec1a1-112">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ec1a1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec1a1-113">Requirements</span></span>



| <span data-ttu-id="ec1a1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec1a1-114">Requirement</span></span> | <span data-ttu-id="ec1a1-115">Value</span><span class="sxs-lookup"><span data-stu-id="ec1a1-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ec1a1-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec1a1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ec1a1-117">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ec1a1-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ec1a1-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ec1a1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ec1a1-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ec1a1-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





