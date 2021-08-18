---
description: Recibe eventos de registro de ventana de IShellWindows.
ms.assetid: c340296d-f8eb-43a1-809d-912ea7412fe2
title: Objeto DShellWindowsEvents (Exdisp.h)
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
ms.openlocfilehash: 13335268b892e4ac95520221fcd2e413c9c255225ccd8fc36c3c73cbf8c327a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009545"
---
# <a name="dshellwindowsevents-object"></a>Objeto DShellWindowsEvents

Recibe eventos de registro de ventana de [**IShellWindows.**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows)

## <a name="members"></a>Miembros

El **objeto DShellWindowsEvents** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto DShellWindowsEvents** tiene estos métodos.



| Método                                                           | Descripción                                                       |
|:-----------------------------------------------------------------|:------------------------------------------------------------------|
| [**WindowRegistered**](dshellwindowsevents-windowregistered.md) | Se llama cuando se registra una ventana como ventana de Shell. <br/> |
| [**WindowRevoked**](dshellwindowsevents-windowrevoked.md)       | Se llama cuando se revoca el registro de una ventana de Shell. <br/> |



 

## <a name="remarks"></a>Comentarios

Use **DShellWindowsEvents para** supervisar cuándo se registra o revoca una ventana de Shell. Para obtener más información, [**vea IShellWindows**](/windows/desktop/api/Exdisp/nn-exdisp-ishellwindows).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Producto<br/> | Internet Explorer 5<br/>                                                                                           |
| Header<br/>  | <dl> <dt>Exdisp.h</dt> </dl>                                      |
| Archivo DLL<br/>     | <dl> <dt>Shdocvw.dll (versión 5.00.2014.0216 o posterior)</dt> </dl> |
| IID<br/>     | IID \_ IShellWindows<br/>                                                                                            |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ShellWindows**](shellwindows.md)
</dt> </dl>

 

 




