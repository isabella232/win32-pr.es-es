---
<span data-ttu-id="d52e7-101">description: método Shell.FindComputer: "Muestra el cuadro de diálogo Resultados de la búsqueda: Equipos.</span><span class="sxs-lookup"><span data-stu-id="d52e7-101">description: Shell.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="d52e7-102">El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado."</span><span class="sxs-lookup"><span data-stu-id="d52e7-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="d52e7-103">ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="d52e7-103">ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="d52e7-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="d52e7-104">APIRef</span></span>
- <span data-ttu-id="d52e7-105">kbSyntax api_name:</span><span class="sxs-lookup"><span data-stu-id="d52e7-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="d52e7-106">Shell.FindComputer api_type:</span><span class="sxs-lookup"><span data-stu-id="d52e7-106">Shell.FindComputer api_type:</span></span> 
- <span data-ttu-id="d52e7-107">Com api_location:</span><span class="sxs-lookup"><span data-stu-id="d52e7-107">COM api_location:</span></span> 
- <span data-ttu-id="d52e7-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="d52e7-108">Shell32.dll</span></span>
---

# <a name="shellfindcomputer-method"></a><span data-ttu-id="d52e7-109">Método Shell.FindComputer</span><span class="sxs-lookup"><span data-stu-id="d52e7-109">Shell.FindComputer method</span></span>

<span data-ttu-id="d52e7-110">Muestra el cuadro **de diálogo Resultados de la búsqueda:** Equipos .</span><span class="sxs-lookup"><span data-stu-id="d52e7-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="d52e7-111">El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="d52e7-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d52e7-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d52e7-112">Syntax</span></span>


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="d52e7-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d52e7-113">Parameters</span></span>

<span data-ttu-id="d52e7-114">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d52e7-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d52e7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d52e7-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="d52e7-116">JScript</span><span class="sxs-lookup"><span data-stu-id="d52e7-116">JScript</span></span>

<span data-ttu-id="d52e7-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d52e7-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="d52e7-118">VB</span><span class="sxs-lookup"><span data-stu-id="d52e7-118">VB</span></span>

<span data-ttu-id="d52e7-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d52e7-119">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="d52e7-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d52e7-120">Examples</span></span>

<span data-ttu-id="d52e7-121">En el ejemplo siguiente se **muestra FindComputer** en uso.</span><span class="sxs-lookup"><span data-stu-id="d52e7-121">The following example shows **FindComputer** in use.</span></span> <span data-ttu-id="d52e7-122">El resultado de este código es  el mismo que al presionar el botón Inicio, hacer clic en **Buscar,** hacer clic en la opción Impresoras, equipos o personas y, a **continuación,** hacer clic en Un equipo de **la red.**</span><span class="sxs-lookup"><span data-stu-id="d52e7-122">The result of this code is the same as pressing the **Start** button, clicking **Search**, clicking the **Printers, computers, or people** option, then clicking **A computer on the network**.</span></span> <span data-ttu-id="d52e7-123">Se muestra un uso adecuado para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="d52e7-123">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="d52e7-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="d52e7-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



<span data-ttu-id="d52e7-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="d52e7-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="d52e7-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="d52e7-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="d52e7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d52e7-127">Requirements</span></span>



| <span data-ttu-id="d52e7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d52e7-128">Requirement</span></span> | <span data-ttu-id="d52e7-129">Valor</span><span class="sxs-lookup"><span data-stu-id="d52e7-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d52e7-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d52e7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d52e7-131">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="d52e7-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d52e7-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d52e7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d52e7-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d52e7-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d52e7-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d52e7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d52e7-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="d52e7-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="d52e7-136">Idl</span><span class="sxs-lookup"><span data-stu-id="d52e7-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d52e7-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="d52e7-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="d52e7-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d52e7-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d52e7-139"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="d52e7-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




