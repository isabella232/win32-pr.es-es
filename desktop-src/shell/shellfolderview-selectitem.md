---
description: Establece el estado de selección de un elemento en la vista.
title: Método ShellFolderView. SelectItem (Shldisp. h)
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
ms.openlocfilehash: d44633983075cdf22581bce05cfb7c073f422084
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278496"
---
# <a name="shellfolderviewselectitem-method"></a>ShellFolderView. SelectItem, método

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

*vItem* \[ de\]
</dt> <dd>

Tipo: **variante \** _

El objeto [_ *carpeta* *](folderitem.md) para el que se establecerá el estado de selección.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Tipo: **Integer**

Un conjunto de marcas que indican el nuevo estado de la selección. Puede ser uno o varios de los valores siguientes.

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

Poner el elemento en modo de edición.

</dd> <dt>



 (4)


</dt> <dd>

Anule la selección de todos los elementos excepto el especificado.

</dd> <dt>



 (8)


</dt> <dd>

Asegúrese de que el elemento se muestra en la vista.

</dd> <dt>



 (16)


</dt> <dd>

Asigne al elemento el foco.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Solo se puede llamar a [**FocusedItem**](shellfolderview-focuseditem.md) en el sistema local. No funcionará cuando se ejecute en una página web a través de HTTP o UNC.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de este método en JScript incrustado en HTML.


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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 




