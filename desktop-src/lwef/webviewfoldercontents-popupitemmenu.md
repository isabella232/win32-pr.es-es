---
title: Método WebViewFolderContents. PopupItemMenu (Shldisp. h)
description: Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.
ms.assetid: 3c07500c-2fe9-4976-a1a8-b128e75f9325
keywords:
- Método PopupItemMenu características del entorno heredado de Windows
- Método PopupItemMenu características de entorno heredado de Windows, objeto WebViewFolderContents
- Objeto WebViewFolderContents características de entorno de Windows heredado, método PopupItemMenu
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
ms.openlocfilehash: 41753814f103998185acc798a37447f22356d2aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801244"
---
# <a name="webviewfoldercontentspopupitemmenu-method"></a>WebViewFolderContents. PopupItemMenu, método

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

*vItem* \[ de\]
</dt> <dd>

Tipo: **variante**

Objeto [**carpeta**](../shell/folderitem.md) para el que se creará el menú contextual.

</dd> <dt>

*VX* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Posición horizontal del menú, en coordenadas de la pantalla.

</dd> <dt>

*VY* \[ en, opcional\]
</dt> <dd>

Tipo: **variante**

Posición vertical del menú, en coordenadas de la pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[BSTR](/previous-versions/windows/desktop/automat/bstr) \** _

Cuando este método devuelve un valor, contiene la cadena de comando.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso correcto de _ *PopupItemMenu** para JScript Embedded en HTML.


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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

