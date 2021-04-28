---
title: Método WebViewFolderContents.PopupItemMenu (Shldisp.h)
description: 'Método WebViewFolderContents.PopupItemMenu: crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.'
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Características heredadas del entorno de Windows del método PopupItemMenu
- Método PopupItemMenu Características heredadas del entorno de Windows , Objeto WebViewFolderContents
- Objeto WebViewFolderContents Características heredadas del entorno de Windows, método PopupItemMenu
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c879e10097b334f0c2d4f98b1b76289d20ee4a93
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102643"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="5ad1e-106">Método WebViewFolderContents.PopupItemMenu</span><span class="sxs-lookup"><span data-stu-id="5ad1e-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="5ad1e-107">Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.</span><span class="sxs-lookup"><span data-stu-id="5ad1e-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ad1e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ad1e-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="5ad1e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ad1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ad1e-110">*vItem* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="5ad1e-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad1e-111">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5ad1e-111">Type: **Variant**</span></span>

<span data-ttu-id="5ad1e-112">Objeto [**FolderItem**](../shell/folderitem.md) para el que se creará el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="5ad1e-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="5ad1e-113">*vx* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5ad1e-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad1e-114">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5ad1e-114">Type: **Variant**</span></span>

<span data-ttu-id="5ad1e-115">Posición horizontal del menú, en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="5ad1e-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="5ad1e-116">*vy* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="5ad1e-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5ad1e-117">Tipo: **Variant**</span><span class="sxs-lookup"><span data-stu-id="5ad1e-117">Type: **Variant**</span></span>

<span data-ttu-id="5ad1e-118">Posición vertical del menú, en coordenadas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="5ad1e-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ad1e-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ad1e-119">Return value</span></span>

<span data-ttu-id="5ad1e-120">Tipo: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***</span><span class="sxs-lookup"><span data-stu-id="5ad1e-120">Type: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***</span></span>

<span data-ttu-id="5ad1e-121">Cuando este método vuelve, contiene la cadena de comando.</span><span class="sxs-lookup"><span data-stu-id="5ad1e-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="5ad1e-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5ad1e-122">Examples</span></span>

<span data-ttu-id="5ad1e-123">En el ejemplo siguiente se muestra el uso adecuado de **PopupItemMenu** para JScript insertado en HTML.</span><span class="sxs-lookup"><span data-stu-id="5ad1e-123">The following example shows the proper use of **PopupItemMenu** for JScript embedded in HTML.</span></span>


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="5ad1e-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ad1e-124">Requirements</span></span>



| <span data-ttu-id="5ad1e-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ad1e-125">Requirement</span></span> | <span data-ttu-id="5ad1e-126">Valor</span><span class="sxs-lookup"><span data-stu-id="5ad1e-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ad1e-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ad1e-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5ad1e-128">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="5ad1e-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5ad1e-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ad1e-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5ad1e-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5ad1e-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5ad1e-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ad1e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ad1e-132"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="5ad1e-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="5ad1e-133">Idl</span><span class="sxs-lookup"><span data-stu-id="5ad1e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ad1e-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ad1e-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="5ad1e-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ad1e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ad1e-136"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="5ad1e-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

