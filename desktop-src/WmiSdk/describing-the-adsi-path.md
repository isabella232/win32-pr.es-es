---
description: El Protocolo ligero de acceso a directorios (LDAP) requiere que se escapen algunos caracteres con una barra diagonal inversa (carácter) cuando se usan en una ruta de \) acceso ldap Active Directory Service Interfaces (ADSI).
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Descripción de la ruta de acceso adsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0ba1dafac273ab3564549a5caca44180161643
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467271"
---
# <a name="describing-the-adsi-path"></a>Descripción de la ruta de acceso adsi

El Protocolo ligero de acceso a directorios (LDAP) requiere que se escapen algunos caracteres con un carácter de barra diagonal inversa ( ) cuando se usan en una ruta de acceso ldap \\ Active Directory Service Interfaces (ADSI).

,=+<>\# ; \\ "

El carácter de escape solo es necesario para el valor de la propiedad **ADSIPath.**

En el ejemplo siguiente se muestra cómo definir la **propiedad ADSIPath.** Tenga en cuenta que \# el carácter del valor de la propiedad **CN** de abc tiene caracteres \# de escape.


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
> Para obtener más información sobre la compatibilidad y la instalación de este componente en un sistema operativo específico, vea Disponibilidad del sistema operativo [de componentes WMI](operating-system-availability-of-wmi-components.md).

 

 

 



