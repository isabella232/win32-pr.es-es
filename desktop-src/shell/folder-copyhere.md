---
description: Copia un elemento o elementos en una carpeta.
title: Método Folder. CopyHere (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: ac616aa88cfb0ad6742c6037ec28e8b93ff1a4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997736"
---
# <a name="foldercopyhere-method"></a>Folder. CopyHere (método)

Copia un elemento o elementos en una carpeta.

## <a name="syntax"></a>Sintaxis


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vItem* 
</dt> <dd>

Tipo: **variante**

Elemento o elementos que se van a copiar. Puede ser una cadena que representa un nombre de archivo, un objeto [**carpeta**](folderitem.md) o un objeto [**FolderItems**](folderitems.md) .

</dd> <dt>

*vOptions* \[ opta\]
</dt> <dd>

Tipo: **variante**

Opciones de la operación de copia. Este valor puede ser cero o una combinación de los siguientes valores. Estos valores se basan en marcas definidas para su uso con el miembro **fFlags** de la estructura [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) de C++. Cada espacio de nombres del shell debe proporcionar su propia implementación de estas marcas, y cada espacio de nombres puede optar por omitir algunos o incluso todos estos marcadores. Estas marcas no se definen por nombre para Visual Basic, VBScript o JScript, por lo que debe definirlas usted mismo o usar sus equivalentes numéricos.

> [!Note]  
> En algunos casos, como los archivos comprimidos (. zip), es posible que algunas marcas de opción se omitan por diseño.

 

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



 (8192)


</dt> <dd>

[Versión 5,0.](versions.md) No copie los archivos conectados como un grupo. Solo se copian los archivos especificados.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

No se proporciona ninguna notificación al programa que realiza la llamada para indicar que la copia se ha completado.

> [!Note]  
> No todos los métodos se implementan para todas las carpetas. Por ejemplo, el método [**ParseName**](folder-parsename.md) no se implementa para la carpeta panel de control ( \_ controles CSIDL). Si intenta llamar a un método no implementado, se genera un error 0x800A01BD (decimal 445).

 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se usa **CopyHere** para copiar el archivo de Autoexec.bat desde el directorio raíz al \\ directorio C: Windows. Se muestra el uso correcto de JScript, VBScript y Visual Basic.

JScript.net


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



VBScript


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Carpeta**](folder.md)
</dt> </dl>

 

 




