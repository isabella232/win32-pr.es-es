---
description: 'Método ShellFolderView.SelectedItems: obtiene un objeto FolderItems que representa todos los elementos seleccionados en la vista.'
title: Método ShellFolderView.SelectedItems (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectedItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1ee3bf2e-f9c9-47d9-a0f2-efedd69770c5
ms.openlocfilehash: c8da62afba7e8cc2f594f15c34e2f2bcf6af1ae8e03f857324d18e79b0967d4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857687"
---
# <a name="shellfolderviewselecteditems-method"></a>Método ShellFolderView.SelectedItems

Obtiene un [**objeto FolderItems**](folderitems.md) que representa todos los elementos seleccionados en la vista.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = ShellFolderView.SelectedItems()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FolderItems**](folderitems.md)\*\***

Referencia de objeto al [**objeto FolderItems.**](folderitems.md)

## <a name="remarks"></a>Comentarios

Solo se puede llamar a **SelectedItems** en el sistema local. No funcionará cuando se ejecute en una página web a través de HTTP o UNC.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de este método en JScript insertado en HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectedItemsJ()
    {
        var objFolderItems;
        
        objFolderItems = WebOC.Document.SelectedItems();
        if (objFolderItems != null)
        {
            alert("Got FolderItems object.");
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
        height=400>
</object>
<br><br>
<INPUT id=SelectedItems 
       type=button 
       value=SelectedItems 
       name=SelectedItems 
       onclick="fnShellFolderViewSelectedItemsJ()">
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



 

 




