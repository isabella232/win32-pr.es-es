---
title: Elemento File (attachmentsType)
description: Contiene la ruta de acceso a un archivo que se envía como datos adjuntos en un mensaje de correo electrónico.
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- Programador de tareas de elemento de archivo
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422165"
---
# <a name="file-attachmentstype-element"></a><span data-ttu-id="17c7a-104">Elemento File (attachmentsType)</span><span class="sxs-lookup"><span data-stu-id="17c7a-104">File (attachmentsType) Element</span></span>

<span data-ttu-id="17c7a-105">Contiene la ruta de acceso a un archivo que se envía como datos adjuntos en un mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="17c7a-105">Contains the path to a file sent as an attachment in an email message.</span></span>

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

<span data-ttu-id="17c7a-106">El elemento de **archivo** se define mediante el tipo complejo de [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="17c7a-106">The **File** element is defined by the [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="17c7a-107">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="17c7a-107">Parent element</span></span>



| <span data-ttu-id="17c7a-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="17c7a-108">Element</span></span>                                                                                      | <span data-ttu-id="17c7a-109">Derivado de</span><span class="sxs-lookup"><span data-stu-id="17c7a-109">Derived from</span></span>                                                               | <span data-ttu-id="17c7a-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="17c7a-110">Description</span></span>                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="17c7a-111">**Datos adjuntos (sendEmailType)**</span><span class="sxs-lookup"><span data-stu-id="17c7a-111">**Attachments (sendEmailType)**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md) | [<span data-ttu-id="17c7a-112">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="17c7a-112">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md) | <span data-ttu-id="17c7a-113">Contiene una lista de datos adjuntos en el mensaje de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="17c7a-113">Contains a list of attachments in the email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="17c7a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17c7a-114">Remarks</span></span>

<span data-ttu-id="17c7a-115">Para el desarrollo de C++, vea la [**propiedad Attachments de IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span><span class="sxs-lookup"><span data-stu-id="17c7a-115">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="17c7a-116">Para el desarrollo de scripts, vea [**EmailAction. Attachments**](emailaction-attachments.md).</span><span class="sxs-lookup"><span data-stu-id="17c7a-116">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17c7a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17c7a-117">Requirements</span></span>



| <span data-ttu-id="17c7a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c7a-118">Requirement</span></span> | <span data-ttu-id="17c7a-119">Value</span><span class="sxs-lookup"><span data-stu-id="17c7a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="17c7a-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17c7a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="17c7a-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="17c7a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="17c7a-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17c7a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="17c7a-123">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="17c7a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





