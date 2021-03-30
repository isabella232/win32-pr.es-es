---
title: Método WebViewFolderContents. PopupItemMenu (Shldisp. h)
description: Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Método PopupItemMenu características del entorno heredado de Windows
- Método PopupItemMenu características de entorno heredado de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredado, método PopupItemMenu
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
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801244"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a><span data-ttu-id="2b334-106">WebViewFolderContents. PopupItemMenu, método</span><span class="sxs-lookup"><span data-stu-id="2b334-106">WebViewFolderContents.PopupItemMenu method</span></span>

<span data-ttu-id="2b334-107">Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.</span><span class="sxs-lookup"><span data-stu-id="2b334-107">Creates a shortcut menu for the specified item and returns the selected command string.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b334-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2b334-108">Syntax</span></span>


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a><span data-ttu-id="2b334-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2b334-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b334-110">*vItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2b334-110">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b334-111">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="2b334-111">Type: **Variant**</span></span>

<span data-ttu-id="2b334-112">Objeto [**carpeta**](../shell/folderitem.md) para el que se creará el menú contextual.</span><span class="sxs-lookup"><span data-stu-id="2b334-112">The [**FolderItem**](../shell/folderitem.md) object for which the shortcut menu will be created.</span></span>

</dd> <dt>

<span data-ttu-id="2b334-113">*VX* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2b334-113">*vx* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2b334-114">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="2b334-114">Type: **Variant**</span></span>

<span data-ttu-id="2b334-115">Posición horizontal del menú, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2b334-115">The horizontal position of the menu, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="2b334-116">*VY* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="2b334-116">*vy* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2b334-117">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="2b334-117">Type: **Variant**</span></span>

<span data-ttu-id="2b334-118">Posición vertical del menú, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2b334-118">The vertical position of the menu, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b334-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2b334-119">Return value</span></span>

<span data-ttu-id="2b334-120">Tipo: \**[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _</span><span class="sxs-lookup"><span data-stu-id="2b334-120">Type: \**[BSTR](/previous-versions/windows/desktop/automat/bstr)\** _</span></span>

<span data-ttu-id="2b334-121">Cuando este método devuelve un valor, contiene la cadena de comando.</span><span class="sxs-lookup"><span data-stu-id="2b334-121">When this method returns, contains the command string.</span></span>

## <a name="examples"></a><span data-ttu-id="2b334-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2b334-122">Examples</span></span>

<span data-ttu-id="2b334-123">En el ejemplo siguiente se muestra el uso correcto de _ *PopupItemMenu*\* para JScript Embedded en HTML.</span><span class="sxs-lookup"><span data-stu-id="2b334-123">The following example shows the proper use of _ *PopupItemMenu*\* for JScript embedded in HTML.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2b334-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b334-124">Requirements</span></span>



| <span data-ttu-id="2b334-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b334-125">Requirement</span></span> | <span data-ttu-id="2b334-126">Value</span><span class="sxs-lookup"><span data-stu-id="2b334-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b334-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b334-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2b334-128">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2b334-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2b334-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2b334-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2b334-130">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2b334-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b334-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2b334-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b334-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b334-132"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2b334-133">IDL</span><span class="sxs-lookup"><span data-stu-id="2b334-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b334-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b334-134"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2b334-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2b334-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b334-136"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2b334-136"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

