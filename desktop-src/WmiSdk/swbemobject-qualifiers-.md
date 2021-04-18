---
description: La propiedad Qualifiers \_ del objeto SWbemObject devuelve un objeto SWbemQualifierSet que es una colección de los calificadores de la clase o la instancia actual. Esta propiedad es de solo lectura.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Qualifiers_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715736"
---
# <a name="swbemobjectqualifiers_-property"></a><span data-ttu-id="277ad-104">SWbemObject. Qualifiers \_ (propiedad)</span><span class="sxs-lookup"><span data-stu-id="277ad-104">SWbemObject.Qualifiers\_ property</span></span>

<span data-ttu-id="277ad-105">La propiedad **Qualifiers \_** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemQualifierSet**](swbemqualifierset.md) que es una colección de los calificadores de la clase o la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="277ad-105">The **Qualifiers\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemQualifierSet**](swbemqualifierset.md) object that is a collection of the qualifiers for the current class or instance.</span></span> <span data-ttu-id="277ad-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="277ad-106">This property is read-only.</span></span>

<span data-ttu-id="277ad-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="277ad-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="277ad-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="277ad-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="277ad-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="277ad-109">Syntax</span></span>


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a><span data-ttu-id="277ad-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="277ad-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="277ad-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="277ad-111">Examples</span></span>

<span data-ttu-id="277ad-112">La [lista de todos los calificadores de un](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) ejemplo de código VBScript de clase WMI en la galería de TechNet usa la propiedad calificador \_ para enumerar los calificadores de clase de una clase WMI especificada.</span><span class="sxs-lookup"><span data-stu-id="277ad-112">The [List All the Qualifiers for a WMI Class](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) VBScript code sample on TechNet Gallery uses the Qualifier\_ property to list the class qualifiers for a specified WMI class.</span></span>

<span data-ttu-id="277ad-113">En el ejemplo de código de [lista de todas las clases abstractas de WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript de la galería de TechNet se enumeran todas las clases abstractas de WMI definidas en el \\ espacio de nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="277ad-113">The [List All Abstract Classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript code sample on TechNet Gallery lists all WMI abstract classes defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="277ad-114">En el ejemplo de código de [lista de todas las clases dinámicas en WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript se usa la \_ propiedad Qualifier para enumerar todas las clases dinámicas de WMI (incluidas las clases de asociación) definidas en el \\ espacio de nombres root cimv2.</span><span class="sxs-lookup"><span data-stu-id="277ad-114">The [List All Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript code sample uses the Qualifier\_ property to list all WMI Dynamic classes (including Association classes) defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="277ad-115">En el ejemplo de código de PowerShell de [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) en la galería de TechNet se enumeran todas las propiedades que se escriben en el espacio de nombres especificado.</span><span class="sxs-lookup"><span data-stu-id="277ad-115">The [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell code sample on TechNet Gallery lists all writeable properties in the specified namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="277ad-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="277ad-116">Requirements</span></span>



| <span data-ttu-id="277ad-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="277ad-117">Requirement</span></span> | <span data-ttu-id="277ad-118">Value</span><span class="sxs-lookup"><span data-stu-id="277ad-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="277ad-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="277ad-119">Minimum supported client</span></span><br/> | <span data-ttu-id="277ad-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="277ad-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="277ad-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="277ad-121">Minimum supported server</span></span><br/> | <span data-ttu-id="277ad-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="277ad-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="277ad-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="277ad-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="277ad-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="277ad-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="277ad-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="277ad-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="277ad-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="277ad-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="277ad-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="277ad-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="277ad-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="277ad-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="277ad-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="277ad-129">CLSID</span></span><br/>                    | <span data-ttu-id="277ad-130">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="277ad-130">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="277ad-131">IID</span><span class="sxs-lookup"><span data-stu-id="277ad-131">IID</span></span><br/>                      | <span data-ttu-id="277ad-132">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="277ad-132">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




