---
description: La propiedad Methods \_ del objeto SWbemObject devuelve un objeto SWbemMethodSet que es una colección de los métodos de la clase o la instancia actual. Esta propiedad es de solo lectura.
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Methods_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6a702f0acf0736810de4d3176f8695fa8008d3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707087"
---
# <a name="swbemobjectmethods_-property"></a><span data-ttu-id="d9823-104">Propiedad SWbemObject. Methods \_</span><span class="sxs-lookup"><span data-stu-id="d9823-104">SWbemObject.Methods\_ property</span></span>

<span data-ttu-id="d9823-105">La **propiedad \_ Methods** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemMethodSet**](swbemmethodset.md) que es una colección de los métodos de la clase o la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="d9823-105">The **Methods\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemMethodSet**](swbemmethodset.md) object that is a collection of the methods for the current class or instance.</span></span> <span data-ttu-id="d9823-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9823-106">This property is read-only.</span></span>

<span data-ttu-id="d9823-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d9823-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d9823-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9823-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9823-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9823-109">Syntax</span></span>


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a><span data-ttu-id="d9823-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d9823-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="d9823-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d9823-111">Examples</span></span>

<span data-ttu-id="d9823-112">En el siguiente [ejemplo de código](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), tomado de la galería de TechNet, se describe cómo enumerar todos los métodos de una clase.</span><span class="sxs-lookup"><span data-stu-id="d9823-112">The following [code sample](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), taken from the TechNet Gallery, describes how to list all methods of a class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="d9823-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9823-113">Requirements</span></span>



| <span data-ttu-id="d9823-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9823-114">Requirement</span></span> | <span data-ttu-id="d9823-115">Value</span><span class="sxs-lookup"><span data-stu-id="d9823-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9823-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9823-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d9823-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9823-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9823-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9823-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d9823-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9823-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9823-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d9823-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d9823-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9823-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9823-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d9823-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9823-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d9823-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d9823-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9823-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9823-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9823-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d9823-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="d9823-126">CLSID</span></span><br/>                    | <span data-ttu-id="d9823-127">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="d9823-127">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="d9823-128">IID</span><span class="sxs-lookup"><span data-stu-id="d9823-128">IID</span></span><br/>                      | <span data-ttu-id="d9823-129">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="d9823-129">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




