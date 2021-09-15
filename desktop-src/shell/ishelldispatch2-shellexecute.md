---
description: 'Método IShellDispatch2.ShellExecute: realiza una operación especificada en un archivo especificado.'
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: Método IShellDispatch2.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468177"
---
# <a name="ishelldispatch2shellexecute-method"></a>Método IShellDispatch2.ShellExecute

Realiza una operación especificada en un archivo especificado.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*sFile* \[ En\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Cadena **que** contiene el nombre del archivo en el que **ShellExecute** realizará la acción especificada por *vOperation*.

</dd> <dt>

*vArguments* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Cadena que contiene valores de parámetro para la operación.

</dd> <dt>

*vDirectory* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Ruta de acceso completa del directorio que contiene el archivo especificado por *sFile*. Si no se especifica este parámetro, se usa el directorio de trabajo actual.

</dd> <dt>

*vOperation* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

La operación que se va a realizar. Este valor se establece en una de las cadenas de verbo admitidas por el archivo. Para obtener una explicación de los verbos, consulte la sección Comentarios. Si no se especifica este parámetro, se realiza la operación predeterminada.

</dd> <dt>

*vShow* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Una recomendación sobre cómo se debe mostrar inicialmente la ventana de la aplicación. La aplicación puede omitir esta recomendación. Este parámetro puede ser uno de los valores siguientes. Si no se especifica este parámetro, la aplicación usa su valor predeterminado.



| Value                                                                                                                               | Significado                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>0</dt> </dl>  | Abra la aplicación con una ventana oculta.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Abra la aplicación con una ventana normal. Si la ventana se minimiza o maximiza, el sistema la restaura a su tamaño y posición originales.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Abra la aplicación con una ventana minimizada.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Abra la aplicación con una ventana maximizada.<br/>                                                                                                 |
| <dl> <dt></dt><dt>4</dt> </dl>  | Abra la aplicación con su ventana en su tamaño y posición más recientes. La ventana activa permanece activa.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Abra la aplicación con su ventana en su tamaño y posición actuales.<br/>                                                                        |
| <dl> <dt></dt><dt>7</dt> </dl>  | Abra la aplicación con una ventana minimizada. La ventana activa permanece activa.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Abra la aplicación con su ventana en el estado predeterminado especificado por la aplicación.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este método se implementa y se accede a través del [**método Shell.ShellExecute.**](./shell-shellexecute.md)

Este método equivale a iniciar uno de los comandos asociados al menú contextual de un archivo. Cada comando se representa mediante una cadena de verbo. El conjunto de verbos admitidos varía de un archivo a otro. El verbo más admitido es "open", que también suele ser el verbo predeterminado. Otros verbos solo pueden ser compatibles con determinados tipos de archivos. Para obtener más información sobre los verbos de Shell, vea [Iniciar aplicaciones](launch.md) o [Extender menús contextuales.](context.md)

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los ejemplos siguientes se muestra el uso **de ShellExecute** para abrir Bloc de notas. El uso se muestra para JScript y VBScript.

JScript:


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
