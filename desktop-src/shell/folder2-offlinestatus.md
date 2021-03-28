---
description: Contiene el estado sin conexión de la carpeta.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Propiedad Carpeta2. OfflineStatus (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984195"
---
# <a name="folder2offlinestatus-property"></a><span data-ttu-id="6a20a-103">Propiedad Carpeta2. OfflineStatus</span><span class="sxs-lookup"><span data-stu-id="6a20a-103">Folder2.OfflineStatus property</span></span>

<span data-ttu-id="6a20a-104">Contiene el estado sin conexión de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="6a20a-104">Contains the offline status of the folder.</span></span>

<span data-ttu-id="6a20a-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6a20a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a20a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a20a-106">Syntax</span></span>


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a><span data-ttu-id="6a20a-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6a20a-107">Property value</span></span>

<span data-ttu-id="6a20a-108">Un **entero** que se establece en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6a20a-108">An **Integer** that is set to one of the following values.</span></span>

<dt>



 <span data-ttu-id="6a20a-109">(OFS \_ DIRTYCACHE)</span><span class="sxs-lookup"><span data-stu-id="6a20a-109">(OFS\_DIRTYCACHE)</span></span>


</dt> <dd>

<span data-ttu-id="6a20a-110">El servidor está en línea con cambios no sincronizados.</span><span class="sxs-lookup"><span data-stu-id="6a20a-110">Server is online with unsynchronized changes.</span></span>

</dd> <dt>



 <span data-ttu-id="6a20a-111">(OFS \_ INACTIVA</span><span class="sxs-lookup"><span data-stu-id="6a20a-111">(OFS\_INACTIVE)</span></span>


</dt> <dd>

<span data-ttu-id="6a20a-112">No se ha habilitado el almacenamiento en caché sin conexión para esta carpeta.</span><span class="sxs-lookup"><span data-stu-id="6a20a-112">Offline caching is not enabled for this folder.</span></span>

</dd> <dt>



 <span data-ttu-id="6a20a-113">(OFS \_ N</span><span class="sxs-lookup"><span data-stu-id="6a20a-113">(OFS\_OFFLINE)</span></span>


</dt> <dd>

<span data-ttu-id="6a20a-114">El servidor está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="6a20a-114">Server is offline.</span></span>

</dd> <dt>



 <span data-ttu-id="6a20a-115">(OFS \_ PANTALLA</span><span class="sxs-lookup"><span data-stu-id="6a20a-115">(OFS\_ONLINE)</span></span>


</dt> <dd>

<span data-ttu-id="6a20a-116">El servidor está en línea.</span><span class="sxs-lookup"><span data-stu-id="6a20a-116">Server is online.</span></span>

</dd> <dt>



 <span data-ttu-id="6a20a-117">(OFS \_ SERVERBACK)</span><span class="sxs-lookup"><span data-stu-id="6a20a-117">(OFS\_SERVERBACK)</span></span>


</dt> <dd>

<span data-ttu-id="6a20a-118">El servidor está sin conexión, pero se puede acceder a él.</span><span class="sxs-lookup"><span data-stu-id="6a20a-118">Server is offline but can be reached.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a20a-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a20a-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6a20a-120">Archivos sin conexión debe habilitarse a través de opciones de carpeta para que **OfflineStatus** funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="6a20a-120">Offline Files must be enabled through Folder Options for **OfflineStatus** to work correctly.</span></span> <span data-ttu-id="6a20a-121">Si la opción Archivos sin conexión no está habilitada, la propiedad devuelve **OFS \_ Inactive**.</span><span class="sxs-lookup"><span data-stu-id="6a20a-121">If the Offline Files option is not enabled, the property returns **OFS\_INACTIVE**.</span></span>

 

## <a name="examples"></a><span data-ttu-id="6a20a-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6a20a-122">Examples</span></span>

<span data-ttu-id="6a20a-123">En el ejemplo siguiente se muestra el uso correcto de **OfflineStatus** para JScript, VBScript y Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6a20a-123">The following example shows the proper use of **OfflineStatus** for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="6a20a-124">JScript.net</span><span class="sxs-lookup"><span data-stu-id="6a20a-124">JScript:</span></span>


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



<span data-ttu-id="6a20a-125">VBScript</span><span class="sxs-lookup"><span data-stu-id="6a20a-125">VBScript:</span></span>


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



<span data-ttu-id="6a20a-126">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="6a20a-126">Visual Basic:</span></span>


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a><span data-ttu-id="6a20a-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a20a-127">Requirements</span></span>



| <span data-ttu-id="6a20a-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a20a-128">Requirement</span></span> | <span data-ttu-id="6a20a-129">Value</span><span class="sxs-lookup"><span data-stu-id="6a20a-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a20a-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a20a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6a20a-131">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="6a20a-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a20a-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a20a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6a20a-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="6a20a-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6a20a-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a20a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a20a-135"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a20a-135"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="6a20a-136">IDL</span><span class="sxs-lookup"><span data-stu-id="6a20a-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6a20a-137"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6a20a-137"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="6a20a-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a20a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a20a-139"><dt>Shell32.dll (versión 5,0 o posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="6a20a-139"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a20a-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a20a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a20a-141">**Carpeta2**</span><span class="sxs-lookup"><span data-stu-id="6a20a-141">**Folder2**</span></span>](folder2-object.md)
</dt> <dt>

[<span data-ttu-id="6a20a-142">**Carpeta**</span><span class="sxs-lookup"><span data-stu-id="6a20a-142">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




