---
description: Mueve un elemento o elementos a esta carpeta.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Método Folder. MoveHere (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808035"
---
# <a name="foldermovehere-method"></a>Folder. MoveHere (método)

Mueve un elemento o elementos a esta carpeta.

## <a name="syntax"></a>Sintaxis


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vItem* \[ de\]
</dt> <dd>

Tipo: **variante**

Elemento o elementos que se van a desplace. Puede ser una cadena que representa un nombre de archivo, un objeto [**carpeta**](folderitem.md) o un objeto [**FolderItems**](folderitems.md) .

</dd> <dt>

*vOptions* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Opciones de la operación de movimiento. Este valor puede ser cero o una combinación de los siguientes valores. Estos valores se basan en marcas definidas para su uso con el miembro **fFlags** de la estructura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) de C++. Estas marcas no se definen como tales para Visual Basic, VBScript o JScript, por lo que debe definirlas usted mismo o usar sus equivalentes numéricos.

<dt>



 (4)


</dt> <dd>

No mostrar un cuadro de diálogo de progreso.

</dd> <dt>



 (8)


</dt> <dd>

Dé al archivo que opere con un nuevo nombre en una operación de movimiento, copia o cambio de nombre si ya existe un archivo con el nombre de destino.

</dd> <dt>



 (16)


</dt> <dd>

Responda con "sí a todo" para cualquier cuadro de diálogo que se muestre.

</dd> <dt>



 (64)


</dt> <dd>

Si es posible, conserve la información de deshacer.

</dd> <dt>



 (128)


</dt> <dd>

Realice la operación en archivos solo si se especifica un nombre de archivo comodín ( \* . \* ).

</dd> <dt>



 (256)


</dt> <dd>

Muestra un cuadro de diálogo de progreso pero no muestra los nombres de archivo.

</dd> <dt>



 (512)


</dt> <dd>

No confirme la creación de un directorio nuevo si la operación requiere que se cree uno.

</dd> <dt>



 (1024)


</dt> <dd>

No muestre una interfaz de usuario si se produce un error.

</dd> <dt>



 (2048)


</dt> <dd>

[Versión 4,71.](versions.md) No copie los atributos de seguridad del archivo.

</dd> <dt>



 (4096)


</dt> <dd>

Solo funciona en el directorio local. No opere de forma recursiva en subdirectorios.

</dd> <dt>



 (9182)


</dt> <dd>

[Versión 5,0.](versions.md) No mueva los archivos conectados como un grupo. Solo mueve los archivos especificados.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

> [!Note]  
> No todos los métodos se implementan para todas las carpetas. Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL). Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **MoveHere** para trasladar el archivo Temp.txt del directorio raíz de la unidad c a la \\ carpeta c: Windows. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
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
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 




