---
title: Propiedad WebViewFolderContents.FocusedItem (Shldisp.h)
description: 'Propiedad WebViewFolderContents.FocusedItem: obtiene un objeto FolderItem que representa el elemento que tiene el foco de entrada.'
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Características heredadas del entorno de Windows focusedItem
- Propiedad FocusedItem heredada Windows environment features , objeto WebViewFolderContents
- Objeto WebViewFolderContents Heredado Windows Environment Features , Propiedad FocusedItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4d9a22ac1529fc7f8f3880f53666e9835fae1088d3c7548abfa38a5f400061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114535"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a>Propiedad WebViewFolderContents.FocusedItem

Obtiene un [**objeto FolderItem**](../shell/folderitem.md) que representa el elemento que tiene el foco de entrada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a>Valor de propiedad

Variable de tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recibe el objeto de elemento centrado.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de esta propiedad en JScript incrustada en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
</body>
</html>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

