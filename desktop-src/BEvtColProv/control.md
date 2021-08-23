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
ms.openlocfilehash: 5eeccd31f3d9ab1f0b0ec05ebf80ea9f880a73fed21b21fe67fe63257af28871
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589025"
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

La **clase Control** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **clase Control** tiene estos métodos.



| Método                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Punto de control**](control-checkpoint.md)                       | Si la configuración actual es el resultado de deshacer, rehacer o restaurar, la marca como si se hubiera establecido explícitamente, de modo que el historial conservará la hora en que se estableció y se creará un archivo de copia de seguridad para él en el siguiente cambio de configuración. Si la configuración actual ya se estableció explícitamente, no tiene ningún efecto. Devuelve 1 si se ejecuta correctamente, 0 en caso de error.<br/> |
| [**DumpDiagnostics**](control-dumpdiagnostics.md)             | Vuelque la información de diagnóstico en el registro.<br/>                                                                                                                                                                                                                                                                                                                  |
| [**FastShutdown**](control-fastshutdown.md)                   | Detenga el recopilador rápidamente, descartando todos los datos en cola.<br/>                                                                                                                                                                                                                                                                                                    |
| [**Vaciar**](control-flush.md)                                 | Vacíe los búferes del reenviador.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**GetConfiguration**](control-getconfiguration.md)           | Lea la configuración activa del recopilador.<br/>                                                                                                                                                                                                                                                                                                                |
| [**IsConfigurationEqual**](control-isconfigurationequal.md)   | Compare el argumento con la configuración activa del recopilador. Devuelve 1 si coinciden, 0 si no lo hacen.<br/>                                                                                                                                                                                                                                                 |
| [**ListBackups**](control-listbackups.md)                     | Devuelve la lista de los archivos de configuración de copia de seguridad guardados que se pueden restaurar.<br/>                                                                                                                                                                                                                                                                                  |
| [**Rehacer**](control-redo.md)                                   | Restablezca la configuración activa del recopilador desde el archivo de copia de seguridad posterior (determinado a partir de la marca de tiempo original actual). Si la configuración se ha deshace, significa volver a hacer el cambio deshacer. Devuelve 1 si se ejecuta correctamente, 0 en caso de error.<br/>                                                                                                    |
| [**RestoreFile**](control-restorefile.md)                     | Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad. Devuelve 1 si se ejecuta correctamente, 0 en caso de error.<br/>                                                                                                                                                                                                                                                        |
| [**RestoreFromTime**](control-restorefromtime.md)             | Restaure la configuración activa del recopilador a partir de un archivo de copia de seguridad, seleccionado por una marca de tiempo. Devuelve 1 si se ejecuta correctamente, 0 en caso de error.<br/>                                                                                                                                                                                                                               |
| [**SetConfiguration**](control-setconfiguration.md)           | Establezca la nueva configuración activa del recopilador. Devuelve 1 si se ejecuta correctamente, 0 en caso de error.<br/>                                                                                                                                                                                                                                                                           |
| [**Apagado**](control-shutdown.md)                           | Detenga el recopilador. Si el recopilador se ejecuta como un servicio, detener el servicio es el mejor enfoque.<br/>                                                                                                                                                                                                                                                     |
| [**Deshacer**](control-undo.md)                                   | Restaure la configuración activa del recopilador a partir del archivo de copia de seguridad anterior (determinado por volver de la marca de tiempo original actual). Si la configuración se acaba de establecer, significa deshacer ese cambio. Las llamadas consecutivas se deshacerán en las configuraciones anteriores y anteriores. Devuelve 1 si se ejecuta correctamente, 0 en caso de error.<br/>                           |
| [**ValidateConfiguration**](control-validateconfiguration.md) | Valide la corrección de un texto de configuración sin establecerlo en activo. Devuelve 1 si se ejecuta correctamente, 0 en caso de error.<br/>                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz \\ de Microsoft Windows \\ \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



 

 




