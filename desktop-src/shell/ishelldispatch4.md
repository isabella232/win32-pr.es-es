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
ms.openlocfilehash: daec9c922a0bac05154c1108f236ddf336a2e380
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468165"
---
# <a name="ishelldispatch4-object"></a>Objeto IShellDispatch4

Extiende el [**objeto IShellDispatch3.**](ishelldispatch3.md) Además de las propiedades y los métodos admitidos por **IShellDispatch3,** **IShellDispatch4** admite cuatro métodos adicionales.

> [!Note]  
> **IShellDispatch4** se implementa y se accede a través del [**objeto Shell.**](shell.md)

 

## <a name="members"></a>Members

El **objeto IShellDispatch4** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto IShellDispatch4** tiene estos métodos.



| Método                                                     | Descripción                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | Obtiene el valor de una directiva Internet Explorer especificada.<br/> |
| [**GetSetting**](ishelldispatch4-getsetting.md)           | Recupera una configuración de Shell global.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Muestra u oculta el escritorio.<br/>                           |
| [**WindowsSeguridad**](ishelldispatch4-windowssecurity.md) | Muestra el **Seguridad de Windows** de diálogo.<br/>            |



 

## <a name="remarks"></a>Observaciones

Para obtener una explicación de Windows servicios, consulte la [documentación de](../services/services.md) servicios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 6.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

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
</dt> </dl>

 

 
