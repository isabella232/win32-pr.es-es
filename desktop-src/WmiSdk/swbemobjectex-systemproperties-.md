---
description: Devuelve un objeto SWbemPropertySet que contiene la colección de propiedades del sistema WMI que se aplican al objeto.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: SWbemObjectEx.Syspropiedad temProperties_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278974"
---
# <a name="swbemobjectexsystemproperties_-property"></a><span data-ttu-id="b7331-103">SWbemObjectEx.Sys\_ propiedad temProperties</span><span class="sxs-lookup"><span data-stu-id="b7331-103">SWbemObjectEx.SystemProperties\_ property</span></span>

<span data-ttu-id="b7331-104">La **propiedad \_ SystemProperties** del objeto [**SWbemObjectEx**](swbemobjectex.md) devuelve un objeto [**SWbemPropertySet**](swbempropertyset.md) que contiene la colección de [propiedades del sistema WMI](wmi-system-properties.md) que se aplican al objeto.</span><span class="sxs-lookup"><span data-stu-id="b7331-104">The **SystemProperties\_** property of the [**SWbemObjectEx**](swbemobjectex.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of [WMI System Properties](wmi-system-properties.md) that apply to the object.</span></span>

<span data-ttu-id="b7331-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b7331-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b7331-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b7331-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7331-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7331-107">Syntax</span></span>


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="b7331-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b7331-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="b7331-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b7331-109">Examples</span></span>

<span data-ttu-id="b7331-110">En el ejemplo de código siguiente se recuperan los valores de propiedad para la clase de proceso de Win32 \_ .</span><span class="sxs-lookup"><span data-stu-id="b7331-110">The following code sample retrieves the property values for the Win32\_Process class.</span></span>


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a><span data-ttu-id="b7331-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7331-111">Requirements</span></span>



| <span data-ttu-id="b7331-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7331-112">Requirement</span></span> | <span data-ttu-id="b7331-113">Value</span><span class="sxs-lookup"><span data-stu-id="b7331-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7331-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7331-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b7331-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7331-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7331-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7331-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b7331-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7331-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7331-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7331-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7331-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7331-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7331-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b7331-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7331-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b7331-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b7331-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7331-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7331-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7331-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b7331-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="b7331-124">CLSID</span></span><br/>                    | <span data-ttu-id="b7331-125">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="b7331-125">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="b7331-126">IID</span><span class="sxs-lookup"><span data-stu-id="b7331-126">IID</span></span><br/>                      | <span data-ttu-id="b7331-127">\_ISWBEMOBJECTEX IID</span><span class="sxs-lookup"><span data-stu-id="b7331-127">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b7331-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7331-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7331-129">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="b7331-129">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> </dl>

 

 




