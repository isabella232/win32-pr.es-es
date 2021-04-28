---
title: Método WebViewFolderContents.SelectItem (Shldisp.h)
description: 'Método WebViewFolderContents.SelectItem: establece el estado de selección de un elemento en la vista.'
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Características heredadas del entorno de Windows del método SelectItem
- SelectItem method Legacy Windows Environment Features , WebViewFolderContents (Objeto WebViewFolderContents)
- WebViewFolderContents object Legacy Windows Environment Features , SelectItem method (Características heredadas del entorno de Windows del objeto WebViewFolderContents), método SelectItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66e2d05c010199f05826df7ed4591e8c7c1723e2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102614"
---
# <a name="webviewfoldercontentsselectitem-method"></a>Método WebViewFolderContents.SelectItem

Establece el estado de selección de un elemento en la vista.

## <a name="syntax"></a>Sintaxis


```JScript
WebViewFolderContents.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vItem* \[ En\]
</dt> <dd>

Tipo: **\* Variant**

Objeto [**FolderItem**](../shell/folderitem.md) para el que se establecerá el estado de selección.

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

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de este método para JScript insertado en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            FileList.SelectItem(objFolderItem, 1);
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



 

