---
description: Se llama en respuesta a la vista Web Barricade que el usuario está descartando.
ms.assetid: 170893b6-c947-45b1-b717-a93a0b083bda
title: Método Carpeta2. DismissedWebViewBarricade (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.DismissedWebViewBarricade
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: cdedc7292b0dd52ca903b944993e32df1ec2c3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156480"
---
# <a name="folder2dismissedwebviewbarricade-method"></a><span data-ttu-id="2943f-103">Carpeta2. DismissedWebViewBarricade (método)</span><span class="sxs-lookup"><span data-stu-id="2943f-103">Folder2.DismissedWebViewBarricade method</span></span>

<span data-ttu-id="2943f-104">Se llama en respuesta a la vista Web Barricade que el usuario está descartando.</span><span class="sxs-lookup"><span data-stu-id="2943f-104">Called in response to the web view barricade being dismissed by the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="2943f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2943f-105">Syntax</span></span>


```JScript
Folder2.DismissedWebViewBarricade()
```



## <a name="parameters"></a><span data-ttu-id="2943f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2943f-106">Parameters</span></span>

<span data-ttu-id="2943f-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="2943f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2943f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2943f-108">Return value</span></span>

<span data-ttu-id="2943f-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="2943f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2943f-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2943f-110">Remarks</span></span>

<span data-ttu-id="2943f-111">Una aplicación llama a este método después de que el usuario descarte la vista Web Barricade.</span><span class="sxs-lookup"><span data-stu-id="2943f-111">An application calls this method after the user dismisses the web view barricade.</span></span>

## <a name="examples"></a><span data-ttu-id="2943f-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2943f-112">Examples</span></span>

<span data-ttu-id="2943f-113">En el ejemplo siguiente se usa **DismissedWebViewBarricade** para especificar que se ha descartado la vista Web Barricade para la carpeta C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="2943f-113">The following example uses **DismissedWebViewBarricade** to specify that the web view barricade for the C:\\Windows folder has been dismissed.</span></span> <span data-ttu-id="2943f-114">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2943f-114">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2943f-115">JScript.net</span><span class="sxs-lookup"><span data-stu-id="2943f-115">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolder2ObjectDismissedWebViewBarricadeJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder2 != null)
        {
            objFolder2.DismissedWebViewBarricade();
        }
    }
</script>
```



<span data-ttu-id="2943f-116">VBScript</span><span class="sxs-lookup"><span data-stu-id="2943f-116">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolder2ObjectDismissedWebViewBarricadeVB()
        dim objShell
        dim objFolder2

        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder2 is nothing) then
            objFolder2.DismissedWebViewBarricade()
        end if

        set objFolder2 = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="2943f-117">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2943f-117">Visual Basic:</span></span>


```VB
Private Sub btnDismissedWebViewBarricade_Click()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2

    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder2 Is Nothing) Then
        objFolder2.DismissedWebViewBarricade
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="2943f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2943f-118">Requirements</span></span>



| <span data-ttu-id="2943f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2943f-119">Requirement</span></span> | <span data-ttu-id="2943f-120">Value</span><span class="sxs-lookup"><span data-stu-id="2943f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2943f-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2943f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2943f-122">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="2943f-122">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2943f-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2943f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2943f-124">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="2943f-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2943f-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2943f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2943f-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2943f-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="2943f-127">IDL</span><span class="sxs-lookup"><span data-stu-id="2943f-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2943f-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2943f-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="2943f-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2943f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2943f-130"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2943f-130"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2943f-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="2943f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2943f-132">**Carpeta2**</span><span class="sxs-lookup"><span data-stu-id="2943f-132">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="2943f-133">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="2943f-133">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




