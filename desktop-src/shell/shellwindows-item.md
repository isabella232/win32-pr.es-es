---
description: Recupera un objeto InternetExplorer que representa la ventana del shell.
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: Método ShellWindows. Item (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ccdb73deb1d97d9c6e1ad8c335db3c58d796a299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277223"
---
# <a name="shellwindowsitem-method"></a><span data-ttu-id="692cb-103">ShellWindows. Item (método)</span><span class="sxs-lookup"><span data-stu-id="692cb-103">ShellWindows.Item method</span></span>

<span data-ttu-id="692cb-104">Recupera un objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa la ventana del shell.</span><span class="sxs-lookup"><span data-stu-id="692cb-104">Retrieves an [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="syntax"></a><span data-ttu-id="692cb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="692cb-105">Syntax</span></span>


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a><span data-ttu-id="692cb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="692cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="692cb-107">*iIndex* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="692cb-107">*iIndex* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="692cb-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="692cb-108">Type: **Variant**</span></span>

<span data-ttu-id="692cb-109">Índice de base cero del elemento que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="692cb-109">The zero-based index of the item to retrieve.</span></span> <span data-ttu-id="692cb-110">Este valor debe ser menor que el valor de la propiedad [**Count**](shellwindows-count.md) .</span><span class="sxs-lookup"><span data-stu-id="692cb-110">This value must be less than the value of the [**Count**](shellwindows-count.md) property.</span></span> <span data-ttu-id="692cb-111">Si se omite este valor, se usa un valor predeterminado de 0.</span><span class="sxs-lookup"><span data-stu-id="692cb-111">If this value is omitted, a default value of 0 is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="692cb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="692cb-112">Return value</span></span>

<span data-ttu-id="692cb-113">Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span><span class="sxs-lookup"><span data-stu-id="692cb-113">Type: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***</span></span>

<span data-ttu-id="692cb-114">Una referencia de objeto al objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa la ventana de Shell.</span><span class="sxs-lookup"><span data-stu-id="692cb-114">An object reference to the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the Shell window.</span></span>

## <a name="examples"></a><span data-ttu-id="692cb-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="692cb-115">Examples</span></span>

<span data-ttu-id="692cb-116">En el ejemplo siguiente se usa [**Item**](folderitemverbs-item.md) para recuperar el objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa el primer elemento de la ventana de Shell.</span><span class="sxs-lookup"><span data-stu-id="692cb-116">The following example uses [**Item**](folderitemverbs-item.md) to retrieve the [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) object that represents the first Shell window item.</span></span> <span data-ttu-id="692cb-117">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="692cb-117">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="692cb-118">JScript.net</span><span class="sxs-lookup"><span data-stu-id="692cb-118">JScript:</span></span>


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



<span data-ttu-id="692cb-119">VBScript</span><span class="sxs-lookup"><span data-stu-id="692cb-119">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="692cb-120">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="692cb-120">Visual Basic:</span></span>


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="692cb-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="692cb-121">Requirements</span></span>



| <span data-ttu-id="692cb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="692cb-122">Requirement</span></span> | <span data-ttu-id="692cb-123">Value</span><span class="sxs-lookup"><span data-stu-id="692cb-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="692cb-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="692cb-124">Minimum supported client</span></span><br/> | <span data-ttu-id="692cb-125">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="692cb-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="692cb-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="692cb-126">Minimum supported server</span></span><br/> | <span data-ttu-id="692cb-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="692cb-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="692cb-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="692cb-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="692cb-129"><dt>Exdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="692cb-129"><dt>Exdisp.h</dt></span></span> </dl>                            |
| <span data-ttu-id="692cb-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="692cb-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="692cb-131"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="692cb-131"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 
