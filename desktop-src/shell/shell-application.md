---
description: Contiene el objeto de aplicación del objeto.
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Propiedad Shell. Application (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a9f9bd7fa28d2b277adfd8038c10c97efe16f51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913306"
---
# <a name="shellapplication-property"></a><span data-ttu-id="1f043-103">Propiedad Shell. Application</span><span class="sxs-lookup"><span data-stu-id="1f043-103">Shell.Application property</span></span>

<span data-ttu-id="1f043-104">Contiene el objeto de aplicación del objeto.</span><span class="sxs-lookup"><span data-stu-id="1f043-104">Contains the object's Application object.</span></span>

<span data-ttu-id="1f043-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1f043-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f043-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f043-106">Syntax</span></span>


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="1f043-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1f043-107">Property value</span></span>

<span data-ttu-id="1f043-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="1f043-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f043-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1f043-109">Remarks</span></span>

<span data-ttu-id="1f043-110">La propiedad **Application** devuelve el objeto de automatización compatible con la aplicación que contiene el control WebBrowser, si ese objeto es accesible.</span><span class="sxs-lookup"><span data-stu-id="1f043-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="1f043-111">De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="1f043-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="1f043-112">Utilice esta propiedad con los comandos **set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de la aplicación de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="1f043-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f043-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f043-113">Requirements</span></span>



| <span data-ttu-id="1f043-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f043-114">Requirement</span></span> | <span data-ttu-id="1f043-115">Value</span><span class="sxs-lookup"><span data-stu-id="1f043-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f043-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f043-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1f043-117">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1f043-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1f043-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f043-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1f043-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1f043-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="1f043-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f043-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f043-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f043-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="1f043-122">IDL</span><span class="sxs-lookup"><span data-stu-id="1f043-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f043-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f043-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="1f043-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f043-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f043-125"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1f043-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
