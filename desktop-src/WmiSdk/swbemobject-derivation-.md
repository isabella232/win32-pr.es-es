---
description: La \_ propiedad de derivación del objeto SWbemObject contiene una matriz de cadenas que describen la jerarquía de derivación de clases para la instancia a la que se hace referencia.
ms.assetid: 8a4daab0-7d10-4a37-aacd-1f3f499b859a
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Derivation_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Derivation_
- ISWbemObject.Derivation_
- ISWbemObject.get_Derivation_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84e7b4e53a1a5544c92bb5116f3f83189789487f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706647"
---
# <a name="swbemobjectderivation_-property"></a><span data-ttu-id="e8ddb-103">SWbemObject. Derivation, \_ propiedad</span><span class="sxs-lookup"><span data-stu-id="e8ddb-103">SWbemObject.Derivation\_ property</span></span>

<span data-ttu-id="e8ddb-104">La propiedad de **derivación \_** del objeto [**SWbemObject**](swbemobject.md) contiene una matriz de cadenas que describen la jerarquía de derivación de clases para la instancia a la que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="e8ddb-104">The **Derivation\_** property of the [**SWbemObject**](swbemobject.md) object contains an array of strings that describe the class derivation hierarchy for the instance being referenced.</span></span> <span data-ttu-id="e8ddb-105">El primer elemento de la matriz define la clase primaria y el último elemento define la clase Dynasty.</span><span class="sxs-lookup"><span data-stu-id="e8ddb-105">The first element in the array defines the parent class and the last element defines the dynasty class.</span></span> <span data-ttu-id="e8ddb-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8ddb-106">This property is read-only.</span></span>

<span data-ttu-id="e8ddb-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e8ddb-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="e8ddb-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e8ddb-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8ddb-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e8ddb-109">Syntax</span></span>


```VB
SWbemObject.Derivation_ As String
```



## <a name="property-value"></a><span data-ttu-id="e8ddb-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e8ddb-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="e8ddb-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e8ddb-111">Examples</span></span>

<span data-ttu-id="e8ddb-112">En el siguiente ejemplo de VBScript se describe cómo recuperar la jerarquía de clases para el LogicalDisk de Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="e8ddb-112">The following VBScript sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```VB
on Error resume next

Set c = GetObject("winmgmts://./root/cimv2:win32_logicaldisk")
d = c.Derivation_

for x = LBound(d) to UBound(d)
 WScript.Echo d(x)
Next

if err <> 0 then
 WScript.Echo Err.Description
end if
```



<span data-ttu-id="e8ddb-113">el siguiente ejemplo de Perl describe cómo recuperar la jerarquía de clases para el LogicalDisk de Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="e8ddb-113">he following Perl sample describes how to retrieve the class hierarchy for win32\_logicaldisk.</span></span>


```
use strict;
use Win32::OLE;

my ($C, $D, @collection);

eval {$C = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
  InstancesOf ("win32_logicaldisk") };
unless ($@) 
{
 @collection = in $C;
 eval {$D = $collection[0]->Derivation_();};
 print "\n";
 unless ($@) 
 {
  print map{"$_\n"} @{$D};
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="e8ddb-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8ddb-114">Requirements</span></span>



| <span data-ttu-id="e8ddb-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8ddb-115">Requirement</span></span> | <span data-ttu-id="e8ddb-116">Value</span><span class="sxs-lookup"><span data-stu-id="e8ddb-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ddb-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8ddb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e8ddb-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8ddb-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8ddb-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e8ddb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e8ddb-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8ddb-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8ddb-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e8ddb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8ddb-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8ddb-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8ddb-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e8ddb-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8ddb-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e8ddb-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e8ddb-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e8ddb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8ddb-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8ddb-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8ddb-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="e8ddb-127">CLSID</span></span><br/>                    | <span data-ttu-id="e8ddb-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="e8ddb-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="e8ddb-129">IID</span><span class="sxs-lookup"><span data-stu-id="e8ddb-129">IID</span></span><br/>                      | <span data-ttu-id="e8ddb-130">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="e8ddb-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




