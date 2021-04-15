---
description: Realiza una operación especificada en un archivo especificado.
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Método Shell.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 83ab9741199bff675245f15dc2ad1ffb20592a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985603"
---
# <a name="shellshellexecute-method"></a>Shell. ShellExecute (método)

Realiza una operación especificada en un archivo especificado.

## <a name="syntax"></a>Sintaxis

JScript.net

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

VBScript

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

VB:

```vb
Shell.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*sFile* \[ de\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Cadena** que contiene el nombre del archivo en el que **ShellExecute** realizará la acción especificada por *vOperation*.

</dd> <dt>

*vArguments* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Cadena que contiene los valores de los parámetros de la operación.

</dd> <dt>

*vDirectory* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Ruta de acceso completa del directorio que contiene el archivo especificado por *sFile*. Si no se especifica este parámetro, se utiliza el directorio de trabajo actual.

</dd> <dt>

*vOperation* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

La operación que se va a realizar. Este valor se establece en una de las cadenas de verbo que admite el archivo. Para obtener una explicación de los verbos, vea la sección Comentarios. Si no se especifica este parámetro, se realiza la operación predeterminada.

</dd> <dt>

*vShow* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Recomendación sobre cómo se debe mostrar inicialmente la ventana de la aplicación. La aplicación puede omitir esta recomendación. Este parámetro puede ser uno de los valores siguientes. Si no se especifica este parámetro, la aplicación usa su valor predeterminado.



| Value                                                                                                                               | Significado                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>0</dt> </dl>  | Abra la aplicación con una ventana oculta.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Abra la aplicación con una ventana normal. Si la ventana está minimizada o maximizada, el sistema la restaura a su tamaño y posición originales.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Abra la aplicación con una ventana minimizada.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Abra la aplicación con una ventana maximizada.<br/>                                                                                                 |
| <dl> <dt></dt><dt>4</dt> </dl>  | Abra la aplicación con su ventana en su tamaño y posición más recientes. La ventana activa permanece activa.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Abra la aplicación con su ventana en su posición y tamaño actuales.<br/>                                                                        |
| <dl> <dt></dt><dt>7</dt> </dl>  | Abra la aplicación con una ventana minimizada. La ventana activa permanece activa.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Abra la aplicación con su ventana en el estado predeterminado especificado por la aplicación.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Este método es equivalente a iniciar uno de los comandos asociados al menú contextual de un archivo. Cada comando se representa mediante una cadena de verbo. El conjunto de verbos admitidos varía de un archivo a un archivo. El verbo que se admite con mayor frecuencia es "Open", que suele ser el verbo predeterminado. Es posible que se admitan otros verbos solo en determinados tipos de archivos. Para obtener más información sobre los verbos de Shell, vea [iniciar aplicaciones](launch.md) o [extender menús contextuales](context.md).

Este método no está disponible actualmente en Microsoft Visual Basic.

## <a name="examples"></a>Ejemplos

En los siguientes ejemplos se muestra el uso de **ShellExecute** para abrir el Bloc de notas. Se muestra el uso de JScript y VBScript.

JScript.net


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

VBScript

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



 

 
