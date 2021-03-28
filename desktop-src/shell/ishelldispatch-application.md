---
description: Contiene un objeto que representa una aplicación.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: Propiedad IShellDispatch. Application (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543166"
---
# <a name="ishelldispatchapplication-property"></a><span data-ttu-id="116cf-103">Propiedad IShellDispatch. Application</span><span class="sxs-lookup"><span data-stu-id="116cf-103">IShellDispatch.Application property</span></span>

<span data-ttu-id="116cf-104">Contiene un objeto que representa una aplicación.</span><span class="sxs-lookup"><span data-stu-id="116cf-104">Contains an object that represents an application.</span></span>

<span data-ttu-id="116cf-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="116cf-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="116cf-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="116cf-106">Syntax</span></span>


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="116cf-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="116cf-107">Property value</span></span>

<span data-ttu-id="116cf-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="116cf-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="116cf-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="116cf-109">Remarks</span></span>

<span data-ttu-id="116cf-110">Esta propiedad se implementa y se obtiene acceso a ella a través de la propiedad [**Shell. EjectPC**](shell-ejectpc.md) .</span><span class="sxs-lookup"><span data-stu-id="116cf-110">This property is implemented and accessed through the [**Shell.EjectPC**](shell-ejectpc.md) property.</span></span>

<span data-ttu-id="116cf-111">La propiedad **Application** devuelve el objeto de automatización compatible con la aplicación que contiene el control WebBrowser, si ese objeto es accesible.</span><span class="sxs-lookup"><span data-stu-id="116cf-111">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="116cf-112">De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="116cf-112">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="116cf-113">Utilice esta propiedad con los comandos **set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de la aplicación de Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="116cf-113">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="116cf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="116cf-114">Requirements</span></span>



| <span data-ttu-id="116cf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="116cf-115">Requirement</span></span> | <span data-ttu-id="116cf-116">Value</span><span class="sxs-lookup"><span data-stu-id="116cf-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="116cf-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="116cf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="116cf-118">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="116cf-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="116cf-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="116cf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="116cf-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="116cf-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="116cf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="116cf-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="116cf-122"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="116cf-122"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="116cf-123">IDL</span><span class="sxs-lookup"><span data-stu-id="116cf-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="116cf-124"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="116cf-124"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="116cf-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="116cf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="116cf-126"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="116cf-126"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
