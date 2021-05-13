---
description: Extiende el objeto IShellDispatch4.
title: Objeto IShellDispatch5 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: 26c3112faa748aa443526fbe9cb493af67502cd7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843006"
---
# <a name="ishelldispatch5-object"></a>Objeto IShellDispatch5

Extiende el [**objeto IShellDispatch4.**](ishelldispatch4.md) Además de las propiedades y los métodos admitidos por **IShellDispatch4,** **IShellDispatch5** agrega un método que muestra las ventanas abiertas en una pila 3D.

> [!Note]  
> **IShellDispatch5** se implementa y se accede a través del [**objeto Shell.**](shell.md)

 

## <a name="members"></a>Members

El **objeto IShellDispatch5** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto IShellDispatch5** tiene estos métodos.



| Método                                                   | Descripción                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**WindowSwitcher**](ishelldispatch5-windowswitcher.md) | Muestra las ventanas abiertas en una pila 3D por la que puede cambiar.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> <dt>

[**IShellDispatch4**](ishelldispatch4.md)
</dt> </dl>

 

 
