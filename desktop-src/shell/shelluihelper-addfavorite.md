---
description: Muestra la interfaz de usuario predeterminada para crear un elemento favorito. La interfaz de usuario se inicializa en los parámetros especificados.
title: Método ShellUIHelper.AddFavorite (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddFavorite
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b30e776e-642c-4599-b83f-ef15bc0b23d2
ms.openlocfilehash: 2ce6fa0a71bb2ab995e510f06b4403c78bebcc60
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842456"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="25493-104">Método ShellUIHelper.AddFavorite</span><span class="sxs-lookup"><span data-stu-id="25493-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="25493-105">Muestra la interfaz de usuario predeterminada para crear un elemento favorito.</span><span class="sxs-lookup"><span data-stu-id="25493-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="25493-106">La interfaz de usuario se inicializa en los parámetros especificados.</span><span class="sxs-lookup"><span data-stu-id="25493-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="25493-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="25493-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="25493-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="25493-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25493-109">*sURL* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="25493-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25493-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="25493-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="25493-111">Valor **string** que especifica la dirección URL del elemento que se va a agregar a la **carpeta Favoritos.**</span><span class="sxs-lookup"><span data-stu-id="25493-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="25493-112">*vTitle* \[ in, opcional\]</span><span class="sxs-lookup"><span data-stu-id="25493-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="25493-113">Tipo: **\* Variant**</span><span class="sxs-lookup"><span data-stu-id="25493-113">Type: **Variant\***</span></span>

<span data-ttu-id="25493-114">Valor **Variant** que especifica el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="25493-114">A **Variant** value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="25493-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="25493-115">Examples</span></span>

<span data-ttu-id="25493-116">En el ejemplo siguiente se muestra el uso adecuado de este método para JScript insertado en HTML y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="25493-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="25493-117">Jscript:</span><span class="sxs-lookup"><span data-stu-id="25493-117">JScript:</span></span>


```JScript
<html>
<head>
<title></title>

<object id="ShellUIHelper"
        classid="CLSID:64AB4BB7-111E-11d1-8F79-00C04FC2FBE1"
        width=0
        height=0
        VIEWASTEXT>
</object>

<script language="JavaScript">
    function fnShellUIHelperAddFavoriteJ()
    {
        ShellUIHelper.AddFavorite("https://www.msn.com", "MSN Home Page");
    }
</script>

</head>
<body onload=fnShellUIHelperAddFavoriteJ()>
</body>
</html>
```



<span data-ttu-id="25493-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="25493-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="25493-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25493-119">Requirements</span></span>



| <span data-ttu-id="25493-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="25493-120">Requirement</span></span> | <span data-ttu-id="25493-121">Value</span><span class="sxs-lookup"><span data-stu-id="25493-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25493-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25493-122">Minimum supported client</span></span><br/> | <span data-ttu-id="25493-123">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="25493-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="25493-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="25493-124">Minimum supported server</span></span><br/> | <span data-ttu-id="25493-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25493-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="25493-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25493-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="25493-127"><dt>Exdisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="25493-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="25493-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="25493-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25493-129"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="25493-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
