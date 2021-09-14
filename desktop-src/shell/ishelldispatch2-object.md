---
description: Extiende el objeto IShellDispatch con una variedad de funcionalidades nuevas.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Objeto IShellDispatch2 (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79d3abbed038e09f2e73c62e5e3d9b16545e8f60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363078"
---
# <a name="ishelldispatch2-object"></a>Objeto IShellDispatch2

Extiende el [**objeto IShellDispatch**](ishelldispatch.md) con una variedad de funcionalidades nuevas.

> [!Note]  
> **IShellDispatch2** se implementa y se accede a través del [**objeto Shell.**](shell.md)

 

## <a name="members"></a>Members

El **objeto IShellDispatch2** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El **objeto IShellDispatch2** tiene estos métodos.



| Método                                                               | Descripción                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**CanStartStopService**](ishelldispatch2-canstartstopservice.md)   | Determina si el usuario actual puede iniciar y detener el servicio con nombre.<br/>    |
| [**FindPrinter**](ishelldispatch2-findprinter.md)                   | Muestra el **cuadro de diálogo Buscar** impresora.<br/>                               |
| [**GetSystemInformation**](ishelldispatch2-getsysteminformation.md) | Recupera información del sistema.<br/>                                           |
| [**IsRestricted**](ishelldispatch2-isrestricted.md)                 | Recupera la configuración de restricción de un grupo del Registro.<br/>              |
| [**IsServiceRunning**](ishelldispatch2-isservicerunning.md)         | Devuelve un valor que indica si se está ejecutando un servicio determinado.<br/> |
| [**ServiceStart**](ishelldispatch2-servicestart.md)                 | Inicia un servicio con nombre.<br/>                                                 |
| [**ServiceStop**](ishelldispatch2-servicestop.md)                   | Detiene un servicio con nombre.<br/>                                                  |
| [**ShellExecute**](ishelldispatch2-shellexecute.md)                 | Realiza una operación especificada en un archivo especificado.<br/>                     |
| [**ShowBrowserBar**](ishelldispatch2-showbrowserbar.md)             | Muestra una barra del explorador.<br/>                                                 |



 

## <a name="remarks"></a>Observaciones

Para obtener una explicación de Windows servicios, consulte la [documentación de](../services/services.md) servicios.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> </dl>

 

 
