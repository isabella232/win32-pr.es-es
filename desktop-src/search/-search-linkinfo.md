---
description: Almacena información sobre los tipos de vínculo y lo usa la interfaz IItemPreviewerExt.
ms.assetid: c1d525ea-ee80-49fb-9447-20465b8f8654
title: Estructura LINKINFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: de74f7aefb61f12bf85a457e4478aa76f2156410
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275267"
---
# <a name="linkinfo-structure"></a><span data-ttu-id="d4d35-103">Estructura LINKINFO</span><span class="sxs-lookup"><span data-stu-id="d4d35-103">LINKINFO structure</span></span>

<span data-ttu-id="d4d35-104">\[**LINKINFO** y [**IItemPreviewerExt**](-search-iitempreviewerext.md) solo se admiten en Windows XP y Windows Server 2003, y ya no deben usarse.\]</span><span class="sxs-lookup"><span data-stu-id="d4d35-104">\[**LINKINFO** and [**IItemPreviewerExt**](-search-iitempreviewerext.md) are supported only on Windows XP and Windows Server 2003, and should no longer be used.\]</span></span>

<span data-ttu-id="d4d35-105">Almacena información sobre los tipos de vínculo y lo usa la interfaz [**IItemPreviewerExt**](-search-iitempreviewerext.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d35-105">Stores information about link types, and is used by the [**IItemPreviewerExt**](-search-iitempreviewerext.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4d35-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d4d35-106">Syntax</span></span>


```C++
typedef struct _LINKINFO {
  LINKTYPE type;
  BSTR     bstrContentType;
  BSTR     bstrEncoding;
  BSTR     bstrFileExt;
  VARIANT  varData;
  DWORD    dwRelatedParts;
  BSTR     bstrRelatedCid;
  Long     lCodePage;
} LINKINFO;
```



## <a name="members"></a><span data-ttu-id="d4d35-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d4d35-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d4d35-108">**type**</span><span class="sxs-lookup"><span data-stu-id="d4d35-108">**type**</span></span>
</dt> <dd>

<span data-ttu-id="d4d35-109">Tipo: **[ **LINKTYPE**](-search-linktype.md)**</span><span class="sxs-lookup"><span data-stu-id="d4d35-109">Type: **[**LINKTYPE**](-search-linktype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="d4d35-110">El tipo de vínculo especificado al rastrear o indizar indicado por una constante [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d35-110">The type of link specified when crawling or indexing indicated by a [**LINKTYPE**](-search-linktype.md) constant.</span></span>

</dd> <dt>

<span data-ttu-id="d4d35-111">**bstrContentType**</span><span class="sxs-lookup"><span data-stu-id="d4d35-111">**bstrContentType**</span></span>
</dt> <dd>

<span data-ttu-id="d4d35-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4d35-112">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d4d35-113">Valor **BSTR** que especifica el tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="d4d35-113">A **BSTR** value that specifies the content type.</span></span>

</dd> <dt>

<span data-ttu-id="d4d35-114">**bstrEncoding**</span><span class="sxs-lookup"><span data-stu-id="d4d35-114">**bstrEncoding**</span></span>
</dt> <dd>

<span data-ttu-id="d4d35-115">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4d35-115">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d4d35-116">Atributo EncodingStyle especificado en el archivo de lenguaje de descripción de servicios web (WSDL).</span><span class="sxs-lookup"><span data-stu-id="d4d35-116">An EncodingStyle attribute specified in the Web Services Description Language (WSDL) file.</span></span>

</dd> <dt>

<span data-ttu-id="d4d35-117">**bstrFileExt**</span><span class="sxs-lookup"><span data-stu-id="d4d35-117">**bstrFileExt**</span></span>
</dt> <dd>

<span data-ttu-id="d4d35-118">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4d35-118">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d4d35-119">Valor **BSTR** que especifica la extensión de nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="d4d35-119">A **BSTR** value that specifies the file name extension.</span></span>

</dd> <dt>

<span data-ttu-id="d4d35-120">**varData**</span><span class="sxs-lookup"><span data-stu-id="d4d35-120">**varData**</span></span>
</dt> <dd>

<span data-ttu-id="d4d35-121">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="d4d35-121">Type: **VARIANT**</span></span>

</dd> <dd>

<span data-ttu-id="d4d35-122">Variante que especifica el valor de la variable.</span><span class="sxs-lookup"><span data-stu-id="d4d35-122">A variant that specifies the variable value.</span></span>

</dd> <dt>

<span data-ttu-id="d4d35-123">**dwRelatedParts**</span><span class="sxs-lookup"><span data-stu-id="d4d35-123">**dwRelatedParts**</span></span>
</dt> <dd>

<span data-ttu-id="d4d35-124">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="d4d35-124">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="d4d35-125">**DWORD** que especifica las partes relacionadas.</span><span class="sxs-lookup"><span data-stu-id="d4d35-125">A **DWORD** that specifies the related parts.</span></span>

</dd> <dt>

<span data-ttu-id="d4d35-126">**bstrRelatedCid**</span><span class="sxs-lookup"><span data-stu-id="d4d35-126">**bstrRelatedCid**</span></span>
</dt> <dd>

<span data-ttu-id="d4d35-127">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4d35-127">Type: **BSTR**</span></span>

</dd> <dd>

<span data-ttu-id="d4d35-128">Valor **BSTR** que especifica una propiedad Cid, una cadena decimal con signo no rellenada.</span><span class="sxs-lookup"><span data-stu-id="d4d35-128">A **BSTR** value that specifies a Cid property, a non-padded, signed decimal string.</span></span>

</dd> <dt>

<span data-ttu-id="d4d35-129">**lCodePage**</span><span class="sxs-lookup"><span data-stu-id="d4d35-129">**lCodePage**</span></span>
</dt> <dd>

<span data-ttu-id="d4d35-130">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="d4d35-130">Type: **Long**</span></span>

</dd> <dd>

<span data-ttu-id="d4d35-131">Página de códigos que se va a usar para codificar la cadena.</span><span class="sxs-lookup"><span data-stu-id="d4d35-131">The code page to use for encoding the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4d35-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d4d35-132">Remarks</span></span>

<span data-ttu-id="d4d35-133">Para obtener una vista previa de los datos adjuntos con un controlador de protocolo de terceros en equipos que ejecutan Windows XP o Windows Server 2003, puede que sea necesario usar la estructura **LINKINFO** y las siguientes API: los métodos [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) y [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) , y la enumeración [**LINKTYPE**](-search-linktype.md) .</span><span class="sxs-lookup"><span data-stu-id="d4d35-133">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the **LINKINFO** structure, and the following APIs: the [**IItemPreviewerExt::GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) and [**IItemPreviewerExt::GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) methods, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4d35-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4d35-134">Requirements</span></span>



| <span data-ttu-id="d4d35-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4d35-135">Requirement</span></span> | <span data-ttu-id="d4d35-136">Value</span><span class="sxs-lookup"><span data-stu-id="d4d35-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d4d35-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4d35-137">Minimum supported client</span></span><br/> | <span data-ttu-id="d4d35-138">Solo aplicaciones de escritorio de Windows XP con SP2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4d35-138">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d4d35-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4d35-139">Minimum supported server</span></span><br/> | <span data-ttu-id="d4d35-140">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4d35-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d4d35-141">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d4d35-141">Redistributable</span></span><br/>          | <span data-ttu-id="d4d35-142">Búsqueda en el escritorio de Windows (WDS) 3,0</span><span class="sxs-lookup"><span data-stu-id="d4d35-142">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



 

 




