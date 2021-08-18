---
title: Método WebViewFolderContents.PopupItemMenu (Shldisp.h)
description: 'Método WebViewFolderContents.PopupItemMenu: crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.'
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Método PopupItemMenu Legacy Windows Environment Features
- Método PopupItemMenu heredado Windows environment features , objeto WebViewFolderContents
- Objeto WebViewFolderContents Heredado Windows Environment Features , método PopupItemMenu
topic_type:
- apiref
api_name:
- WebViewFolderContents.PopupItemMenu
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 274237b2a17aa3e891f0c65f139cc7b251c1ff8a78b1f0ad387fb2931c8e3107
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035973"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>Método WebViewFolderContents.PopupItemMenu

Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = WebViewFolderContents.PopupItemMenu(
  vItem,
  [ vx ],
  [ vy ]
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*vItem* \[ En\]
</dt> <dd>

Tipo: **Variant**

Objeto [**FolderItem**](../shell/folderitem.md) para el que se creará el menú contextual.

</dd> <dt>

*vx* \[ in, opcional\]
</dt> <dd>

Tipo: **Variant**

Posición horizontal del menú, en coordenadas de pantalla.

</dd> <dt>

*vy* \[ en, opcional\]
</dt> <dd>

Tipo: **Variant**

Posición vertical del menú, en coordenadas de pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[BSTR](/previous-versions/windows/desktop/automat/bstr)\***

Cuando este método vuelve, contiene la cadena de comando.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso adecuado de **PopupItemMenu** JScript insertado en HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsPopupItemMenuJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            var szCommand;

            szCommand = FileList.PopupItemMenu(objFolderItem);
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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

