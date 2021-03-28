---
description: Contiene el objeto de aplicación del elemento de carpeta.
ms.assetid: cd8d6dea-1d16-4d62-b56b-c915192f730b
title: Propiedad carpeta. Application (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 72816ed0c426f6ff3fa92c30a1ec31757c0a02fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539519"
---
# <a name="folderitemapplication-property"></a><span data-ttu-id="9fc6a-103">Propiedad carpeta. Application</span><span class="sxs-lookup"><span data-stu-id="9fc6a-103">FolderItem.Application property</span></span>

<span data-ttu-id="9fc6a-104">Contiene el objeto de **aplicación** del elemento de carpeta.</span><span class="sxs-lookup"><span data-stu-id="9fc6a-104">Contains the **Application** object of the folder item.</span></span>

<span data-ttu-id="9fc6a-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9fc6a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fc6a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9fc6a-106">Syntax</span></span>


```JScript
objApplication = FolderItem.Application
```



## <a name="property-value"></a><span data-ttu-id="9fc6a-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9fc6a-107">Property value</span></span>

<span data-ttu-id="9fc6a-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de **aplicación** .</span><span class="sxs-lookup"><span data-stu-id="9fc6a-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the **Application** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9fc6a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fc6a-109">Remarks</span></span>

<span data-ttu-id="9fc6a-110">La propiedad **Application** devuelve el objeto de automatización compatible con la aplicación que contiene el control WebBrowser, si ese objeto es accesible.</span><span class="sxs-lookup"><span data-stu-id="9fc6a-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="9fc6a-111">De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="9fc6a-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="9fc6a-112">Utilice esta propiedad con los comandos **set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de la aplicación de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="9fc6a-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fc6a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fc6a-113">Requirements</span></span>



| <span data-ttu-id="9fc6a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fc6a-114">Requirement</span></span> | <span data-ttu-id="9fc6a-115">Value</span><span class="sxs-lookup"><span data-stu-id="9fc6a-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fc6a-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fc6a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9fc6a-117">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9fc6a-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9fc6a-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9fc6a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9fc6a-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9fc6a-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9fc6a-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fc6a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fc6a-121"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fc6a-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9fc6a-122">IDL</span><span class="sxs-lookup"><span data-stu-id="9fc6a-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9fc6a-123"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9fc6a-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9fc6a-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9fc6a-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fc6a-125"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9fc6a-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
