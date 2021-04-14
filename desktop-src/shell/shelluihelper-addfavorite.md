---
description: Muestra la interfaz de usuario predeterminada para crear un elemento favorito. La interfaz de usuario se inicializa con los parámetros especificados.
title: Método ShellUIHelper. AddFavorite (exdisp. h)
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
ms.openlocfilehash: a5c3cae52f0ad18c1f2ddf6cf91759d1c6daf6c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986022"
---
# <a name="shelluihelperaddfavorite-method"></a><span data-ttu-id="520ac-104">ShellUIHelper. AddFavorite, método</span><span class="sxs-lookup"><span data-stu-id="520ac-104">ShellUIHelper.AddFavorite method</span></span>

<span data-ttu-id="520ac-105">Muestra la interfaz de usuario predeterminada para crear un elemento favorito.</span><span class="sxs-lookup"><span data-stu-id="520ac-105">Displays the default user interface for creating a favorite item.</span></span> <span data-ttu-id="520ac-106">La interfaz de usuario se inicializa con los parámetros especificados.</span><span class="sxs-lookup"><span data-stu-id="520ac-106">The user interface is initialized to the specified parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="520ac-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="520ac-107">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddFavorite(
  sURL,
  [ vTitle ]
)
```



## <a name="parameters"></a><span data-ttu-id="520ac-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="520ac-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="520ac-109">*sURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="520ac-109">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="520ac-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="520ac-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="520ac-111">Valor de **cadena** que especifica la dirección URL del elemento que se va a agregar a la carpeta **Favoritos** .</span><span class="sxs-lookup"><span data-stu-id="520ac-111">A **String** value that specifies the URL of the item to be added to the **Favorites** folder.</span></span>

</dd> <dt>

<span data-ttu-id="520ac-112">*vTitle* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="520ac-112">*vTitle* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="520ac-113">Tipo: \**variante \** _</span><span class="sxs-lookup"><span data-stu-id="520ac-113">Type: \**Variant\** _</span></span>

<span data-ttu-id="520ac-114">Valor _ *Variant*\* que especifica el nombre del elemento.</span><span class="sxs-lookup"><span data-stu-id="520ac-114">A _ *Variant*\* value that specifies the name of the item.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="520ac-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="520ac-115">Examples</span></span>

<span data-ttu-id="520ac-116">En el ejemplo siguiente se muestra el uso correcto de este método para JScript incrustado en HTML y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="520ac-116">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="520ac-117">JScript.net</span><span class="sxs-lookup"><span data-stu-id="520ac-117">JScript:</span></span>


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



<span data-ttu-id="520ac-118">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="520ac-118">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddFavoriteVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddFavorite "https://www.msn.com", "MSN Home Page"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="520ac-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="520ac-119">Requirements</span></span>



| <span data-ttu-id="520ac-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="520ac-120">Requirement</span></span> | <span data-ttu-id="520ac-121">Value</span><span class="sxs-lookup"><span data-stu-id="520ac-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="520ac-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="520ac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="520ac-123">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="520ac-123">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="520ac-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="520ac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="520ac-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="520ac-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="520ac-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="520ac-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="520ac-127"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="520ac-127"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="520ac-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="520ac-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="520ac-129"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="520ac-129"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
