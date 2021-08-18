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
ms.openlocfilehash: 41a37d1b8f9874bdddd5a9593e0eade8bc0b5b92d30f8ada4ee9c6295af1d632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968404"
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
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



 

 
