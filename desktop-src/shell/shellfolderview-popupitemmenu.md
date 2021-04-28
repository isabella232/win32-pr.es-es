---
description: 'Método ShellFolderView.PopupItemMenu: crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.'
title: Método ShellFolderView.PopupItemMenu (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: cb862ba159f55d3ab82495ddeb32a87f3ce1901b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083393"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="ae887-103">Método ShellFolderView.PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="ae887-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="ae887-104">Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ae887-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae887-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae887-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="ae887-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ae887-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae887-107">*vItem* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="ae887-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae887-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ae887-108">Type: **Variant**</span></span>

<span data-ttu-id="ae887-109">Objeto [**FolderItem**](folderitem.md) para el que se creará el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="ae887-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="ae887-110">*vx* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ae887-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ae887-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ae887-111">Type: **Variant**</span></span>

<span data-ttu-id="ae887-112">Posición horizontal del menú, en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ae887-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="ae887-113">*vy* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ae887-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ae887-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="ae887-114">Type: **Variant**</span></span>

<span data-ttu-id="ae887-115">Posición vertical del menú, en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ae887-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae887-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae887-116">Return value</span></span>

<span data-ttu-id="ae887-117">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="ae887-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="ae887-118">Cadena **que** recibe la cadena de comando.</span><span class="sxs-lookup"><span data-stu-id="ae887-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae887-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae887-119">Requirements</span></span>



| <span data-ttu-id="ae887-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae887-120">Requirement</span></span> | <span data-ttu-id="ae887-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ae887-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae887-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae887-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae887-123">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="ae887-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ae887-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ae887-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae887-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ae887-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ae887-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ae887-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae887-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="ae887-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ae887-128">Idl</span><span class="sxs-lookup"><span data-stu-id="ae887-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ae887-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae887-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ae887-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ae887-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae887-131"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ae887-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
