---
description: Las operaciones con privilegios requieren privilegios de seguridad como SeLoadDriverPrivilege (wbemPrivilegeLoadDriver en las constantes de API de scripting), privilegio que debe habilitarse para una cuenta que carga un controlador de dispositivo.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Ejecución de operaciones con privilegios
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965292"
---
# <a name="executing-privileged-operations"></a>Ejecución de operaciones con privilegios

Las operaciones con privilegios requieren [privilegios](scripting-api-constants.md)de seguridad como **SeLoadDriverPrivilege** **(wbemPrivilegeLoadDriver en** las constantes de API de scripting), privilegio que debe habilitarse para una cuenta que carga un controlador de dispositivo. No puede agregar privilegios a un administrador o usuario a través de WMI, solo puede habilitar los privilegios que ya tiene la cuenta. Para obtener una lista de privilegios, vea [**Constantes \_ de privilegios**](privilege-constants.md).

De forma predeterminada, un usuario local de un equipo puede leer datos estáticos del repositorio [*WMI,*](gloss-w.md)escribir en instancias proporcionadas por proveedores y ejecutar métodos de proveedor, a menos que el proveedor exija requisitos de seguridad especiales propios. Solo los administradores pueden [conectarse a](connecting-to-wmi-on-a-remote-computer.md)un equipo remoto, cambiar descriptores de seguridad o cambiar datos estáticos del repositorio WMI, como una definición de clase WMI. Todos los privilegios están habilitados para una conexión remota. Para obtener más información, [vea Proteger una conexión WMI remota.](securing-a-remote-wmi-connection.md)

Las constantes de privilegios para C++ difieren de las que usan lenguajes de automatización como Visual Basic. Los scripts deben usar el valor de la constante en lugar del nombre. Para obtener más información, [vea Ejecutar operaciones con privilegios mediante C++](executing-privileged-operations-using-c-.md) o Ejecutar operaciones con [privilegios mediante VBScript](executing-privileged-operations-using-vbscript.md).

Una causa común de errores de acceso denegado al usar WMI es la falta de un privilegio habilitado para las operaciones, como obtener todas las instancias de [**\_ NTEventlogFile de Win32.**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)) Sin habilitar el **privilegio SeSecurity,** no se puede acceder al archivo de registro de seguridad.

En el ejemplo de código de VBScript siguiente se muestra cómo establecer el **privilegio SeSecurity** en la cadena de moniker. Cuando se usa en el moniker, el nombre de privilegio entre paréntesis quita la "Se" inicial. Para obtener más información, [vea Constructing a Moniker String](constructing-a-moniker-string.md).


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

[**Constantes de privilegios**](privilege-constants.md)
</dt> </dl>

 

 
