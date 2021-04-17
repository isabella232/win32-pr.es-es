---
description: Establece o recupera el nombre de CAPICOM del atributo. Esta es la propiedad predeterminada.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Propiedad Attribute.Name
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670451"
---
# <a name="attributename-property"></a><span data-ttu-id="7b244-104">Propiedad Attribute.Name</span><span class="sxs-lookup"><span data-stu-id="7b244-104">Attribute.Name property</span></span>

<span data-ttu-id="7b244-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="7b244-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="7b244-106">En su lugar, use la [**clase CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="7b244-106">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="7b244-107">La propiedad **Name** establece o recupera el nombre de CAPICOM del atributo.</span><span class="sxs-lookup"><span data-stu-id="7b244-107">The **Name** property sets or retrieves the CAPICOM name of the attribute.</span></span> <span data-ttu-id="7b244-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="7b244-108">This is the default property.</span></span>

<span data-ttu-id="7b244-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="7b244-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b244-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7b244-110">Syntax</span></span>


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a><span data-ttu-id="7b244-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="7b244-111">Property value</span></span>

<span data-ttu-id="7b244-112">Un valor de la enumeración de [**\_ atributos de CAPICOM**](capicom-attribute.md) que especifica el nombre de CAPICOM del atributo.</span><span class="sxs-lookup"><span data-stu-id="7b244-112">A value of the [**CAPICOM\_ATTRIBUTE**](capicom-attribute.md) enumeration that specifies the CAPICOM name of the attribute.</span></span> <span data-ttu-id="7b244-113">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="7b244-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="7b244-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7b244-114">Value</span></span>                                                                                                                                                                                                                                                                                 | <span data-ttu-id="7b244-115">Significado</span><span class="sxs-lookup"><span data-stu-id="7b244-115">Meaning</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <span data-ttu-id="7b244-116"><dt>**\_tiempo de firma de atributo autenticado de CAPICOM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7b244-116"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME**</dt></span></span> </dl>                         | <span data-ttu-id="7b244-117">El atributo contiene la hora a la que se creó la firma.</span><span class="sxs-lookup"><span data-stu-id="7b244-117">The attribute contains the time that the signature was created.</span></span><br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <span data-ttu-id="7b244-118"><dt>**\_nombre de documento de atributo autenticado de CAPICOM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7b244-118"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_NAME**</dt></span></span> </dl>                      | <span data-ttu-id="7b244-119">El atributo contiene el nombre del documento firmado.</span><span class="sxs-lookup"><span data-stu-id="7b244-119">The attribute contains the name of the signed document.</span></span><br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <span data-ttu-id="7b244-120"><dt>**\_Descripción del documento de atributo autenticado de CAPICOM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7b244-120"><dt>**CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_DOCUMENT\_DESCRIPTION**</dt></span></span> </dl> | <span data-ttu-id="7b244-121">El atributo contiene una descripción del documento firmado.</span><span class="sxs-lookup"><span data-stu-id="7b244-121">The attribute contains a description of the signed document.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="7b244-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7b244-122">Remarks</span></span>

<span data-ttu-id="7b244-123">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el estado completo del objeto.</span><span class="sxs-lookup"><span data-stu-id="7b244-123">When the value of this property is reset, directly or indirectly, the whole state of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b244-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b244-124">Requirements</span></span>



| <span data-ttu-id="7b244-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b244-125">Requirement</span></span> | <span data-ttu-id="7b244-126">Value</span><span class="sxs-lookup"><span data-stu-id="7b244-126">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b244-127">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="7b244-127">End of client support</span></span><br/> | <span data-ttu-id="7b244-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b244-128">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b244-129">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="7b244-129">End of server support</span></span><br/> | <span data-ttu-id="7b244-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b244-130">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b244-131">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="7b244-131">Redistributable</span></span><br/>       | <span data-ttu-id="7b244-132">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b244-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7b244-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7b244-133">DLL</span></span><br/>                   | <dl> <span data-ttu-id="7b244-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b244-134"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b244-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b244-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b244-136">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="7b244-136">**Attribute**</span></span>](attribute.md)
</dt> </dl>

 

 
