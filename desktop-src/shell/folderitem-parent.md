---
description: Obtiene un objeto que representa el elemento primario del elemento.
ms.assetid: 612e76d8-d8bc-419c-b319-75b1f324840a
title: Propiedad carpeta. Parent (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Parent
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: f2da3504596c3b351318b33c929dad3b5a958165
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808023"
---
# <a name="folderitemparent-property"></a>Carpeta. Parent (propiedad)

Obtiene un objeto que representa el elemento primario del elemento.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objParent = FolderItem.Parent
```



## <a name="property-value"></a>Valor de propiedad

Variable de tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recibe el objeto primario.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de los **elementos primarios** para JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



VBScript


```VB
 <script language="VBScript">
    function fnFolderItemParentVB()
        dim objShell
        dim objFolder2
        dim ssfWINDOWS

        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem

                set objFolderItem = objFolder2.Self
                    if (not objFolderItem is nothing) then
                        dim objParent

                        set objParent = objFolderItem.Parent
                            if (not objParent is nothing) then
                                alert("Got parent object")
                            end if
                        set objParent = nothing
                    end if
                set objFolderItem = nothing
            end if
        set objFolder2 = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
<script language="JScript">
    function fnFolderItemParentJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;

        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;

            objFolderItem = objFolder2.Self;
            {
                var objParent;

                objParent = objFolderItem.Parent;
                if (objParent != null)
                {
                    alert("Got parent object");
                }
            }
        }
    }
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 
