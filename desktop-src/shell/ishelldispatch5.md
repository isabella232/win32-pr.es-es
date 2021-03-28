---
description: Extiende el objeto IShellDispatch4.
title: Objeto IShellDispatch5 (Shldisp. h)
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
ms.openlocfilehash: cbf3e960d7bfb9cd15411142cc036a21a9995ff9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984643"
---
# <a name="ishelldispatch5-object"></a>Objeto IShellDispatch5

Extiende el objeto [**IShellDispatch4**](ishelldispatch4.md) . Además de las propiedades y los métodos admitidos por **IShellDispatch4**, **IShellDispatch5** agrega un método que muestra ventanas abiertas en una pila 3D.

> [!Note]  
> **IShellDispatch5** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .

 

## <a name="members"></a>Miembros

El objeto **IShellDispatch5** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **IShellDispatch5** tiene estos métodos.



| Método                                                   | Descripción                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**WindowSwitcher**](ishelldispatch5-windowswitcher.md) | Muestra las ventanas abiertas en una pila 3D que se puede desplazar.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto de Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> <dt>

[**IShellDispatch4**](ishelldispatch4.md)
</dt> </dl>

 

 
