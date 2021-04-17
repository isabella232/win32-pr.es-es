---
description: La propiedad MsiLogging establece el modo de registro predeterminado para el paquete de Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Propiedad MsiLogging
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681044"
---
# <a name="msilogging-property"></a>Propiedad MsiLogging

La propiedad **MsiLogging** establece el modo de registro predeterminado para el paquete de Windows Installer. Si esta propiedad opcional está presente en la [tabla de propiedades](property-table.md), el instalador genera un archivo de registro denominado MSI \* . Inicia. La ruta de acceso completa al archivo de registro se proporciona mediante el valor de la propiedad [**MsiLogFileLocation**](msilogfilelocation.md) .

## <a name="value"></a>Value

El valor de esta propiedad debe ser una cadena de los siguientes caracteres que especifican el modo de registro predeterminado.



| Value                                                                        | Significado                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>I</dt> </dl> | Mensajes de estado.<br/>                                                    |
| <dl> <dt>w</dt> </dl> | Advertencias no graves.<br/>                                                  |
| <dl> <dt>e</dt> </dl> | Todos los mensajes de error.<br/>                                                 |
| <dl> <dt>un</dt> </dl> | Inicio de acciones.<br/>                                                |
| <dl> <dt>r</dt> </dl> | Registros específicos de la acción.<br/>                                            |
| <dl> <dt>u</dt> </dl> | Solicitudes de usuario.<br/>                                                      |
| <dl> <dt>c</dt> </dl> | Parámetros iniciales de la interfaz de usuario.<br/>                                              |
| <dl> <dt>m</dt> </dl> | Memoria insuficiente o información de salida irrecuperable.<br/>                            |
| <dl> <dt>o</dt> </dl> | Mensajes de espacio insuficiente en disco.<br/>                                         |
| <dl> <dt>m</dt> </dl> | Propiedades de terminal.<br/>                                                |
| <dl> <dt>v</dt> </dl> | Salida detallada.<br/>                                                     |
| <dl> <dt>x</dt> </dl> | Información de depuración adicional. Solo disponible en Windows Server 2003.<br/> |
| <dl> <dt>!</dt> </dl> | Vacíe cada línea en el registro.<br/>                                         |



 

## <a name="remarks"></a>Observaciones

Esta propiedad está disponible a partir de Windows Installer 4,0.

No se pueden usar los valores "+" y " \* " de la opción/l en el valor de la propiedad **MsiLogging** .

El modo de registro se puede establecer mediante una directiva, una opción de línea de comandos o mediante programación. Esto invalida el modo de registro predeterminado. Para obtener más información acerca de todos los métodos que están disponibles para establecer el modo de registro, consulte el [registro normal](normal-logging.md) en la sección [registro de Windows Installer](windows-installer-logging.md) .

Si la propiedad **MsiLogging** está presente en la [tabla de propiedades](property-table.md), el modo de registro predeterminado del paquete se puede modificar cambiando el valor de esta propiedad mediante una [transformación de base de datos](database-transforms.md). El modo de registro predeterminado no se puede cambiar mediante un [paquete de revisión](patch-packages.md) (un archivo. msp).

Si se ha establecido la propiedad **MsiLogging** en la [tabla de propiedades](property-table.md), se puede especificar el modo de registro predeterminado para todos los usuarios del equipo mediante el establecimiento de la Directiva de [DisableLoggingFromPackage](disableloggingfrompackage.md) y la Directiva de [registro](logging.md) . El establecimiento de la Directiva DisableLoggingFromPackage y de la Directiva de registro reemplazará la propiedad **MsiLogging** de todos los paquetes.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 4,5 en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> <dt>

[No se admite en Windows Installer 3,1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




