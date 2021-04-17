---
title: Método WebViewFolderContents. SelectItem (Shldisp. h)
description: Establece el estado de selección de un elemento en la vista.
ms.assetid: c0e163ee-1951-476c-807a-781e26766d99
keywords:
- Método SelectItem características del entorno heredado de Windows
- Método SelectItem características de entorno heredado de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredado, método SelectItem
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
ms.openlocfilehash: e491fb27db2d6e1e9b449be4aa2924684021539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714538"
---
# <a name="webviewfoldercontentsselectitem-method"></a>WebViewFolderContents. SelectItem, método

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

*vItem* \[ de\]
</dt> <dd>

Tipo: **variante \** _

El objeto [_ *carpeta* *](../shell/folderitem.md) para el que se establecerá el estado de selección.

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

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de este método para JScript incrustado en HTML.


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



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

