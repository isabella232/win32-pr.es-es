---
description: Recupera los detalles sobre un elemento de una carpeta. Por ejemplo, su tamaño, tipo o la hora de la última modificación.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Método Folder. GetDetailsOf (ShlObj \_ Core. h)
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
ms.openlocfilehash: 3ab89f00f254778a2417644d894f1e9e81eb43cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000857"
---
# <a name="foldergetdetailsof-method"></a>Folder. GetDetailsOf (método)

Recupera los detalles sobre un elemento de una carpeta. Por ejemplo, su tamaño, tipo o la hora de la última modificación.

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

Tipo: **variante**

Elemento para el que se va a recuperar la información. Debe ser un objeto [**carpeta**](folderitem.md) .

</dd> <dt>

*iColumn* 
</dt> <dd>

Tipo: **Integer**

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

Recupera la fecha y la hora en que se modificó el elemento por última vez.

</dd> <dt>



 (4)


</dt> <dd>

Recupera los atributos del elemento.

</dd> <dt>



 (-1)


</dt> <dd>

Recupera la información de información sobre herramientas para el elemento.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

Cadena que contiene los detalles recuperados.

## <a name="remarks"></a>Observaciones

> [!Note]  
> No todos los métodos se implementan para todas las carpetas. Por ejemplo, el método [_ *ParseName* *](folder-parsename.md) no está implementado para la carpeta panel de control ( \_ controles CSIDL). Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **GetDetailsOf** para recuperar el tipo del archivo denominado Clock.avi. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


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



VBScript


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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>ShlObj \_ Core. h (incluye Shldisp. h)</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 
