---
description: El método EnableLog del objeto de instalador habilita el registro del tipo de mensaje seleccionado para todas las sesiones de instalación posteriores en el espacio de proceso actual.
ms.assetid: eb384587-0870-4812-866c-b483c1dfa841
title: Instalador. EnableLog (método)
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
ms.openlocfilehash: 573b56dda0479f58595b0849f6443fd8a2e67e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653355"
---
# <a name="installerenablelog-method"></a>Instalador. EnableLog (método)

El método **EnableLog** del objeto de [**instalador**](installer-object.md) habilita el registro del tipo de mensaje seleccionado para todas las sesiones de instalación posteriores en el espacio de proceso actual.

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

Cadena requerida que contiene letras que representan los tipos de mensaje que se van a registrar. La cadena puede ser una combinación de los valores siguientes.



| Value | Descripción                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| I     | Mensajes de solo información.                                                                             |
| w     | Mensajes de advertencia no graves.                                                                            |
| h     | Mensajes de error que pueden ser errores irrecuperables.                                                               |
| f     | Lista de archivos en uso que se deben reemplazar.                                                         |
| a     | Inicio de la notificación de acción.                                                                          |
| r     | Registro de datos de acción que contiene contenido específico de la acción.                                              |
| u     | Mensajes de solicitud de usuario.                                                                                 |
| c     | Parámetros de inicialización de la interfaz de usuario.                                                                          |
| m     | Mensaje de memoria insuficiente.                                                                                 |
| v     | Envía grandes cantidades de información al archivo de registro que no suele ser útil para los usuarios. Se puede usar para la compatibilidad. |
| p     | Tabla de propiedades dump; "propiedad = valor" al finalizar el motor                                          |
| \+    | Anexar al archivo de registro existente.                                                                           |
| !     | Vacíe cada línea en el archivo de registro.                                                                       |
| x     | Información de depuración adicional. Esta opción solo está disponible en Windows Server 2003.                      |
| o     | Mensajes de espacio insuficiente en disco.                                                                            |



 

</dd> <dt>

*MSDTC* 
</dt> <dd>

Cadena requerida que contiene la ruta de acceso al archivo de registro que se va a crear. Use una cadena vacía ("") para desactivar el registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La ruta de acceso a la ubicación del archivo de registro ya debe existir al utilizar este método. El instalador no crea la estructura de directorios para el archivo de registro.

Las opciones de registro establecidas mediante **EnableLog** invalidan cualquier configuración existente de la Directiva de registro de Windows Installer.

De forma predeterminada, el registro sobrescribe un archivo de registro existente. Debe usar la letra ' + ' en el modo de registro para anexar a un archivo de registro existente.

No se recomienda la opción '! ' porque puede ralentizar considerablemente la instalación. Esta opción puede ser útil al depurar una instalación de.

El siguiente script de ejemplo activa el registro detallado para una instalación de. Al final de la instalación, el archivo de registro generado estará en c: \\ temp \\ install. log.


```VB
    Dim Installer
    Set Installer = CreateObject("WindowsInstaller.Installer")
    Installer.EnableLog "voicewarmup", "c:\temp\install.log"
    Installer.InstallProduct "\\server\share\products\sample\sample.msi"
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Registro de Windows Installer](windows-installer-logging.md)
</dt> </dl>

 

 




