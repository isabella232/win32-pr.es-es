---
description: El \_ método GetObjectText del objeto SWbemObject devuelve una representación textual del objeto.
ms.assetid: 8b980863-14ad-4884-8897-dd076d927824
ms.tgt_platform: multiple
title: Método SWbemObject.GetObjectText_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
- ISWbemObject.GetObjectText_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2447d8361d02626e1f5ea8fae1928ffd563d52ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648277"
---
# <a name="swbemobjectgetobjecttext_-method"></a><span data-ttu-id="70e2d-103">SWbemObject. GetObjectText, \_ método</span><span class="sxs-lookup"><span data-stu-id="70e2d-103">SWbemObject.GetObjectText\_ method</span></span>

<span data-ttu-id="70e2d-104">El **método \_ GetObjectText** del objeto [**SWbemObject**](swbemobject.md) devuelve una representación textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="70e2d-104">The **GetObjectText\_** method of the [**SWbemObject**](swbemobject.md) object returns a textual rendering of the object.</span></span> <span data-ttu-id="70e2d-105">Este objeto se puede usar para mostrar el contenido de un objeto.</span><span class="sxs-lookup"><span data-stu-id="70e2d-105">This object can be used to display an object's contents.</span></span> <span data-ttu-id="70e2d-106">Actualmente, solo se admite la sintaxis MOF como formato de salida.</span><span class="sxs-lookup"><span data-stu-id="70e2d-106">Currently, only the MOF syntax is supported as an output format.</span></span> <span data-ttu-id="70e2d-107">Tenga en cuenta que el texto MOF devuelto no contiene toda la información sobre el objeto; el texto MOF solo contiene información suficiente para que el compilador MOF pueda volver a crear el objeto original.</span><span class="sxs-lookup"><span data-stu-id="70e2d-107">Notice that the MOF text returned does not contain all the information about the object; the MOF text contains only enough information for the MOF compiler to be able to re-create the original object.</span></span> <span data-ttu-id="70e2d-108">Por ejemplo, no hay información sobre los calificadores propagados o las propiedades de la clase primaria.</span><span class="sxs-lookup"><span data-stu-id="70e2d-108">For instance, there is no information about the propagated qualifiers or the parent class properties.</span></span>

<span data-ttu-id="70e2d-109">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="70e2d-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="70e2d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70e2d-110">Syntax</span></span>


```VB
strMofText = .GetObjectText_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="70e2d-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70e2d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70e2d-112">*iFlags* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="70e2d-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="70e2d-113">Reserved y debe ser 0 (cero) si se especifica.</span><span class="sxs-lookup"><span data-stu-id="70e2d-113">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70e2d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70e2d-114">Return value</span></span>

<span data-ttu-id="70e2d-115">Si es correcto, este método devuelve una cadena que contiene el texto de salida.</span><span class="sxs-lookup"><span data-stu-id="70e2d-115">If successful, this method returns a string that contains the output text.</span></span>

## <a name="error-codes"></a><span data-ttu-id="70e2d-116">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="70e2d-116">Error codes</span></span>

<span data-ttu-id="70e2d-117">Después de completar el método **GetObjectText \_** , el objeto **Err** puede contener uno de los códigos de error de la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="70e2d-117">After the completion of the **GetObjectText\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="70e2d-118">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="70e2d-118">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="70e2d-119">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="70e2d-119">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="70e2d-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="70e2d-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="70e2d-121">Se especificó un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="70e2d-121">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="70e2d-122">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="70e2d-122">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="70e2d-123">Memoria insuficiente para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="70e2d-123">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="70e2d-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="70e2d-124">Examples</span></span>

<span data-ttu-id="70e2d-125">El código siguiente, tomado de la [lista de la definición de una clase WMI en formato MOF](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) ejemplo de código VBScript en la galería de TechNet, recupera y muestra la representación textual de una definición de clase WMI en la sintaxis MOF (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="70e2d-125">The following code, taken from the [List the Definition of a WMI Class in MOF Format](https://Gallery.TechNet.Microsoft.Com/6bb54091-dd6f-4d0b-87af-2431fb8c3be6) VBScript code sample in the TechNet Gallery, retrieves and displays the textual representation of a WMI class definition in MOF (Managed Object Format) syntax.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Const wbemFlagUseAmendedQualifiers = &h20000 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace) 
 
Set objClass = objWMIService.Get(strClass, wbemFlagUseAmendedQualifiers) 
strMOF = objClass.GetObjectText_ 
  
WScript.Echo strMOF 
```



## <a name="requirements"></a><span data-ttu-id="70e2d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70e2d-126">Requirements</span></span>



| <span data-ttu-id="70e2d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="70e2d-127">Requirement</span></span> | <span data-ttu-id="70e2d-128">Value</span><span class="sxs-lookup"><span data-stu-id="70e2d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="70e2d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70e2d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="70e2d-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="70e2d-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="70e2d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70e2d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="70e2d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="70e2d-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="70e2d-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70e2d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="70e2d-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="70e2d-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="70e2d-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="70e2d-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="70e2d-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="70e2d-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="70e2d-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="70e2d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70e2d-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70e2d-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="70e2d-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="70e2d-139">CLSID</span></span><br/>                    | <span data-ttu-id="70e2d-140">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="70e2d-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="70e2d-141">IID</span><span class="sxs-lookup"><span data-stu-id="70e2d-141">IID</span></span><br/>                      | <span data-ttu-id="70e2d-142">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="70e2d-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




