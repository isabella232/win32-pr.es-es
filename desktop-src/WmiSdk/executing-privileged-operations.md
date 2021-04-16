---
description: Las operaciones con privilegios requieren privilegios de seguridad como SeLoadDriverPrivilege (wbemPrivilegeLoadDriver en las constantes de API de scripting), un privilegio que debe habilitarse para una cuenta que está cargando un controlador de dispositivo.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Ejecutar operaciones con privilegios
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706156"
---
# <a name="executing-privileged-operations"></a>Ejecutar operaciones con privilegios

Las operaciones con privilegios requieren privilegios de seguridad como **SeLoadDriverPrivilege** (**WbemPrivilegeLoadDriver** en las [constantes de API de scripting](scripting-api-constants.md)), un privilegio que debe habilitarse para una cuenta que está cargando un controlador de dispositivo. No puede Agregar privilegios a un administrador o usuario a través de WMI, solo puede habilitar los privilegios que la cuenta ya tiene. Para obtener una lista de privilegios, [**consulte \_ constantes de privilegios**](privilege-constants.md).

De forma predeterminada, un usuario local de un equipo puede leer datos estáticos del [*repositorio WMI*](gloss-w.md), escribir en instancias proporcionadas por los proveedores y ejecutar métodos de proveedor, a menos que el proveedor aplique requisitos de seguridad especiales por sí solos. Solo los administradores pueden [conectarse a un equipo remoto](connecting-to-wmi-on-a-remote-computer.md), cambiar los descriptores de seguridad o cambiar los datos estáticos del repositorio WMI, como una definición de clase WMI. Todos los privilegios están habilitados para una conexión remota. Para obtener más información, consulte [protección de una conexión WMI remota](securing-a-remote-wmi-connection.md).

Las constantes de privilegios de C++ difieren de las que se usan en los lenguajes de automatización como Visual Basic. Los scripts deben usar el valor de la constante en lugar del nombre. Para obtener más información, vea [ejecutar operaciones con privilegios mediante C++](executing-privileged-operations-using-c-.md) o [ejecutar operaciones con privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md).

Una causa común de los errores de acceso denegado cuando se usa WMI es la falta de un privilegio habilitado para las operaciones, como obtener todas las instancias de [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)). Sin habilitar el privilegio **SeSecurity** , no se puede tener acceso al archivo de registro de seguridad.

En el ejemplo de código de VBScript siguiente se muestra cómo establecer el privilegio **SeSecurity** en la cadena de moniker. Cuando se usa en el moniker, el nombre de privilegio entre paréntesis quita el "se" inicial. Para obtener más información, vea [crear una cadena de moniker](constructing-a-moniker-string.md).


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de privilegio**](privilege-constants.md)
</dt> </dl>

 

 
