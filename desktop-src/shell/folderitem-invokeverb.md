---
description: Ejecuta un verbo en el elemento.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: Método carpeta. InvokeVerb (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 259ff9613756940d5da8a37585dbf39fb2dc0a26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539513"
---
# <a name="folderiteminvokeverb-method"></a><span data-ttu-id="41fcb-103">Carpeta. InvokeVerb, método</span><span class="sxs-lookup"><span data-stu-id="41fcb-103">FolderItem.InvokeVerb method</span></span>

<span data-ttu-id="41fcb-104">Ejecuta un verbo en el elemento.</span><span class="sxs-lookup"><span data-stu-id="41fcb-104">Executes a verb on the item.</span></span>

## <a name="syntax"></a><span data-ttu-id="41fcb-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41fcb-105">Syntax</span></span>


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a><span data-ttu-id="41fcb-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41fcb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41fcb-107">*vVerb* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="41fcb-107">*vVerb* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="41fcb-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="41fcb-108">Type: **Variant**</span></span>

<span data-ttu-id="41fcb-109">Cadena que especifica el verbo que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="41fcb-109">A string that specifies the verb to be executed.</span></span> <span data-ttu-id="41fcb-110">Debe ser uno de los valores devueltos por la propiedad [**FolderItemVerb.Name**](folderitemverb-name.md) del elemento.</span><span class="sxs-lookup"><span data-stu-id="41fcb-110">It must be one of the values returned by the item's [**FolderItemVerb.Name**](folderitemverb-name.md) property.</span></span> <span data-ttu-id="41fcb-111">Si no se especifica ningún verbo, se invocará el verbo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="41fcb-111">If no verb is specified, the default verb will be invoked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41fcb-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41fcb-112">Return value</span></span>

<span data-ttu-id="41fcb-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="41fcb-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="41fcb-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41fcb-114">Remarks</span></span>

<span data-ttu-id="41fcb-115">Un verbo es una cadena que se usa para especificar una acción determinada que admite un elemento.</span><span class="sxs-lookup"><span data-stu-id="41fcb-115">A verb is a string used to specify a particular action that an item supports.</span></span> <span data-ttu-id="41fcb-116">Invocar un verbo es equivalente a seleccionar un comando en el menú contextual de un elemento.</span><span class="sxs-lookup"><span data-stu-id="41fcb-116">Invoking a verb is equivalent to selecting a command from an item's shortcut menu.</span></span> <span data-ttu-id="41fcb-117">Normalmente, al invocar un verbo se inicia una aplicación relacionada.</span><span class="sxs-lookup"><span data-stu-id="41fcb-117">Typically, invoking a verb launches a related application.</span></span> <span data-ttu-id="41fcb-118">Por ejemplo, al invocar el verbo "abrir" en un archivo. txt, se abre el archivo con un editor de texto, normalmente el Bloc de notas de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="41fcb-118">For example, invoking the "open" verb on a .txt file opens the file with a text editor, usually Microsoft Notepad.</span></span> <span data-ttu-id="41fcb-119">Vea [iniciar aplicaciones](launch.md) para obtener más información sobre los verbos.</span><span class="sxs-lookup"><span data-stu-id="41fcb-119">See [Launching Applications](launch.md) for further discussion of verbs.</span></span>

<span data-ttu-id="41fcb-120">El objeto [**FolderItemVerbs**](folderitemverbs.md) representa la colección de verbos asociados al elemento.</span><span class="sxs-lookup"><span data-stu-id="41fcb-120">The [**FolderItemVerbs**](folderitemverbs.md) object represents the collection of verbs associated with the item.</span></span> <span data-ttu-id="41fcb-121">El verbo predeterminado puede variar para los distintos elementos, pero suele ser "Open".</span><span class="sxs-lookup"><span data-stu-id="41fcb-121">The default verb may vary for different items, but it is typically "open".</span></span>

## <a name="examples"></a><span data-ttu-id="41fcb-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="41fcb-122">Examples</span></span>

<span data-ttu-id="41fcb-123">En el ejemplo siguiente se usa **InvokeVerb** para invocar el verbo predeterminado ("Open" en este caso) en la carpeta Windows.</span><span class="sxs-lookup"><span data-stu-id="41fcb-123">The following example uses **InvokeVerb** to invoke the default verb ("open" in this case) on the Windows folder.</span></span> <span data-ttu-id="41fcb-124">Se muestra el uso correcto de JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="41fcb-124">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="41fcb-125">JScript.net</span><span class="sxs-lookup"><span data-stu-id="41fcb-125">JScript:</span></span>


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



<span data-ttu-id="41fcb-126">VBScript</span><span class="sxs-lookup"><span data-stu-id="41fcb-126">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="41fcb-127">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="41fcb-127">Visual Basic:</span></span>


```VB
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="41fcb-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41fcb-128">Requirements</span></span>



| <span data-ttu-id="41fcb-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="41fcb-129">Requirement</span></span> | <span data-ttu-id="41fcb-130">Value</span><span class="sxs-lookup"><span data-stu-id="41fcb-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41fcb-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41fcb-131">Minimum supported client</span></span><br/> | <span data-ttu-id="41fcb-132">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="41fcb-132">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="41fcb-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41fcb-133">Minimum supported server</span></span><br/> | <span data-ttu-id="41fcb-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41fcb-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="41fcb-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41fcb-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="41fcb-136"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="41fcb-136"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="41fcb-137">IDL</span><span class="sxs-lookup"><span data-stu-id="41fcb-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41fcb-138"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41fcb-138"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="41fcb-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41fcb-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41fcb-140"><dt>Shell32.dll (versión 4,71 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="41fcb-140"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41fcb-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="41fcb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41fcb-142">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="41fcb-142">**FolderItem**</span></span>](folderitem.md)
</dt> <dt>

[<span data-ttu-id="41fcb-143">**Verbos**</span><span class="sxs-lookup"><span data-stu-id="41fcb-143">**Verbs**</span></span>](folderitem-verbs.md)
</dt> <dt>

[<span data-ttu-id="41fcb-144">**DoIt**</span><span class="sxs-lookup"><span data-stu-id="41fcb-144">**DoIt**</span></span>](folderitemverb-doit.md)
</dt> </dl>

 

 




