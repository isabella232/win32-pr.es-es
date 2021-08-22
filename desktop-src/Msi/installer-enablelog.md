---
description: El método EnableLog del objeto Installer habilita el registro del tipo de mensaje seleccionado para todas las sesiones de instalación posteriores en el espacio de proceso actual.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Método Installer.EnableLog
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.EnableLog
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 48481a701b7e78de372f5579dab5c9d5976a68063958b0812d6ae1ddc08b109a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631701"
---
# <a name="installerenablelog-method"></a>Método Installer.EnableLog

El **método EnableLog** del objeto [**Installer**](installer-object.md) habilita el registro del tipo de mensaje seleccionado para todas las sesiones de instalación posteriores en el espacio de proceso actual.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.EnableLog(
  logMode,
  logFile
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*logMode* 
</dt> <dd>

Cadena necesaria que contiene letras que representan los tipos de mensaje que se registrarán. La cadena puede ser una combinación de los valores siguientes.



| Valor | Descripción                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | Mensajes de solo información.                                                                             |
| w     | Mensajes de advertencia no irreales.                                                                            |
| e     | Mensajes de error que pueden ser errores irreales.                                                               |
| f     | Lista de archivos en uso que deben reemplazarse.                                                         |
| a     | Notificación de inicio de acción.                                                                          |
| r     | Registro de datos de acción que contiene contenido específico de la acción.                                              |
| u     | Mensajes de solicitud de usuario.                                                                                 |
| c     | Parámetros de inicialización de la interfaz de usuario.                                                                          |
| m     | Mensaje de memoria fuera de memoria.                                                                                 |
| v     | Envía grandes cantidades de información al archivo de registro que no suele ser útil para los usuarios. Se puede usar para soporte técnico. |
| p     | Tabla de propiedades dump; "property = value" al finalizar el motor                                          |
| \+    | Anexe al archivo de registro existente.                                                                           |
| !     | Vacíe cada línea en el archivo de registro.                                                                       |
| x     | Información de depuración adicional. Esta opción solo está disponible con Windows Server 2003.                      |
| o     | Mensajes de espacio fuera del disco.                                                                            |



 

</dd> <dt>

*Logfile* 
</dt> <dd>

Cadena necesaria que contiene la ruta de acceso al archivo de registro que se va a crear. Use una cadena vacía ("") para desactivar el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La ruta de acceso a la ubicación del archivo de registro ya debe existir cuando se usa este método. El instalador no crea la estructura de directorios para el archivo de registro.

Las opciones de registro establecidas mediante **EnableLog** invalidan cualquier configuración de directiva de registro Windows instalador existente.

El registro sobrescribe un archivo de registro existente de forma predeterminada. Debe usar la letra "+" en el modo de registro para anexar a un archivo de registro existente.

No se recomienda la opción "!" porque puede ralentizar considerablemente la instalación. Esta opción puede ser útil al depurar una instalación.

El siguiente script de ejemplo activa el registro detallado para una instalación. Al final de la instalación, el archivo de registro generado estará en c: \\ temp \\ install.log.


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Registro del instalador](windows-installer-logging.md)
</dt> </dl>

 

 




