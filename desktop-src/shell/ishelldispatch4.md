---
description: Extiende el objeto IShellDispatch3.
title: Objeto IShellDispatch4 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: 057ef4082bac8d04c006d951db7d2d251be2f8c62e88af65bc1a69678514af81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118969014"
---
# <a name="ishelldispatch4-object"></a>Objeto IShellDispatch4

Extiende el [**objeto IShellDispatch3.**](ishelldispatch3.md) Además de las propiedades y los métodos admitidos por **IShellDispatch3,** **IShellDispatch4** admite cuatro métodos adicionales.

> [!Note]  
> **IShellDispatch4** se implementa y se accede a través del [**objeto Shell.**](shell.md)

 

## <a name="members"></a>Miembros

El **objeto IShellDispatch4** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto IShellDispatch4** tiene estos métodos.



| Método                                                     | Descripción                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | Obtiene el valor de una directiva Internet Explorer especificada.<br/> |
| [**GetSetting**](ishelldispatch4-getsetting.md)           | Recupera una configuración de Shell global.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Muestra u oculta el escritorio.<br/>                           |
| [**WindowsSeguridad**](ishelldispatch4-windowssecurity.md) | Muestra el **cuadro Seguridad de Windows** de diálogo.<br/>            |



 

## <a name="remarks"></a>Comentarios

Para obtener una explicación de Windows servicios, consulte la [documentación de](../services/services.md) servicios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> </dl>

 

 
