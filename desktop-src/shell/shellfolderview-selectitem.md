---
description: 'Método ShellFolderView.SelectItem: establece el estado de selección de un elemento en la vista.'
title: Método ShellFolderView.SelectItem (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: c8cbff0da4da55d9621bfeb01f26c5ed62fe230a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116753"
---
# <a name="shellfolderviewselectitem-method"></a>Método ShellFolderView.SelectItem

Establece el estado de selección de un elemento en la vista.

## <a name="syntax"></a>Sintaxis


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vItem* \[ En\]
</dt> <dd>

Tipo: **\* Variant**

Objeto [**FolderItem**](folderitem.md) para el que se establecerá el estado de selección.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Tipo: **Entero**

Conjunto de marcas que indican el nuevo estado de selección. Puede ser uno o varios de los valores siguientes.

<dt>



  (0)


</dt> <dd>

Anule la selección del elemento.

</dd> <dt>



 (1)


</dt> <dd>

Seleccione el elemento.

</dd> <dt>



 (3)


</dt> <dd>

Coloque el elemento en modo de edición.

</dd> <dt>



 (4)


</dt> <dd>

Anule la selección de todos los elementos menos el especificado.

</dd> <dt>



 (8)


</dt> <dd>

Asegúrese de que el elemento se muestra en la vista.

</dd> <dt>



 (16)


</dt> <dd>

Dé el foco al elemento.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Solo se puede llamar a [**FocusedItem**](shellfolderview-focuseditem.md) en el sistema local. No funcionará cuando se ejecute en una página web a través de HTTP o UNC.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de este método en JScript incrustado en HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
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
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
</body>
</html>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 




