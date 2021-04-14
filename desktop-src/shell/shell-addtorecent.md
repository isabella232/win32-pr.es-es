---
description: Agrega un archivo a la lista de elementos usados más recientemente (MRU).
ms.assetid: 26D2AE5A-FC7E-4c7c-9F10-8D3D7AA236E7
title: Método Shell. AddToRecent (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.AddToRecent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c4372cc6cfac25f94e607f14734a9f544cd4fcbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986063"
---
# <a name="shelladdtorecent-method"></a><span data-ttu-id="1f2c6-103">Shell. AddToRecent (método)</span><span class="sxs-lookup"><span data-stu-id="1f2c6-103">Shell.AddToRecent method</span></span>

<span data-ttu-id="1f2c6-104">Agrega un archivo a la lista de elementos usados más recientemente (MRU).</span><span class="sxs-lookup"><span data-stu-id="1f2c6-104">Adds a file to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2c6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1f2c6-105">Syntax</span></span>


```JScript
Shell.AddToRecent(
  varFile,
  [ bstrCategory ]
)
```


```VB

Shell.AddToRecent( _
  ByVal varFile As Variant, _
  [ ByVal bstrCategory As BSTR ] _
)
```





## <a name="parameters"></a><span data-ttu-id="1f2c6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1f2c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f2c6-107">*varFile* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1f2c6-107">*varFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f2c6-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="1f2c6-108">Type: **Variant**</span></span>

<span data-ttu-id="1f2c6-109">**Cadena** que contiene la ruta de acceso del archivo que se va a agregar a la lista de documentos usados recientemente.</span><span class="sxs-lookup"><span data-stu-id="1f2c6-109">A **String** that contains the path of the file to add to the list of recently used documents.</span></span>

<span data-ttu-id="1f2c6-110">**Windows Vista**: establezca este parámetro en **null** para borrar la carpeta documentos recientes.</span><span class="sxs-lookup"><span data-stu-id="1f2c6-110">**Windows Vista**: Set this parameter to **null** to clear the recent documents folder.</span></span>

</dd> <dt>

<span data-ttu-id="1f2c6-111">*bstrCategory* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1f2c6-111">*bstrCategory* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1f2c6-112">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1f2c6-112">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1f2c6-113">**Cadena** que contiene el nombre de la categoría en la que se va a colocar el archivo.</span><span class="sxs-lookup"><span data-stu-id="1f2c6-113">A **String** that contains the name of the category in which to place the file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f2c6-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1f2c6-114">Return value</span></span>

### <a name="jscript"></a><span data-ttu-id="1f2c6-115">JScript</span><span class="sxs-lookup"><span data-stu-id="1f2c6-115">JScript</span></span>

<span data-ttu-id="1f2c6-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1f2c6-116">This method does not return a value.</span></span>

### <a name="vb"></a><span data-ttu-id="1f2c6-117">VB</span><span class="sxs-lookup"><span data-stu-id="1f2c6-117">VB</span></span>

<span data-ttu-id="1f2c6-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="1f2c6-118">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="1f2c6-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1f2c6-119">Examples</span></span>

<span data-ttu-id="1f2c6-120">En los siguientes ejemplos se muestra el uso de **AddToRecent** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="1f2c6-120">The following examples show the use of **AddToRecent** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="1f2c6-121">JScript.net</span><span class="sxs-lookup"><span data-stu-id="1f2c6-121">JScript:</span></span>


```JScript
<script language="JScript">
    function fnIShellDispatch3AddToRecentJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("system.ini");
            if (objFolderItem != null)
            {
                objShell.AddToRecent(objFolderItem.Path);
            }
        }
    }
</script>
```



<span data-ttu-id="1f2c6-122">VBScript</span><span class="sxs-lookup"><span data-stu-id="1f2c6-122">VBScript:</span></span>


```VB
<script language="VBScript">
     function fnIShellDispatch3AddToRecentVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
            
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder.ParseName("system.ini")
                if (not objFolderItem is nothing) then
                    objShell.AddToRecent (objFolderItem.Path)
                end if
                set objFolderItem = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



<span data-ttu-id="1f2c6-123">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="1f2c6-123">Visual Basic:</span></span>


```VB
Private Sub fnIShellDispatch3AddToRecent()
    Dim objShell  As Shell
    Dim objFolder As Folder
    Dim ssfWINDOWS As Long

    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem

        Set objFolderItem = objFolder.ParseName("system.ini")
        If (Not objFolderItem Is Nothing) Then
            objShell.AddToRecent (objFolderItem.Path)
        End If
        Set objFolderItem = Nothing
    End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="1f2c6-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f2c6-124">Requirements</span></span>



| <span data-ttu-id="1f2c6-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f2c6-125">Requirement</span></span> | <span data-ttu-id="1f2c6-126">Value</span><span class="sxs-lookup"><span data-stu-id="1f2c6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f2c6-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f2c6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="1f2c6-128">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="1f2c6-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="1f2c6-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1f2c6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="1f2c6-130">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="1f2c6-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1f2c6-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1f2c6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f2c6-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f2c6-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1f2c6-133">IDL</span><span class="sxs-lookup"><span data-stu-id="1f2c6-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f2c6-134"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f2c6-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1f2c6-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1f2c6-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f2c6-136"><dt>Shell32.dll (versión 6,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="1f2c6-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



 

 
