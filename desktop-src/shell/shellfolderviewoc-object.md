---
description: Reenvía los eventos desencadenados por un objeto ShellFolderView especificado a los controladores de eventos ShellFolderViewOC correspondientes.
title: Objeto ShellFolderViewOC (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: 2670578417dc616d30f319887f5281fa5d0615f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468058"
---
# <a name="shellfolderviewoc-object"></a>Objeto ShellFolderViewOC

Reenvía los eventos desencadenados por un objeto [**ShellFolderView**](shellfolderview.md) especificado a los controladores de eventos **ShellFolderViewOC** correspondientes.

## <a name="members"></a>Members

El **objeto ShellFolderViewOC** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)

### <a name="events"></a>Eventos

El **objeto ShellFolderViewOC** tiene estos eventos.



| Evento                                                          | Descripción                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**EnumDone**](shellfolderviewoc-enumdone.md)                 | Indica que el [**objeto ShellFolderView**](shellfolderview.md) ha terminado de enumerar el contenido de la carpeta.<br/> |
| [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) | Indica que el estado de selección de uno o varios elementos de la vista ha cambiado.<br/>                                     |



 

### <a name="methods"></a>Métodos

El **objeto ShellFolderViewOC** tiene estos métodos.



| Método                                                   | Descripción                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetFolderView**](shellfolderviewoc-setfolderview.md) | Reenvía los eventos del objeto [**ShellFolderView**](shellfolderview.md) especificado al controlador de **eventos ShellFolderViewOC** correspondiente.<br/> |



 

## <a name="remarks"></a>Observaciones

El [**objeto ShellFolderView**](shellfolderview.md) desvía dos eventos, [**EnumDone**](shellfolderviewoc-enumdone.md) y [**SelectionChanged,**](shellfolderviewoc-selectionchanged.md)que suelen controlar las aplicaciones. Sin embargo, algunas aplicaciones deben controlar eventos de una serie de **objetos ShellFolderView.** Por ejemplo, una aplicación podría hospedar un control WebBrowser que permite a los usuarios navegar por una serie de carpetas. Cada carpeta tiene su propio **objeto ShellFolderView** con sus eventos asociados. Controlar estos eventos puede ser difícil.

El **objeto ShellFolderViewOC** simplifica el control de eventos para estos escenarios. Permite a las aplicaciones controlar eventos para todos los [**objetos ShellFolderView**](shellfolderview.md) con un único par de controladores de eventos **ShellFolderViewOC.** Cada vez que el usuario navega a una nueva carpeta, la aplicación pasa el objeto **ShellFolderView** asociado al objeto **ShellFolderViewOC** llamando a [**SetFolderView**](shellfolderviewoc-setfolderview.md). A continuación, cuando se desencadena un evento [**EnumDone**](shellfolderviewoc-enumdone.md) o [**SelectionChanged,**](shellfolderviewoc-selectionchanged.md) el objeto **ShellFolderViewOC** reenvía el evento a su propio controlador para su procesamiento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShellFolderView**](shellfolderview.md)
</dt> </dl>

 

 




