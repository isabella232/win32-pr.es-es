---
description: Mueve un elemento o elementos a esta carpeta.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Método Folder.MoveHere (Shldisp.h)
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
ms.openlocfilehash: eb826d23a168d81d838341e96fa5e613f8b6f5261a3cda548a2be320acebbde8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458923"
---
# <a name="foldermovehere-method"></a>Método Folder.MoveHere

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

*vItem* \[ En\]
</dt> <dd>

Tipo: **Variant**

Elemento o elementos que se moverá. Puede ser una cadena que representa un nombre de archivo, un [**objeto FolderItem**](folderitem.md) o [**un objeto FolderItems.**](folderitems.md)

</dd> <dt>

*vOptions* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Opciones para la operación de movimiento. Este valor puede ser cero o una combinación de los valores siguientes. Estos valores se basan en marcas definidas para su uso con el **miembro fFlags** de la estructura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) de C++. Estas marcas no se definen como tales para Visual Basic, VBScript o JScript, por lo que debe definirlas usted mismo o usar sus equivalentes numéricos.

<dt>



 (4)


</dt> <dd>

No mostrar un cuadro de diálogo de progreso.

</dd> <dt>



 (8)


</dt> <dd>

Asigne al archivo que se está operando con un nombre nuevo en una operación de movimiento, copia o cambio de nombre si ya existe un archivo con el nombre de destino.

</dd> <dt>



 (16)


</dt> <dd>

Responda con "Sí a todo" para cualquier cuadro de diálogo que se muestre.

</dd> <dt>



 (64)


</dt> <dd>

Conserve la información de deshacer, si es posible.

</dd> <dt>



 (128)


</dt> <dd>

Realice la operación en los archivos solo si se especifica un nombre de archivo comodín ( \* . \* ).

</dd> <dt>



 (256)


</dt> <dd>

Muestra un cuadro de diálogo de progreso, pero no muestra los nombres de archivo.

</dd> <dt>



 (512)


</dt> <dd>

No confirme la creación de un nuevo directorio si la operación requiere que se cree uno.

</dd> <dt>



 (1024)


</dt> <dd>

No muestre una interfaz de usuario si se produce un error.

</dd> <dt>



 (2048)


</dt> <dd>

[Versión 4.71.](versions.md) No copie los atributos de seguridad del archivo.

</dd> <dt>



 (4096)


</dt> <dd>

Solo funciona en el directorio local. No funcione de forma recursiva en subdirectorios.

</dd> <dt>



 (9182)


</dt> <dd>

[Versión 5.0.](versions.md) No mueva los archivos conectados como un grupo. Mueva solo los archivos especificados.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

> [!Note]  
> No todos los métodos se implementan para todas las carpetas. Por ejemplo, el [**método ParseName**](folder-parsename.md) no se implementa para la carpeta Panel de control (CSIDL \_ CONTROLS). Si intenta llamar a un método sin implementar, se 0x800A01BD error (decimal 445).

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se **usa MoveHere** para mover el archivo Temp.txt desde el directorio raíz de la unidad C a la Windows \\ C: . Se muestra un uso adecuado para JScript, VBScript y Visual Basic.

JScript:


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



Vbscript:


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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




