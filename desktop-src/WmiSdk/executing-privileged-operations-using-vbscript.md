---
description: Si usa la API de scripting para WMI, puede establecer privilegios de seguridad específicos.
ms.assetid: 65b923d5-5244-498d-9644-d4978fb84f85
ms.tgt_platform: multiple
title: Ejecutar operaciones con privilegios mediante VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 13a7cf29aa444856e4da2fc9a73eeda0d8a3ccc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156821"
---
# <a name="executing-privileged-operations-using-vbscript"></a>Ejecutar operaciones con privilegios mediante VBScript

Si usa la API de scripting para WMI, puede establecer privilegios de seguridad específicos. Por ejemplo, puede establecer los privilegios de seguridad para solicitar un apagado del sistema operativo o para examinar el registro de eventos de seguridad. Para obtener más información, vea [ejecutar con privilegios especiales](/windows/desktop/SecBP/running-with-special-privileges).

Solo tiene que establecer privilegios cuando tenga acceso a WMI en el equipo. Cuando se tiene acceso a un host remoto, COM RPC establece automáticamente los privilegios. Para determinar todos los privilegios necesarios, consulte la documentación de las clases WMI específicas a las que desea obtener acceso, como por ejemplo, [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem). Para obtener más información, consulte [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)

En este tema se describen las siguientes secciones:

-   [Establecer un privilegio desde el objeto de seguridad \_](/windows)
-   [Establecer un privilegio como parte de un moniker](#setting-a-privilege-as-part-of-a-moniker)
-   [Revocar y restablecer privilegios](#revoking-and-resetting-privileges)
-   [Temas relacionados](#related-topics)

## <a name="setting-a-privilege-from-the-security_-object"></a>Establecer un privilegio desde el objeto de seguridad \_

Utilice el procedimiento siguiente para establecer privilegios de seguridad en Visual Basic.

**Para establecer privilegios en Visual Basic**

1.  Cree un objeto de tipo [**SWbemLocator**](swbemlocator.md).
2.  Agregue el nuevo privilegio al objeto [**SWbemLocator. Security \_**](swbemlocator-security-.md) .

    El objeto de [**seguridad \_**](swbemlocator-security-.md) contiene una colección [**SWbemObjectSet**](swbemobjectset.md) . Los objetos del conjunto son objetos [**SWbemSecurity**](swbemsecurity.md) . Para obtener más información, vea [obtener acceso a una colección](accessing-a-collection.md).

3.  Inicie sesión en WMI y recupere un objeto [**SWbemServices**](swbemservices.md) .

    El objeto [**SWbemServices**](swbemservices.md) hereda el privilegio que se establece en el paso anterior.

También puede establecer un privilegio mediante el método [**SWbemPrivilegeSet. AddAsString**](swbemprivilegeset-addasstring.md) .

## <a name="setting-a-privilege-as-part-of-a-moniker"></a>Establecer un privilegio como parte de un moniker

Puede establecer un privilegio como parte de un moniker.

En el ejemplo siguiente se muestra cómo agregar un privilegio de depuración a un moniker.


```VB
Set Service = GetObject("winmgmts:{impersonationLevel=impersonate, (Debug)}")
```



## <a name="revoking-and-resetting-privileges"></a>Revocar y restablecer privilegios

En el ejemplo siguiente se muestra cómo establecer el privilegio **SeDebugPrivilege** y revocar el privilegio **SeRemoteShutdownPrivilege** .


```VB
Set Service = GetObject("winmgmts:{impersonate,(Debug,!RemoteShutdown)}")
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Constantes de privilegio**](privilege-constants.md)
</dt> <dt>

[Ejecutar operaciones con privilegios](executing-privileged-operations.md)
</dt> </dl>

 

 
