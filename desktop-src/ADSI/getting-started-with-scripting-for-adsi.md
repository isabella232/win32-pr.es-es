---
title: Tareas iniciales scripting para ADSI
description: El scripting es útil para los administradores del sistema que desean crear scripts por lotes para tareas usadas con frecuencia.
ms.assetid: ae479d6b-75cf-4659-8a91-c2cbdcf56091
ms.tgt_platform: multiple
keywords:
- Tareas iniciales scripting para ADSI ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a83da0194fb03cdb31430f389dbfbf64327806b1b142be3b9c1c5813696548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839958"
---
# <a name="getting-started-with-scripting-for-adsi"></a>Tareas iniciales scripting para ADSI

El scripting es útil para los administradores del sistema que desean crear scripts por lotes para tareas usadas con frecuencia.

Para iniciar el scripting con ADSI, debe tener un equipo que ejecute Windows o que haya iniciado sesión en un dominio que contenga datos para las cuentas de equipo del directorio.

## <a name="a-simple-scripting-sample-finding-names-and-locations-of-computer-accounts"></a>Un ejemplo de scripting simple: buscar nombres y ubicaciones de cuentas de equipo

Cree un nuevo archivo de texto mediante un editor de texto. En el ejemplo de código siguiente se muestra cómo buscar nombres y ubicaciones de cuentas de equipo.


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



Guarde el archivo como First.vbs. Modifique la línea que comienza por "objCommand.CommandText" para cambiar la ruta de acceso al dominio. En el símbolo del sistema, escriba **cscript First.vbs** para una línea de comandos o First.vbs para Windows scripting. Los resultados deben devolverse en el símbolo del sistema.

Para obtener más información sobre el scripting para ADSI, [vea Active Directory Service Interfaces Scripting](adsi-scripting-tutorial.md).

 

 




