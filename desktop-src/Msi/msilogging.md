---
description: La propiedad MsiLogging establece el modo de registro predeterminado para el Windows installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: MsiLogging, propiedad
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074380"
---
# <a name="msilogging-property"></a>MsiLogging, propiedad

La **propiedad MsiLogging** establece el modo de registro predeterminado para el paquete Windows Installer. Si esta propiedad opcional está presente en la [tabla Property](property-table.md), el instalador genera un archivo de registro denominado \* MSI. REGISTRO. El valor de la propiedad [**MsiLogFileLocation**](msilogfilelocation.md) proporciona la ruta de acceso completa al archivo de registro.

## <a name="value"></a>Value

El valor de esta propiedad debe ser una cadena de los caracteres siguientes que especifican el modo de registro predeterminado.



| Value                                                                        | Significado                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>I</dt> </dl> | Mensajes de estado.<br/>                                                    |
| <dl> <dt>w</dt> </dl> | Advertencias nofatales.<br/>                                                  |
| <dl> <dt>e</dt> </dl> | Todos los mensajes de error.<br/>                                                 |
| <dl> <dt>Un</dt> </dl> | Inicio de acciones.<br/>                                                |
| <dl> <dt>r</dt> </dl> | Registros específicos de la acción.<br/>                                            |
| <dl> <dt>u</dt> </dl> | Solicitudes de usuario.<br/>                                                      |
| <dl> <dt>c</dt> </dl> | Parámetros iniciales de la interfaz de usuario.<br/>                                              |
| <dl> <dt>m</dt> </dl> | Información de salida irreales o de memoria fuera de memoria.<br/>                            |
| <dl> <dt>o</dt> </dl> | Mensajes de espacio fuera del disco.<br/>                                         |
| <dl> <dt>P</dt> </dl> | Propiedades del terminal.<br/>                                                |
| <dl> <dt>V</dt> </dl> | Salida detallada.<br/>                                                     |
| <dl> <dt>x</dt> </dl> | Información de depuración adicional. Solo está disponible en Windows Server 2003.<br/> |
| <dl> <dt>!</dt> </dl> | Vacíe cada línea en el registro.<br/>                                         |



 

## <a name="remarks"></a>Observaciones

Esta propiedad está disponible a partir de Windows Installer 4.0.

No puede usar los valores "+" y " " de \* la opción /L en el valor de la **propiedad MsiLogging.**

El modo de registro se puede establecer mediante directiva, una opción de línea de comandos o mediante programación. Esto invalida el modo de registro predeterminado. Para obtener más información sobre todos los métodos que están disponibles para establecer el modo de registro, vea [Registro normal](normal-logging.md) en la [Windows registro](windows-installer-logging.md) del instalador.

Si la **propiedad MsiLogging** está presente en la tabla [Property](property-table.md), el modo de registro predeterminado del paquete se puede modificar cambiando el valor de esta propiedad mediante una transformación de base [de datos](database-transforms.md). El modo de registro predeterminado no se puede cambiar mediante un [paquete de revisión](patch-packages.md) (un archivo .msp).

Si la propiedad **MsiLogging** se ha establecido en la tabla [Property](property-table.md), se puede especificar el modo de registro predeterminado para todos los usuarios del equipo estableciendo la directiva [DisableLoggingFromPackage](disableloggingfrompackage.md) y la directiva [de](logging.md) registro. Si se establece la directiva DisableLoggingFromPackage y la directiva de registro, se invalidará **la propiedad MsiLogging** para todos los paquetes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una Windows installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




