---
description: Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.
title: Método ShellFolderView. PopupItemMenu (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.PopupItemMenu
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 1610d91e-87c3-4ba5-9147-1595eddb2c3a
ms.openlocfilehash: 513f654442361da840cb02089810c814275c5867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278498"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>ShellFolderView. PopupItemMenu, método

Crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = ShellFolderView.PopupItemMenu(
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

Objeto [**carpeta**](folderitem.md) para el que se creará el menú contextual.

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

Tipo: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr) \** _

_ *Cadena** que recibe la cadena de comandos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4,71 o posterior)</dt> </dl> |



 

 
