---
description: Extiende el objeto IShellDispatch con una variedad de nuevas funciones.
ms.assetid: 74687929-0777-479b-9853-2b0cf4b6adc9
title: Objeto IShellDispatch2 (Shldisp. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984675"
---
# <a name="ishelldispatch2-object"></a>Objeto IShellDispatch2

Extiende el objeto [**IShellDispatch**](ishelldispatch.md) con una variedad de nuevas funciones.

> [!Note]  
> **IShellDispatch2** se implementa y se obtiene acceso a él a través del objeto de [**Shell**](shell.md) .

 

## <a name="members"></a>Miembros

El objeto **IShellDispatch2** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

El objeto **IShellDispatch2** tiene estos métodos.



| Método                                                               | Descripción                                                                        |
|:---------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**CanStartStopService**](ishelldispatch2-canstartstopservice.md)   | Determina si el usuario actual puede iniciar y detener el servicio con nombre.<br/>    |
| [**FindPrinter**](ishelldispatch2-findprinter.md)                   | Muestra el cuadro de diálogo **Buscar impresora** .<br/>                               |
| [**GetSystemInformation**](ishelldispatch2-getsysteminformation.md) | Recupera información del sistema.<br/>                                           |
| [**IsRestricted**](ishelldispatch2-isrestricted.md)                 | Recupera el valor de restricción de un grupo del registro.<br/>              |
| [**IsServiceRunning**](ishelldispatch2-isservicerunning.md)         | Devuelve un valor que indica si se está ejecutando un servicio determinado.<br/> |
| [**ServiceStart**](ishelldispatch2-servicestart.md)                 | Inicia un servicio con nombre.<br/>                                                 |
| [**ServiceStop**](ishelldispatch2-servicestop.md)                   | Detiene un servicio con nombre.<br/>                                                  |
| [**ShellExecute**](ishelldispatch2-shellexecute.md)                 | Realiza una operación especificada en un archivo especificado.<br/>                     |
| [**ShowBrowserBar**](ishelldispatch2-showbrowserbar.md)             | Muestra una barra del explorador.<br/>                                                 |



 

## <a name="remarks"></a>Observaciones

Para obtener una explicación de los servicios de Windows, consulte la documentación de los [servicios](../services/services.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Objeto de Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> </dl>

 

 
