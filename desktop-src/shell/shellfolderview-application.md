---
description: 'Propiedad ShellFolderView.Application: contiene el objeto Application del objeto.'
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: Propiedad ShellFolderView.Application (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 95ef542f91235b3b068e1b1b54768b4dd453d9b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083473"
---
# <a name="shellfolderviewapplication-property"></a><span data-ttu-id="8cc6c-103">Propiedad ShellFolderView.Application</span><span class="sxs-lookup"><span data-stu-id="8cc6c-103">ShellFolderView.Application property</span></span>

<span data-ttu-id="8cc6c-104">Contiene el objeto Application del objeto .</span><span class="sxs-lookup"><span data-stu-id="8cc6c-104">Contains the object's Application object.</span></span>

<span data-ttu-id="8cc6c-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8cc6c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8cc6c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8cc6c-106">Syntax</span></span>


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a><span data-ttu-id="8cc6c-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="8cc6c-107">Property value</span></span>

<span data-ttu-id="8cc6c-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto Application.</span><span class="sxs-lookup"><span data-stu-id="8cc6c-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the Application object.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cc6c-109">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8cc6c-109">Remarks</span></span>

<span data-ttu-id="8cc6c-110">La **propiedad Application** devuelve el objeto de automatización admitido por la aplicación que contiene el control WebBrowser, si ese objeto es accesible.</span><span class="sxs-lookup"><span data-stu-id="8cc6c-110">The **Application** property returns the automation object supported by the application that contains the WebBrowser control, if that object is accessible.</span></span> <span data-ttu-id="8cc6c-111">De lo contrario, esta propiedad devuelve el objeto de automatización del control WebBrowser.</span><span class="sxs-lookup"><span data-stu-id="8cc6c-111">Otherwise, this property returns the WebBrowser control's automation object.</span></span>

<span data-ttu-id="8cc6c-112">Use esta propiedad con los comandos **Set** y **CreateObject** o con el comando **GetObject** para crear y manipular una instancia de windows Internet Explorer aplicación.</span><span class="sxs-lookup"><span data-stu-id="8cc6c-112">Use this property with the **Set** and **CreateObject** commands or with the **GetObject** command to create and manipulate an instance of the Windows Internet Explorer application.</span></span>

## <a name="requirements"></a><span data-ttu-id="8cc6c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8cc6c-113">Requirements</span></span>



| <span data-ttu-id="8cc6c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="8cc6c-114">Requirement</span></span> | <span data-ttu-id="8cc6c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8cc6c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8cc6c-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cc6c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8cc6c-117">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="8cc6c-117">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8cc6c-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8cc6c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8cc6c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8cc6c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8cc6c-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8cc6c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cc6c-121"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="8cc6c-121"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8cc6c-122">Idl</span><span class="sxs-lookup"><span data-stu-id="8cc6c-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8cc6c-123"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="8cc6c-123"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8cc6c-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8cc6c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cc6c-125"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8cc6c-125"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
