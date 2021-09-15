---
title: Método WebViewFolderContents.SelectedItems (Shldisp.h)
description: 'Método WebViewFolderContents.SelectedItems: obtiene un objeto FolderItems que representa todos los elementos seleccionados en la vista.'
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Características heredadas del entorno de Windows SelectedItems
- Método SelectedItems heredado Windows de entorno , objeto WebViewFolderContents
- Objeto WebViewFolderContents Heredado de Windows Environment Features , Método SelectedItems
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25a242991f6f9472610dffa20593f9cab5d8c310
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359142"
---
# <a name="webviewfoldercontentsselecteditems-method"></a>Método WebViewFolderContents.SelectedItems

Obtiene un [**objeto FolderItems**](../shell/folderitems.md) que representa todos los elementos seleccionados en la vista.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FolderItems**](../shell/folderitems.md)\*\***

Referencia de objeto al [**objeto FolderItems.**](../shell/folderitems.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de este método para JScript insertado en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

