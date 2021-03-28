---
description: Obtiene un conjunto de marcas que indican las opciones actuales de la vista.
ms.assetid: 83a17033-bd7f-44de-a0c8-460d12c4825d
title: Propiedad ShellFolderView. ViewOptions (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.ViewOptions
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e336034e7d5037b8037c6fd0ef549fe5f87da312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997864"
---
# <a name="shellfolderviewviewoptions-property"></a><span data-ttu-id="c8203-103">Propiedad ShellFolderView. ViewOptions</span><span class="sxs-lookup"><span data-stu-id="c8203-103">ShellFolderView.ViewOptions property</span></span>

<span data-ttu-id="c8203-104">Obtiene un conjunto de marcas que indican las opciones actuales de la vista.</span><span class="sxs-lookup"><span data-stu-id="c8203-104">Gets a set of flags that indicate the current options of the view.</span></span>

<span data-ttu-id="c8203-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c8203-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8203-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8203-106">Syntax</span></span>


```JScript
objViewOptions = ShellFolderView.ViewOptions
```



## <a name="property-value"></a><span data-ttu-id="c8203-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c8203-107">Property value</span></span>

<span data-ttu-id="c8203-108">Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de opciones de vista.</span><span class="sxs-lookup"><span data-stu-id="c8203-108">A variable of type [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) that receives the view options object.</span></span> <span data-ttu-id="c8203-109">Contiene uno o varios de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="c8203-109">Contains one or more of the following values:</span></span>

<dt>

<span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>

<span data-ttu-id="c8203-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO \_ SHOWALLOBJECTS** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="c8203-110"><span id="SFVVO_SHOWALLOBJECTS"></span><span id="sfvvo_showallobjects"></span>**SFVVO\_SHOWALLOBJECTS** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="c8203-111">La opción **Mostrar todos los archivos** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="c8203-111">The **Show All Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>

<span data-ttu-id="c8203-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO \_ SHOWEXTENSIONS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="c8203-112"><span id="SFVVO_SHOWEXTENSIONS"></span><span id="sfvvo_showextensions"></span>**SFVVO\_SHOWEXTENSIONS** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="c8203-113">La opción **Ocultar extensiones para tipos de archivo conocidos** está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="c8203-113">The **Hide extensions for known file types** option is disabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>

<span data-ttu-id="c8203-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO \_ SHOWCOMPCOLOR** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="c8203-114"><span id="SFVVO_SHOWCOMPCOLOR"></span><span id="sfvvo_showcompcolor"></span>**SFVVO\_SHOWCOMPCOLOR** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="c8203-115">La opción **Mostrar los archivos comprimidos y las carpetas con un color alternativo** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="c8203-115">The **Display Compressed Files and Folders with Alternate Color** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>

<span data-ttu-id="c8203-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO \_ SHOWSYSFILES** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="c8203-116"><span id="SFVVO_SHOWSYSFILES"></span><span id="sfvvo_showsysfiles"></span>**SFVVO\_SHOWSYSFILES** (0x00000020)</span></span>


</dt> <dd>

<span data-ttu-id="c8203-117">La opción no **Mostrar archivos ocultos** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="c8203-117">The **Do Not Show Hidden Files** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>

<span data-ttu-id="c8203-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO \_ WIN95CLASSIC** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="c8203-118"><span id="SFVVO_WIN95CLASSIC"></span><span id="sfvvo_win95classic"></span>**SFVVO\_WIN95CLASSIC** (0x00000040)</span></span>


</dt> <dd>

<span data-ttu-id="c8203-119">La opción de **estilo clásico** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="c8203-119">The **Classic Style** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>

<span data-ttu-id="c8203-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO \_ DOUBLECLICKINWEBVIEW** (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="c8203-120"><span id="SFVVO_DOUBLECLICKINWEBVIEW"></span><span id="sfvvo_doubleclickinwebview"></span>**SFVVO\_DOUBLECLICKINWEBVIEW** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="c8203-121">La opción hacer **doble clic para abrir un elemento** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="c8203-121">The **Double-Click to Open an Item** option is enabled.</span></span>

</dd> <dt>

<span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>

<span data-ttu-id="c8203-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO \_ DESKTOPHTML** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="c8203-122"><span id="SFVVO_DESKTOPHTML"></span><span id="sfvvo_desktophtml"></span>**SFVVO\_DESKTOPHTML** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="c8203-123">La opción **Active Desktop: ver como página web** está habilitada.</span><span class="sxs-lookup"><span data-stu-id="c8203-123">The **Active Desktop – View as Web Page** option is enabled.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c8203-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8203-124">Remarks</span></span>

<span data-ttu-id="c8203-125">Solo se puede llamar a [**FocusedItem**](shellfolderview-focuseditem.md) en el sistema local.</span><span class="sxs-lookup"><span data-stu-id="c8203-125">[**FocusedItem**](shellfolderview-focuseditem.md) can only be called on the local system.</span></span> <span data-ttu-id="c8203-126">No funcionará cuando se ejecute en una página web a través de HTTP o UNC.</span><span class="sxs-lookup"><span data-stu-id="c8203-126">It will not work when run on a webpage over HTTP or UNC.</span></span>

## <a name="examples"></a><span data-ttu-id="c8203-127">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c8203-127">Examples</span></span>

<span data-ttu-id="c8203-128">En el ejemplo siguiente se muestra el uso correcto de este método en JScript incrustado en HTML.</span><span class="sxs-lookup"><span data-stu-id="c8203-128">The following example shows the proper use of this method in JScript embedded in HTML.</span></span>


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewViewOptionsJ()
    {
        var objOptions;
        
        objOptions = WebOC.Document.ViewOptions;
        if (objOptions != null)
        {
            alert(objOptions);
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC"
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400>
</object>
<br><br>
<INPUT id=ViewOptions 
       type=button 
       value=ViewOptions 
       name=ViewOptions 
       onclick="fnShellFolderViewViewOptionsJ()">
</body>
</html>
```



## <a name="requirements"></a><span data-ttu-id="c8203-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8203-129">Requirements</span></span>



| <span data-ttu-id="c8203-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8203-130">Requirement</span></span> | <span data-ttu-id="c8203-131">Value</span><span class="sxs-lookup"><span data-stu-id="c8203-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8203-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8203-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c8203-133">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="c8203-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c8203-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8203-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c8203-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="c8203-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c8203-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c8203-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8203-137"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8203-137"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="c8203-138">IDL</span><span class="sxs-lookup"><span data-stu-id="c8203-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c8203-139"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c8203-139"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="c8203-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8203-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8203-141"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c8203-141"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
