---
description: El Protocolo ligero de acceso a directorios (LDAP) requiere que se escapen algunos caracteres con una barra diagonal inversa ( \) carácter cuando se utilizan en una ruta de acceso de las interfaces de servicio Active Directory LDAP (ADSI).
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Descripción de la ruta de acceso ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6f3f28ffa5faa80dbd9f3d7906bba542e47e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544838"
---
# <a name="describing-the-adsi-path"></a>Descripción de la ruta de acceso ADSI

El Protocolo ligero de acceso a directorios (LDAP) requiere que se escapen algunos caracteres con una barra diagonal inversa ( \) carácter cuando se utilizan en una ruta de acceso de las interfaces de servicio Active Directory LDAP (ADSI).

, = +<>\# ; \\ "

El carácter de escape solo es necesario para el valor de la propiedad **ADSIPath** .

En el ejemplo siguiente se muestra cómo definir la propiedad **ADSIPath** . Tenga en cuenta que el \# carácter del valor de la propiedad **CN** de ABC es un carácter de \# escape.


```C++
// #include <windows.h> for this code to compile

BSTR strObjPath = 
    SysAllocString(L"ds_user.ADSIPath=\"LDAP://CN=abc\#,"
                   L"CN=Users,DC=dsprovider,DC=nttest,"
                   L"DC=microsoft,DC=com\"");

// Use strObjectPath here.

SysFreeString(strObjPath); // Free memory resources.
```



> [!Note]  
> Para obtener más información acerca de la compatibilidad y la instalación de este componente en un sistema operativo específico, consulte [disponibilidad del sistema operativo de los componentes de WMI](operating-system-availability-of-wmi-components.md).

 

 

 



