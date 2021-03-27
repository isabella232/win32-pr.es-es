---
description: Recibe los eventos de registro de la ventana IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Objeto DShellWindowsEvents (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DShellWindowsEvents
api_type:
- COM
api_location:
- Shdocvw.dll
ms.openlocfilehash: 7df1571556b5f2942f181b4c88b22ff3bc83f273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987552"
---
# <a name="dshellwindowsevents-object"></a>Objeto DShellWindowsEvents

Recibe los eventos de registro de la ventana [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows) .

## <a name="members"></a>Miembros

El objeto **DShellWindowsEvents** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **DShellWindowsEvents** tiene estos métodos.



| Método                                                           | Descripción                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**WindowRegistered**](dshellwindowsevents-windowregistered.md) | Se llama cuando una ventana se registra como una ventana de Shell. <br/> |
| [**WindowRevoked**](dshellwindowsevents-windowrevoked.md)       | Se llama cuando se revoca el registro de una ventana de Shell. <br/> |



 

## <a name="remarks"></a>Observaciones

Use **DShellWindowsEvents** para supervisar Cuándo se registra o revoca una ventana de Shell. Para obtener más información, vea [**IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Producto<br/> | Internet Explorer 5<br/>                                                                                           |
| Encabezado<br/>  | <dl> <dt>Exdisp. h</dt> </dl>                                      |
| Archivo DLL<br/>     | <dl> <dt>Shdocvw.dll (versión 5.00.2014.0216 o posterior)</dt> </dl> |
| IID<br/>     | \_ISHELLWINDOWS IID<br/>                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShellWindows**](shellwindows.md)
</dt> </dl>

 

 




