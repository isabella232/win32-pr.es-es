---
<span data-ttu-id="851f3-101">description: método IShellDispatch.FindComputer: "Muestra los resultados de la búsqueda: equipos .</span><span class="sxs-lookup"><span data-stu-id="851f3-101">description: IShellDispatch.FindComputer method - 'Displays the Search Results: Computers dialog box.</span></span> <span data-ttu-id="851f3-102">El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado."</span><span class="sxs-lookup"><span data-stu-id="851f3-102">The dialog box shows the result of the search for a specified computer.'</span></span>
<span data-ttu-id="851f3-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span><span class="sxs-lookup"><span data-stu-id="851f3-103">ms.assetid: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 title: IShellDispatch.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type:</span></span> 
- <span data-ttu-id="851f3-104">APIRef</span><span class="sxs-lookup"><span data-stu-id="851f3-104">APIRef</span></span>
- <span data-ttu-id="851f3-105">kbSyntax api_name:</span><span class="sxs-lookup"><span data-stu-id="851f3-105">kbSyntax api_name:</span></span> 
- <span data-ttu-id="851f3-106">IShellDispatch.FindComputer api_type:</span><span class="sxs-lookup"><span data-stu-id="851f3-106">IShellDispatch.FindComputer api_type:</span></span> 
- <span data-ttu-id="851f3-107">Com api_location:</span><span class="sxs-lookup"><span data-stu-id="851f3-107">COM api_location:</span></span> 
- <span data-ttu-id="851f3-108">Shell32.dll</span><span class="sxs-lookup"><span data-stu-id="851f3-108">Shell32.dll</span></span>
---

# <a name="ishelldispatchfindcomputer-method"></a><span data-ttu-id="851f3-109">Método IShellDispatch.FindComputer</span><span class="sxs-lookup"><span data-stu-id="851f3-109">IShellDispatch.FindComputer method</span></span>

<span data-ttu-id="851f3-110">Muestra el cuadro **de diálogo Resultados de la búsqueda:** Equipos.</span><span class="sxs-lookup"><span data-stu-id="851f3-110">Displays the **Search Results: Computers** dialog box.</span></span> <span data-ttu-id="851f3-111">El cuadro de diálogo muestra el resultado de la búsqueda de un equipo especificado.</span><span class="sxs-lookup"><span data-stu-id="851f3-111">The dialog box shows the result of the search for a specified computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="851f3-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="851f3-112">Syntax</span></span>


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a><span data-ttu-id="851f3-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="851f3-113">Parameters</span></span>

<span data-ttu-id="851f3-114">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="851f3-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="851f3-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="851f3-115">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="851f3-116">JScript</span><span class="sxs-lookup"><span data-stu-id="851f3-116">JScript</span></span>

<span data-ttu-id="851f3-117">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="851f3-117">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="851f3-118">VB</span><span class="sxs-lookup"><span data-stu-id="851f3-118">VB</span></span>

<span data-ttu-id="851f3-119">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="851f3-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="851f3-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="851f3-120">Remarks</span></span>

<span data-ttu-id="851f3-121">Este método se implementa y se accede a través del [**método Shell.FindComputer.**](shell-findcomputer.md)</span><span class="sxs-lookup"><span data-stu-id="851f3-121">This method is implemented and accessed through the [**Shell.FindComputer**](shell-findcomputer.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="851f3-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="851f3-122">Examples</span></span>

<span data-ttu-id="851f3-123">En los ejemplos siguientes se muestra el uso **de FindComputer** en JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="851f3-123">The following examples show the use of **FindComputer** in JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="851f3-124">Jscript:</span><span class="sxs-lookup"><span data-stu-id="851f3-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
    }
</script>
```



<span data-ttu-id="851f3-125">Vbscript:</span><span class="sxs-lookup"><span data-stu-id="851f3-125">VBScript:</span></span>


```VB
 <script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="851f3-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="851f3-126">Visual Basic:</span></span>


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="851f3-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="851f3-127">Requirements</span></span>



| <span data-ttu-id="851f3-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="851f3-128">Requirement</span></span> | <span data-ttu-id="851f3-129">Valor</span><span class="sxs-lookup"><span data-stu-id="851f3-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="851f3-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="851f3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="851f3-131">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="851f3-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="851f3-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="851f3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="851f3-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="851f3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="851f3-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="851f3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="851f3-135"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="851f3-135"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="851f3-136">Idl</span><span class="sxs-lookup"><span data-stu-id="851f3-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="851f3-137"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="851f3-137"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="851f3-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="851f3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="851f3-139"><dt>Shell32.dll (versión 4.71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="851f3-139"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




