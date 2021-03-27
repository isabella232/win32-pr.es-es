---
description: Contiene el objeto de aplicación de la carpeta.
ms.assetid: 1dba83eb-1af6-42d9-b2c9-ab7767888efe
title: Propiedad Folder. Application (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Application
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: 13a6a90dd324498c332f7bf580ff5ec987a0c5b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496781"
---
# <a name="folderapplication-property"></a><span data-ttu-id="293a7-103">Folder. Application (propiedad)</span><span class="sxs-lookup"><span data-stu-id="293a7-103">Folder.Application property</span></span>

<span data-ttu-id="293a7-104">Contiene el objeto de aplicación de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="293a7-104">Contains the folder's Application object.</span></span>

<span data-ttu-id="293a7-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="293a7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="293a7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="293a7-106">Syntax</span></span>


```JScript
Application = Folder.Application
```



## <a name="property-value"></a><span data-ttu-id="293a7-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="293a7-107">Property value</span></span>

<span data-ttu-id="293a7-108">Una referencia de objeto al objeto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="293a7-108">An object reference to the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="293a7-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="293a7-109">Remarks</span></span>

<span data-ttu-id="293a7-110">La propiedad **Application** devuelve el objeto de automatización compatible con la aplicación que contiene el control WebBrowser, si ese objeto es accesible.</span><span class="sxs-lookup"><span data-stu-id="293a7-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="293a7-111">De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="293a7-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="293a7-112">Utilice esta propiedad con los comandos **set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de la aplicación de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="293a7-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Internet Explorer application.</span></span>

> [!Note]  
> <span data-ttu-id="293a7-113">No todos los métodos se implementan para todas las carpetas.</span><span class="sxs-lookup"><span data-stu-id="293a7-113">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="293a7-114">Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="293a7-114">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="293a7-115">Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).</span><span class="sxs-lookup"><span data-stu-id="293a7-115">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="293a7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="293a7-116">Requirements</span></span>



| <span data-ttu-id="293a7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="293a7-117">Requirement</span></span> | <span data-ttu-id="293a7-118">Value</span><span class="sxs-lookup"><span data-stu-id="293a7-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="293a7-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293a7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="293a7-120">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="293a7-120">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="293a7-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="293a7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="293a7-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="293a7-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="293a7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="293a7-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="293a7-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="293a7-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="293a7-125">IDL</span><span class="sxs-lookup"><span data-stu-id="293a7-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="293a7-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="293a7-126"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




