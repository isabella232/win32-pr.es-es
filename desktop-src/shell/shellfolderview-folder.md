---
description: 'Propiedad ShellFolderView.Folder: obtiene un objeto Folder que representa la vista.'
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: Propiedad ShellFolderView.Folder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 40ff2dbed37aa8ceb80072870c78cee4e63cba3656550081be2c655cb6f6ddf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857714"
---
# <a name="shellfolderviewfolder-property"></a>Propiedad ShellFolderView.Folder

Obtiene un [**objeto Folder**](folder.md) que representa la vista.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a>Valor de propiedad

Objeto que recibe el [**objeto Folder.**](folder.md)

## <a name="remarks"></a>Comentarios

**Solo** se puede llamar a la carpeta en el sistema local. No funcionará cuando se ejecute en una página web a través de HTTP o UNC.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de esta propiedad para JScript incrustada en HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC" 
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




