---
title: Propiedad WebViewFolderContents.FocusedItem (Shldisp.h)
description: 'Propiedad WebViewFolderContents.FocusedItem: obtiene un objeto FolderItem que representa el elemento que tiene el foco de entrada.'
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Características heredadas del entorno de Windows de la propiedad FocusedItem
- Objeto WebViewFolderContents de características heredadas del entorno de Windows de la propiedad FocusedItem
- Objeto WebViewFolderContents Características heredadas del entorno de Windows, propiedad FocusedItem
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
ms.openlocfilehash: 724743b81f605dc9ba5794a4a796b8a0c4a2a03f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102733"
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

En el ejemplo siguiente se muestra el uso adecuado de esta propiedad en JScript insertado en HTML.


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



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

