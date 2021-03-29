---
description: La propiedad Namespace del objeto SWbemObjectPath contiene el nombre del espacio de nombres que forma parte de la ruta de acceso del objeto.
ms.assetid: be88670d-6f0d-4b9d-886f-3e70bf4758ed
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath. Namespace (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Namespace
- ISWbemObjectPath.Namespace
- ISWbemObjectPath.get_Namespace
- ISWbemObjectPath.put_Namespace
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 885f7069e901d1d4a490ad7539077463f6c1838c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277323"
---
# <a name="swbemobjectpathnamespace-property"></a><span data-ttu-id="5247e-103">Propiedad SWbemObjectPath. Namespace</span><span class="sxs-lookup"><span data-stu-id="5247e-103">SWbemObjectPath.Namespace property</span></span>

<span data-ttu-id="5247e-104">La propiedad **namespace** del objeto [**SWbemObjectPath**](swbemobjectpath.md) contiene el nombre del espacio de nombres que forma parte de la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="5247e-104">The **Namespace** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the name of the namespace that is part of the object path.</span></span> <span data-ttu-id="5247e-105">Por ejemplo, la ruta de acceso siguiente muestra la propiedad de espacio de nombres que devuelve la raíz \\ cimv2:</span><span class="sxs-lookup"><span data-stu-id="5247e-105">For example, the following path shows the namespace property that returns root\\cimv2:</span></span>

``` syntax
\\computer\root\cimv2:win32_logicaldisk="a:"
```

<span data-ttu-id="5247e-106">Para ver la explicación de la sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5247e-106">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="5247e-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5247e-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5247e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5247e-108">Syntax</span></span>


```VB
SWbemObjectPath.Namespace As String
```



## <a name="property-value"></a><span data-ttu-id="5247e-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5247e-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="5247e-110">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5247e-110">Examples</span></span>

<span data-ttu-id="5247e-111">En el ejemplo siguiente se muestra cómo obtener el nombre del espacio de nombres de las instancias de [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) que son discos duros.</span><span class="sxs-lookup"><span data-stu-id="5247e-111">The following example shows you how to obtain the namespace name from instances of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) that are hard disks.</span></span> <span data-ttu-id="5247e-112">El script se conecta al espacio de nombres predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5247e-112">The script connects to the default namespace.</span></span>


```VB
Const HARD_DISK = 3
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer)

Set colDisks = objWMIService.ExecQuery _
    ("Select * from Win32_LogicalDisk " _
    & "Where DriveType = " & HARD_DISK & "")
For Each objDisk in colDisks
    Set objpath = objDisk.path_
    Wscript.Echo "Path of Win32_Logical disk instance " _
    & objDisk.DeviceID & " = " & objpath.Namespace   
Next
```



## <a name="requirements"></a><span data-ttu-id="5247e-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5247e-113">Requirements</span></span>



| <span data-ttu-id="5247e-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="5247e-114">Requirement</span></span> | <span data-ttu-id="5247e-115">Value</span><span class="sxs-lookup"><span data-stu-id="5247e-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5247e-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5247e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5247e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5247e-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5247e-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5247e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5247e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5247e-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5247e-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5247e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5247e-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5247e-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5247e-122">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="5247e-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="5247e-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5247e-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5247e-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5247e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5247e-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5247e-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5247e-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="5247e-126">CLSID</span></span><br/>                    | <span data-ttu-id="5247e-127">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="5247e-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="5247e-128">IID</span><span class="sxs-lookup"><span data-stu-id="5247e-128">IID</span></span><br/>                      | <span data-ttu-id="5247e-129">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="5247e-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

