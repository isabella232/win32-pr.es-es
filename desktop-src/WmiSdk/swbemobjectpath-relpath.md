---
description: La propiedad Relpath del objeto SWbemObjectPath contiene la ruta de acceso relativa de la ruta de acceso completa.
ms.assetid: 9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b
ms.tgt_platform: multiple
title: Propiedad SWbemObjectPath. Relpath (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Relpath
- ISWbemObjectPath.Relpath
- ISWbemObjectPath.get_Relpath
- ISWbemObjectPath.put_Relpath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8330d1cdc65e818acd4fda63b223303b779b5472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659955"
---
# <a name="swbemobjectpathrelpath-property"></a><span data-ttu-id="d35fb-103">Propiedad SWbemObjectPath. Relpath</span><span class="sxs-lookup"><span data-stu-id="d35fb-103">SWbemObjectPath.Relpath property</span></span>

<span data-ttu-id="d35fb-104">La propiedad **Relpath** del objeto [**SWbemObjectPath**](swbemobjectpath.md) contiene la ruta de acceso relativa de la ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="d35fb-104">The **Relpath** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the relative path from the complete path.</span></span>

<span data-ttu-id="d35fb-105">Para obtener una explicación de esta sintaxis, vea [convenciones de documentos para la API de scripting](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d35fb-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d35fb-106">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d35fb-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d35fb-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d35fb-107">Syntax</span></span>


```VB
SWbemObjectPath.Relpath As String
```



## <a name="property-value"></a><span data-ttu-id="d35fb-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="d35fb-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="d35fb-109">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d35fb-109">Examples</span></span>

<span data-ttu-id="d35fb-110">En el ejemplo de código de VBScript siguiente se muestra la diferencia entre los datos obtenidos de [**SWbemObject. Path \_**](swbemobject-path-.md) y **SWbemObjectPath. Relpath**.</span><span class="sxs-lookup"><span data-stu-id="d35fb-110">The following VBScript code example shows the difference between the data obtained from [**SWbemObject.Path\_**](swbemobject-path-.md) and **SWbemObjectPath.Relpath**.</span></span>


```VB
set objWMIService = GetObject ("winmgmts:root/cimv2")

set Processes = objWMIService.ExecQuery( _
    "Select * from win32_process")

For Each Process in Processes
 WScript.Echo Process.Path_ 
 WScript.Echo Process.Path_.Relpath
Next
```



## <a name="requirements"></a><span data-ttu-id="d35fb-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d35fb-111">Requirements</span></span>



| <span data-ttu-id="d35fb-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d35fb-112">Requirement</span></span> | <span data-ttu-id="d35fb-113">Value</span><span class="sxs-lookup"><span data-stu-id="d35fb-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d35fb-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d35fb-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d35fb-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d35fb-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d35fb-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d35fb-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d35fb-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d35fb-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d35fb-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d35fb-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d35fb-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d35fb-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d35fb-120">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d35fb-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="d35fb-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d35fb-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d35fb-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d35fb-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d35fb-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d35fb-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d35fb-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="d35fb-124">CLSID</span></span><br/>                    | <span data-ttu-id="d35fb-125">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="d35fb-125">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="d35fb-126">IID</span><span class="sxs-lookup"><span data-stu-id="d35fb-126">IID</span></span><br/>                      | <span data-ttu-id="d35fb-127">\_ISWBEMOBJECTPATH IID</span><span class="sxs-lookup"><span data-stu-id="d35fb-127">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




