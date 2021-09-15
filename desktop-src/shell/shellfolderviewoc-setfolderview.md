---
description: Reenvía los eventos del objeto ShellFolderView especificado al controlador de eventos ShellFolderViewOC correspondiente.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Método ShellFolderViewOC.SetFolderView (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468055"
---
# <a name="shellfolderviewocsetfolderview-method"></a>Método ShellFolderViewOC.SetFolderView

Reenvía los eventos del objeto [**ShellFolderView**](shellfolderview.md) especificado al controlador [**de eventos ShellFolderViewOC**](shellfolderviewoc-object.md) correspondiente.

## <a name="syntax"></a>Sintaxis


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*oShellFolderView* \[ En\]
</dt> <dd>

Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\***

Objeto [**ShellFolderView.**](shellfolderview.md) Sus [**eventos EnumDone**](shellfolderviewoc-enumdone.md) [**y SelectionChanged**](shellfolderview-selectionchanged.md) se reenviarán al controlador de [**eventos ShellFolderViewOC**](shellfolderviewoc-object.md) correspondiente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
