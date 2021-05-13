---
description: 'Método ShellFolderView.PopupItemMenu: crea un menú contextual para el elemento especificado y devuelve la cadena de comando seleccionada.'
title: Método ShellFolderView.PopupItemMenu (Shldisp.h)
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
ms.openlocfilehash: 7a2feda23d6e1759e1c0be27805fefbb6b592df7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840756"
---
# <a name="shellfolderviewpopupitemmenu-method"></a>Método ShellFolderView.PopupItemMenu

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

*vItem* \[ En\]
</dt> <dd>

Tipo: **Variant**

Objeto [**FolderItem**](folderitem.md) para el que se creará el menú contextual.

</dd> <dt>

*vx* \[ in, opcional\]
</dt> <dd>

Tipo: **Variant**

Posición horizontal del menú, en coordenadas de pantalla.

</dd> <dt>

*vy* \[ in, opcional\]
</dt> <dd>

Tipo: **Variant**

Posición vertical del menú, en coordenadas de pantalla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

Cadena **que** recibe la cadena de comando.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]<br/>                                         |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                           |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 4.71 o posterior)</dt> </dl> |



 

 
