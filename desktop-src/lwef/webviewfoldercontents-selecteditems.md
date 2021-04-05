---
title: Método WebViewFolderContents.SelectedItems (Shldisp.h)
description: Obtiene un objeto FolderItems que representa todos los elementos seleccionados en la vista.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Método SelectedItems características del entorno heredado de Windows
- Método SelectedItems herencia de características de entorno de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredadas, método SelectedItems
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
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079681"
---
# <a name="webviewfoldercontentsselecteditems-method"></a>WebViewFolderContents. SelectedItems (método)

Obtiene un objeto [**FolderItems**](../shell/folderitems.md) que representa todos los elementos seleccionados en la vista.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **FolderItems**](../shell/folderitems.md)\*\***

Una referencia de objeto al objeto [**FolderItems**](../shell/folderitems.md) .

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de este método para JScript incrustado en HTML.


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

