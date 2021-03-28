---
description: Extiende el objeto IShellDispatch3.
title: Objeto IShellDispatch4 (Shldisp. h)
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
ms.openlocfilehash: 0bdada12a48f9c48749b614e6b45ff5427e62b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543123"
---
# <a name="ishelldispatch4-object"></a>Objeto IShellDispatch4

Extiende el objeto [**IShellDispatch3**](ishelldispatch3.md) . Además de las propiedades y los métodos admitidos por **IShellDispatch3**, **IShellDispatch4** admite cuatro métodos adicionales.

> [!Note]  
> **IShellDispatch4** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .

 

## <a name="members"></a>Miembros

El objeto **IShellDispatch4** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **IShellDispatch4** tiene estos métodos.



| Método                                                     | Descripción                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | Obtiene el valor de una directiva especificada de Internet Explorer.<br/> |
| [**GetSetting**](ishelldispatch4-getsetting.md)           | Recupera una configuración de Shell global.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Muestra u oculta el escritorio.<br/>                           |
| [**WindowsSecurity**](ishelldispatch4-windowssecurity.md) | Muestra el cuadro de diálogo **seguridad de Windows** .<br/>            |



 

## <a name="remarks"></a>Observaciones

Para obtener una explicación de los servicios de Windows, consulte la documentación de los [servicios](../services/services.md) .

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
</dt> </dl>

 

 
