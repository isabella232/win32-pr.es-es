---
description: La \_ propiedad Properties del objeto SWbemObject devuelve un objeto SWbemPropertySet que es una colección de las propiedades de la clase o la instancia actual. Esta propiedad es de solo lectura.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: Propiedad SWbemObject.Properties_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706051"
---
# <a name="swbemobjectproperties_-property"></a><span data-ttu-id="eae26-104">Propiedad SWbemObject. Properties \_</span><span class="sxs-lookup"><span data-stu-id="eae26-104">SWbemObject.Properties\_ property</span></span>

<span data-ttu-id="eae26-105">La **propiedad \_ Properties** del objeto [**SWbemObject**](swbemobject.md) devuelve un objeto [**SWbemPropertySet**](swbempropertyset.md) que es una colección de las propiedades de la clase o la instancia actual.</span><span class="sxs-lookup"><span data-stu-id="eae26-105">The **Properties\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that is a collection of the properties for the current class or instance.</span></span> <span data-ttu-id="eae26-106">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eae26-106">This property is read-only.</span></span>

<span data-ttu-id="eae26-107">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eae26-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="eae26-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="eae26-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eae26-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eae26-109">Syntax</span></span>


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="eae26-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="eae26-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="eae26-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="eae26-111">Examples</span></span>

<span data-ttu-id="eae26-112">El ejemplo de código de PowerShell [generar scripts de clase WMI de PowerShell](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) en la galería de TechNet usa la \_ propiedad Properties para generar un script para cada una de las clases WMI que mostrarán el nombre de la clase WMI y las propiedades.</span><span class="sxs-lookup"><span data-stu-id="eae26-112">The [Generate Powershell WMI Class Scripts](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) PowerShell code example on TechNet Gallery uses the Properties\_ property to generate a script for each of the WMI classes that will list the WMI class name and the properties.</span></span>

<span data-ttu-id="eae26-113">En el código siguiente, tomado de la [lista todas las propiedades de un ejemplo de código de VBScript de clase WMI](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) en la galería de TechNet, se enumeran las propiedades de una clase WMI especificada.</span><span class="sxs-lookup"><span data-stu-id="eae26-113">The following code, taken from the [List All the Properties for a WMI Class](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) VBScript code example on TechNet Gallery, Lists the properties for a specified WMI class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="eae26-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eae26-114">Requirements</span></span>



| <span data-ttu-id="eae26-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="eae26-115">Requirement</span></span> | <span data-ttu-id="eae26-116">Value</span><span class="sxs-lookup"><span data-stu-id="eae26-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eae26-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eae26-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eae26-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eae26-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eae26-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eae26-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eae26-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eae26-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eae26-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eae26-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eae26-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eae26-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eae26-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="eae26-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="eae26-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eae26-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eae26-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eae26-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eae26-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eae26-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eae26-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="eae26-127">CLSID</span></span><br/>                    | <span data-ttu-id="eae26-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="eae26-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="eae26-129">IID</span><span class="sxs-lookup"><span data-stu-id="eae26-129">IID</span></span><br/>                      | <span data-ttu-id="eae26-130">\_ISWBEMOBJECT IID</span><span class="sxs-lookup"><span data-stu-id="eae26-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




