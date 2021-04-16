---
description: Control de la instancia del recopilador. Requiere los privilegios de administrador (BA).
ms.assetid: 83b485b2-b03b-4882-a3ff-187eac299755
ms.tgt_platform: multiple
title: Control (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 2681af7425fd5cacf88375e11e4658e5d4b1a2c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538337"
---
# <a name="control-class"></a>Control (clase)

Control de la instancia del recopilador. Requiere los privilegios de administrador (BA).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Provider("BootEventCollectorWmiProvider"), AMENDMENT]
class Control
{
};
```

## <a name="members"></a>Miembros

La clase de **control** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **control** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Punto de control**](control-checkpoint.md)                       | Si la configuración actual es el resultado de la operación de deshacer/rehacer/restaurar, la marca como si se hubiera establecido explícitamente, de modo que el historial conservará la hora en que se estableció y se creará un archivo de copia de seguridad en el siguiente cambio de configuración. Si la configuración actual ya estaba establecida explícitamente, no tiene ningún efecto. Devuelve 1 si se realiza correctamente, 0 en caso de error.<br/> |
| [**DumpDiagnostics**](control-dumpdiagnostics.md)             | Vuelca la información de diagnóstico en el registro.<br/>                                                                                                                                                                                                                                                                                                                  |
| [**FastShutdown**](control-fastshutdown.md)                   | Detenga el recopilador rápidamente, descartando todos los datos en cola.<br/>                                                                                                                                                                                                                                                                                                    |
| [**Vaciar**](control-flush.md)                                 | Vacíe los búferes del reenviador.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**GetConfiguration**](control-getconfiguration.md)           | Lea la configuración activa del recopilador.<br/>                                                                                                                                                                                                                                                                                                                |
| [**IsConfigurationEqual**](control-isconfigurationequal.md)   | Compare el argumento con la configuración activa del recopilador. Devuelve 1 si coinciden; 0 si no lo hacen.<br/>                                                                                                                                                                                                                                                 |
| [**ListBackups**](control-listbackups.md)                     | Devuelve la lista de los archivos de configuración de copia de seguridad guardados que se pueden restaurar.<br/>                                                                                                                                                                                                                                                                                  |
| [**Rehacer**](control-redo.md)                                   | Restablezca la configuración activa del recopilador del archivo de copia de seguridad posterior (determinado por el avance desde la marca de tiempo original actual). Si se ha deshecho la configuración, significa que se rehace el cambio deshecho. Devuelve 1 si se realiza correctamente, 0 en caso de error.<br/>                                                                                                    |
| [**RestoreFile**](control-restorefile.md)                     | Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad. Devuelve 1 si se realiza correctamente, 0 en caso de error.<br/>                                                                                                                                                                                                                                                        |
| [**RestoreFromTime**](control-restorefromtime.md)             | Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad, seleccionado por una marca de tiempo. Devuelve 1 si se realiza correctamente, 0 en caso de error.<br/>                                                                                                                                                                                                                               |
| [**SetConfiguration**](control-setconfiguration.md)           | Establezca la nueva configuración activa del recopilador. Devuelve 1 si se realiza correctamente, 0 en caso de error.<br/>                                                                                                                                                                                                                                                                           |
| [**Apagado**](control-shutdown.md)                           | Detenga el recopilador. Si el recopilador se ejecuta como un servicio, el mejor enfoque es detener el servicio.<br/>                                                                                                                                                                                                                                                     |
| [**Deshacer**](control-undo.md)                                   | Restaure la configuración activa del recopilador a partir del archivo de copia de seguridad anterior (determinado mediante el regreso de la marca de tiempo original actual). Si se ha establecido la configuración, significa deshacer ese cambio. Las llamadas consecutivas desharán a las configuraciones anteriores y anteriores. Devuelve 1 si se realiza correctamente, 0 en caso de error.<br/>                           |
| [**ValidateConfiguration**](control-validateconfiguration.md) | Validar un texto de configuración para comprobar su exactitud sin establecerlo activo. Devuelve 1 si se realiza correctamente, 0 en caso de error.<br/>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz de \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

 




