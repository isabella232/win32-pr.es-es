---
description: Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.
title: Método ShellFolderView. PopupItemMenu (Shldisp. h)
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
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278498"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="ea333-103">ShellFolderView. PopupItemMenu, método</span><span class="sxs-lookup"><span data-stu-id="ea333-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="ea333-104">Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.</span><span class="sxs-lookup"><span data-stu-id="ea333-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea333-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ea333-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="ea333-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ea333-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea333-107">*vItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ea333-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea333-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="ea333-108">Type: **Variant**</span></span>

<span data-ttu-id="ea333-109">Objeto [**carpeta**](folderitem.md) para el que se creará el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="ea333-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="ea333-110">*VX* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ea333-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea333-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="ea333-111">Type: **Variant**</span></span>

<span data-ttu-id="ea333-112">Posición horizontal del menú, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ea333-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="ea333-113">*VY* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ea333-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ea333-114">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="ea333-114">Type: **Variant**</span></span>

<span data-ttu-id="ea333-115">Posición vertical del menú, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="ea333-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea333-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ea333-116">Return value</span></span>

<span data-ttu-id="ea333-117">Tipo: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="ea333-117">Type: \**[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="ea333-118">_ *Cadena*\* que recibe la cadena de comandos.</span><span class="sxs-lookup"><span data-stu-id="ea333-118">The _ *String*\* that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea333-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea333-119">Requirements</span></span>



| <span data-ttu-id="ea333-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea333-120">Requirement</span></span> | <span data-ttu-id="ea333-121">Value</span><span class="sxs-lookup"><span data-stu-id="ea333-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea333-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea333-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ea333-123">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="ea333-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ea333-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ea333-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ea333-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ea333-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ea333-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea333-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea333-127"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea333-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ea333-128">IDL</span><span class="sxs-lookup"><span data-stu-id="ea333-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea333-129"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea333-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ea333-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ea333-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea333-131"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="ea333-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
