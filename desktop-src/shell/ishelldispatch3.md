---
description: Extiende el objeto IShellDispatch2.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: Objeto IShellDispatch3 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 8f02095415ff2682e1f2a2eeb21c4afe0754b72251f6129856f1b6a415913cf4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720921"
---
# <a name="ishelldispatch3-object"></a>Objeto IShellDispatch3

Extiende el [**objeto IShellDispatch2.**](ishelldispatch2-object.md) **IShellDispatch3 admite** un nuevo método además de las propiedades y los métodos admitidos por **IShellDispatch2.**

> [!Note]  
> **IShellDispatch3** se implementa y se accede a través del [**objeto Shell.**](shell.md)

 

## <a name="members"></a>Miembros

El **objeto IShellDispatch3** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto IShellDispatch3** tiene estos métodos.



| Método                                             | Descripción                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [**AddToRecent**](ishelldispatch3-addtorecent.md) | Agrega un archivo a la lista de mru usada más recientemente.<br/> |



 

## <a name="remarks"></a>Comentarios

Para obtener una explicación de Windows servicios, consulte la [documentación de](../services/services.md) servicios.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> </dl>

 

 
