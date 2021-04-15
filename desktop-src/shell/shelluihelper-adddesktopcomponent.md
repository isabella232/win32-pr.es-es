---
description: Agrega un elemento a Microsoft Active Desktop.
title: Método ShellUIHelper. AddDesktopComponent (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellUIHelper.AddDesktopComponent
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 41634a89-15b9-41c8-ba3f-4bf19b786f6f
ms.openlocfilehash: d5234a0b43ea25c8ac931dc14ec90f7a6696ddfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985955"
---
# <a name="shelluihelperadddesktopcomponent-method"></a><span data-ttu-id="47240-103">ShellUIHelper. AddDesktopComponent, método</span><span class="sxs-lookup"><span data-stu-id="47240-103">ShellUIHelper.AddDesktopComponent method</span></span>

<span data-ttu-id="47240-104">Agrega un elemento a Microsoft Active Desktop.</span><span class="sxs-lookup"><span data-stu-id="47240-104">Adds an item to the Microsoft Active Desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="47240-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="47240-105">Syntax</span></span>


```JScript
iRetVal = ShellUIHelper.AddDesktopComponent(
  sURL,
  sType,
  [ Left ],
  [ Top ],
  [ Width ],
  [ Height ]
)
```



## <a name="parameters"></a><span data-ttu-id="47240-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="47240-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47240-107">*sURL* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47240-107">*sURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47240-108">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="47240-108">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="47240-109">Valor de **cadena** que especifica la dirección URL del nuevo elemento favorito.</span><span class="sxs-lookup"><span data-stu-id="47240-109">A **String** value that specifies the URL of the new favorite item.</span></span>

</dd> <dt>

<span data-ttu-id="47240-110">*SSE esperaba una* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="47240-110">*sType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47240-111">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="47240-111">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="47240-112">Valor de **cadena** que especifica el tipo de elemento que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="47240-112">A **String** value that specifies the type of item being added.</span></span> <span data-ttu-id="47240-113">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="47240-113">This can be one of the following values.</span></span>

<dt>



 <span data-ttu-id="47240-114">impresión</span><span class="sxs-lookup"><span data-stu-id="47240-114">(image)</span></span>


</dt> <dd>

<span data-ttu-id="47240-115">El componente es una imagen.</span><span class="sxs-lookup"><span data-stu-id="47240-115">The component is an image.</span></span>

</dd> <dt>



 <span data-ttu-id="47240-116">bsitio</span><span class="sxs-lookup"><span data-stu-id="47240-116">(website)</span></span>


</dt> <dd>

<span data-ttu-id="47240-117">El componente es un sitio Web.</span><span class="sxs-lookup"><span data-stu-id="47240-117">The component is a website.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="47240-118">*Izquierda* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="47240-118">*Left* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="47240-119">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="47240-119">Type: **Variant**</span></span>

<span data-ttu-id="47240-120">Posición del borde izquierdo del componente, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="47240-120">The position of the left edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="47240-121">*Parte superior* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="47240-121">*Top* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="47240-122">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="47240-122">Type: **Variant**</span></span>

<span data-ttu-id="47240-123">Posición del borde superior del componente, en coordenadas de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="47240-123">The position of the top edge of the component, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="47240-124">*Ancho* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="47240-124">*Width* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="47240-125">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="47240-125">Type: **Variant**</span></span>

<span data-ttu-id="47240-126">Ancho del componente, en unidades de pantalla.</span><span class="sxs-lookup"><span data-stu-id="47240-126">The width of the component, in screen units.</span></span>

</dd> <dt>

<span data-ttu-id="47240-127">*Alto* \[ de en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="47240-127">*Height* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="47240-128">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="47240-128">Type: **Variant**</span></span>

<span data-ttu-id="47240-129">Alto del componente, en unidades de pantalla.</span><span class="sxs-lookup"><span data-stu-id="47240-129">The height of the component, in screen units.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="47240-130">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="47240-130">Examples</span></span>

<span data-ttu-id="47240-131">En el ejemplo siguiente se muestra el uso correcto de este método para JScript incrustado en HTML y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="47240-131">The following example shows the proper usage of this method for JScript embedded in HTML and Visual Basic.</span></span>

<span data-ttu-id="47240-132">JScript.net</span><span class="sxs-lookup"><span data-stu-id="47240-132">JScript:</span></span>


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
    function fnShellUIHelperAddDesktopComponentJ()
    {
        ShellUIHelper.AddDesktopComponent("https://www.microsoft.com/", "website");
    }
</script>

</head>
<body onload=fnShellUIHelperAddDesktopComponentJ()>
</body>
</html>
```



<span data-ttu-id="47240-133">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="47240-133">Visual Basic:</span></span>


```VB
Private Sub fnShellUIHelperAddDesktopComponentVB()
    Dim objShellUIHelper As ShellUIHelper
    
    Set objShellUIHelper = New ShellUIHelper
        objShellUIHelper.AddDesktopComponent "https://www.microsoft.com/", "website"
    Set objShellUIHelper = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="47240-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="47240-134">Requirements</span></span>



| <span data-ttu-id="47240-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="47240-135">Requirement</span></span> | <span data-ttu-id="47240-136">Value</span><span class="sxs-lookup"><span data-stu-id="47240-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47240-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47240-137">Minimum supported client</span></span><br/> | <span data-ttu-id="47240-138">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="47240-138">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="47240-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="47240-139">Minimum supported server</span></span><br/> | <span data-ttu-id="47240-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="47240-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="47240-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47240-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="47240-142"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47240-142"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="47240-143">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="47240-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="47240-144"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="47240-144"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
