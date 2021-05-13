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
ms.openlocfilehash: 7a2feda23d6e1759e1c0be27805fefbb6b592df7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840756"
---
# <a name="shellfolderviewpopupitemmenu-method"></a><span data-ttu-id="9f738-103">Método ShellFolderView.PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="9f738-103">ShellFolderView.PopupItemMenu method</span></span>

<span data-ttu-id="9f738-104">Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.</span><span class="sxs-lookup"><span data-stu-id="9f738-104">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f738-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f738-105">Syntax</span></span>


```JScript
retVal = ShellFolderView.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="9f738-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9f738-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f738-107">*vItem* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="9f738-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f738-108">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9f738-108">Type: **Variant**</span></span>

<span data-ttu-id="9f738-109">Objeto [**FolderItem**](folderitem.md) para el que se creará el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="9f738-109">The [**FolderItem**](folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="9f738-110">*vx* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9f738-110">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f738-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9f738-111">Type: **Variant**</span></span>

<span data-ttu-id="9f738-112">Posición horizontal del menú, en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9f738-112">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="9f738-113">*vy* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="9f738-113">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9f738-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="9f738-114">Type: **Variant**</span></span>

<span data-ttu-id="9f738-115">Posición vertical del menú, en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="9f738-115">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f738-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9f738-116">Return value</span></span>

<span data-ttu-id="9f738-117">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="9f738-117">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="9f738-118">Cadena **que** recibe la cadena de comando.</span><span class="sxs-lookup"><span data-stu-id="9f738-118">The **String** that receives the command string.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f738-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f738-119">Requirements</span></span>



| <span data-ttu-id="9f738-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f738-120">Requirement</span></span> | <span data-ttu-id="9f738-121">Value</span><span class="sxs-lookup"><span data-stu-id="9f738-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f738-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f738-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9f738-123">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="9f738-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9f738-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9f738-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9f738-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9f738-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="9f738-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f738-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f738-127"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="9f738-127"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="9f738-128">Idl</span><span class="sxs-lookup"><span data-stu-id="9f738-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f738-129"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f738-129"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="9f738-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9f738-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f738-131"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="9f738-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
