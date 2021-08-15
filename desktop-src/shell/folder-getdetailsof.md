---
description: Recupera detalles sobre un elemento de una carpeta. Por ejemplo, su tamaño, tipo o la hora de su última modificación.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Método Folder.GetDetailsOf (Shlobj \_ core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c703150069bc839f2d20024c0de8f3197fba09c5c3571e3de818dec3f3d6737c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860333"
---
# <a name="foldergetdetailsof-method"></a>Método Folder.GetDetailsOf

Recupera detalles sobre un elemento de una carpeta. Por ejemplo, su tamaño, tipo o la hora de su última modificación.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vItem* 
</dt> <dd>

Tipo: **Variant**

Elemento para el que se va a recuperar la información. Debe ser un [**objeto FolderItem.**](folderitem.md)

</dd> <dt>

*iColumn* 
</dt> <dd>

Tipo: **Entero**

Valor **entero** que especifica la información que se va a recuperar. La información disponible para un elemento depende de la carpeta en la que se muestra. Este valor corresponde al número de columna de base cero que se muestra en una vista de Shell. Para un elemento del sistema de archivos, puede ser uno de los siguientes valores:

<dt>



  (0)


</dt> <dd>

Recupera el nombre del elemento.

</dd> <dt>



 (1)


</dt> <dd>

Recupera el tamaño del elemento.

</dd> <dt>



 (2)


</dt> <dd>

Recupera el tipo del elemento.

</dd> <dt>



 (3)


</dt> <dd>

Recupera la fecha y hora en que se modificó por última vez el elemento.

</dd> <dt>



 (4)


</dt> <dd>

Recupera los atributos del elemento.

</dd> <dt>



 (-1)


</dt> <dd>

Recupera la información de información del elemento.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

Cadena que contiene el detalle recuperado.

## <a name="remarks"></a>Comentarios

> [!Note]  
> No todos los métodos se implementan para todas las carpetas. Por ejemplo, el [**método ParseName**](folder-parsename.md) no se implementa para la carpeta Panel de control (CSIDL \_ CONTROLS). Si intenta llamar a un método sin implementar, se 0x800A01BD error (decimal 445).

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa GetDetailsOf** para recuperar el tipo del archivo denominado Clock.avi. Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
            end if
            
            set objFolderItem = nothing
        end if
        
        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
    End If
    
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shlobj \_ core.h (incluir Shldisp.h)</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
