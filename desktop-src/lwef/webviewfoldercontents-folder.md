---
title: Propiedad WebViewFolderContents.Folder (Shldisp.h)
description: 'Propiedad WebViewFolderContents.Folder: obtiene un objeto Folder que representa la vista.'
ms.assetid: 1d81c27a-1e48-4c0a-b74d-c63af43a909d
keywords:
- Propiedades de carpeta Características heredadas Windows entorno de ejecución
- Propiedad de carpeta Legacy Windows Environment Features , Objeto WebViewFolderContents
- Objeto WebViewFolderContents heredado de Windows environment features , propiedad Folder
topic_type:
- apiref
api_name:
- WebViewFolderContents.Folder
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af475d55351d9278ca954a9ebb896ef03928538b9984a2f87478ed3358a1741e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607845"
---
# <a name="webviewfoldercontentsfolder-property"></a>Propiedad WebViewFolderContents.Folder

Obtiene un [**objeto Folder**](../shell/folder.md) que representa la vista.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
Folder = WebViewFolderContents.Folder
```



## <a name="property-value"></a>Valor de propiedad

Objeto que recibe el [**objeto Folder.**](../shell/folder.md)

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de esta propiedad JScript incrustada en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFolderJ()
    {
        var objFolder;

        objFolder = FileList.Folder;
        if (objFolder != null)
        {
            alert(objFolder.Title);
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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

