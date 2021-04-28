---
description: 'Propiedad Shell.Application: contiene el objeto Application del objeto .'
ms.assetid: 5335f4dd-ca80-49c8-8953-e32a6e6308e0
title: Propiedad Shell.Application (Shldisp.h)
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
ms.openlocfilehash: 5a90b3953ed54b8a3652d6c9c26533d433ffb600
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083863"
---
# <a name="shellapplication-property"></a><span data-ttu-id="387ba-103">Propiedad Shell.Application</span><span class="sxs-lookup"><span data-stu-id="387ba-103">Shell.Application property</span></span>

<span data-ttu-id="387ba-104">Contiene el objeto Application del objeto .</span><span class="sxs-lookup"><span data-stu-id="387ba-104">Contains the object's Application object.</span></span>

<span data-ttu-id="387ba-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="387ba-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="387ba-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="387ba-106">Syntax</span></span>


```JScript
objApplication = Shell.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a><span data-ttu-id="387ba-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="387ba-107">Property value</span></span>

<span data-ttu-id="387ba-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto Application.</span><span class="sxs-lookup"><span data-stu-id="387ba-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="387ba-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="387ba-109">Remarks</span></span>

<span data-ttu-id="387ba-110">La **propiedad Application** devuelve el objeto de automatización admitido por la aplicación que contiene el control WebBrowser, si ese objeto es accesible.</span><span class="sxs-lookup"><span data-stu-id="387ba-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="387ba-111">De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="387ba-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="387ba-112">Use esta propiedad con los comandos **Set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de windows Internet Explorer aplicación.</span><span class="sxs-lookup"><span data-stu-id="387ba-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="387ba-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="387ba-113">Requirements</span></span>



| <span data-ttu-id="387ba-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="387ba-114">Requirement</span></span> | <span data-ttu-id="387ba-115">Valor</span><span class="sxs-lookup"><span data-stu-id="387ba-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="387ba-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="387ba-116">Minimum supported client</span></span><br/> | <span data-ttu-id="387ba-117">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="387ba-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="387ba-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="387ba-118">Minimum supported server</span></span><br/> | <span data-ttu-id="387ba-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="387ba-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="387ba-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="387ba-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="387ba-121"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="387ba-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="387ba-122">Idl</span><span class="sxs-lookup"><span data-stu-id="387ba-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="387ba-123"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="387ba-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="387ba-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="387ba-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="387ba-125"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="387ba-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
