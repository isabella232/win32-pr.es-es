---
title: Elemento CredentialsBlob (EapHostUserCredentials)
description: Se usa cuando la configuración del método es un BLOB binario en lugar de en formato de texto XML.
ms.assetid: 9d03374b-74f6-428e-8d3e-f8dccf51884e
keywords:
- Elemento CredentialsBlob EAPHost
topic_type:
- apiref
api_name:
- CredentialsBlob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fe7514c3aff50a7ecddadb3d8073a37b6c770eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150072"
---
# <a name="credentialsblob-eaphostusercredentials-element"></a><span data-ttu-id="2bd0b-104">Elemento CredentialsBlob (EapHostUserCredentials)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-104">CredentialsBlob (EapHostUserCredentials) Element</span></span>

<span data-ttu-id="2bd0b-105">El elemento **CredentialsBlob (EapHostUserCredentials)** se usa cuando la configuración del método es un BLOB binario en lugar de en formato de texto XML.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-105">The **CredentialsBlob (EapHostUserCredentials)** element is used when the method configuration is a binary BLOB instead of in XML text format.</span></span>

``` syntax
<xs:element name="CredentialsBlob"
    type="hexBinary"
 />
```

<span data-ttu-id="2bd0b-106">El elemento **CredentialsBlob** se define mediante el elemento [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2bd0b-106">The **CredentialsBlob** element is defined by the [**EapHostUserCredentials**](eaphostusercredentialsschema-eaphostusercredentials-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2bd0b-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bd0b-107">Remarks</span></span>

<span data-ttu-id="2bd0b-108">Los elementos [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) y **CredentialsBlob** no se pueden usar simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-108">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and **CredentialsBlob** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bd0b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2bd0b-109">Requirements</span></span>



| <span data-ttu-id="2bd0b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2bd0b-110">Requirement</span></span> | <span data-ttu-id="2bd0b-111">Value</span><span class="sxs-lookup"><span data-stu-id="2bd0b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2bd0b-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bd0b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2bd0b-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2bd0b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2bd0b-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2bd0b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2bd0b-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2bd0b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2bd0b-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="2bd0b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="2bd0b-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="2bd0b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2bd0b-118">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="2bd0b-118">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

<span data-ttu-id="2bd0b-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="2bd0b-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2bd0b-120">**EapHostUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="2bd0b-120">**EapHostUserCredentials**</span></span>](eaphostusercredentialsschema-eaphostusercredentials-element.md)
</dt> <dt>

[<span data-ttu-id="2bd0b-121">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="2bd0b-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2bd0b-122">Esquema eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="2bd0b-122">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





