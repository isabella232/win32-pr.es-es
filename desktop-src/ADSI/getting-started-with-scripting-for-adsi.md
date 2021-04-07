---
title: Introducción con scripting para ADSI
description: El scripting es útil para los administradores del sistema que quieren crear scripts por lotes para tareas de uso frecuente.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- Introducción con scripting para ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8a85a9ea110ca80f45c3a0f0f1917e8d25c08ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993853"
---
# <a name="getting-started-with-scripting-for-adsi"></a>Introducción con scripting para ADSI

El scripting es útil para los administradores del sistema que quieren crear scripts por lotes para tareas de uso frecuente.

Para iniciar la secuencia de comandos con ADSI, debe tener un equipo que ejecute Windows o que inicie sesión en un dominio que contenga los datos de las cuentas de equipo en el directorio.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Ejemplo sencillo de scripting: búsqueda de nombres y ubicaciones de cuentas de equipo

Cree un nuevo archivo de texto con un editor de texto. En el ejemplo de código siguiente se muestra cómo buscar los nombres y las ubicaciones de las cuentas de equipo.


```VB
'---------------------------------------------------------------
' Returns the name and location for all the computer accounts in 
' Active Directory.
'--------------------------------------------------------------- 
Const ADS_SCOPE_SUBTREE = 2
Set objConnection = CreateObject("ADODB.Connection")
Set objCommand =   CreateObject("ADODB.Command")
objConnection.Provider = "ADsDSOObject"
objConnection.Open "Active Directory Provider"
Set objCommand.ActiveConnection = objConnection
objCommand.CommandText = "Select Name, Location from 'LDAP://DC=fabrikam,DC=com' " & "where objectClass='computer'"  
objCommand.Properties("Page Size") = 1000
objCommand.Properties("Timeout") = 30 
objCommand.Properties("Searchscope") = ADS_SCOPE_SUBTREE 
objCommand.Properties("Cache Results") = False 
Set objRecordSet = objCommand.Execute
objRecordSet.MoveFirst
Do Until objRecordSet.EOF
    Wscript.Echo "Computer Name: " & objRecordSet.Fields("Name").Value
    Wscript.Echo "Location: " & objRecordSet.Fields("Location").Value
    objRecordSet.MoveNext
Loop
```



Guarde el archivo como First.vbs. Modifique la línea que comienza por "objCommand. CommandText" para cambiar la ruta de acceso a su dominio. En el símbolo del sistema, escriba **cscript First.vbs** para una línea de comandos o First.vbs para Windows Scripting. Los resultados se deben devolver en el símbolo del sistema.

Para obtener más información sobre el scripting para ADSI, vea [Active Directory scripting de interfaces de servicio](adsi-scripting-tutorial.md).

 

 




