---
description: El Protocolo ligero de acceso a directorios (LDAP) requiere que se escapen algunos caracteres con una barra diagonal inversa (carácter) cuando se usan en una ruta de acceso de \) LDAP Active Directory Service Interfaces (ADSI).
ms.assetid: bc04359c-4eda-4574-a9c2-f005a1d92dea
ms.tgt_platform: multiple
title: Descripción de la ruta de acceso adsi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0ba1dafac273ab3564549a5caca44180161643
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387114"
---
# <a name="describing-the-adsi-path"></a><span data-ttu-id="7c304-103">Descripción de la ruta de acceso adsi</span><span class="sxs-lookup"><span data-stu-id="7c304-103">Describing the ADSI Path</span></span>

<span data-ttu-id="7c304-104">El Protocolo ligero de acceso a directorios (LDAP) requiere que se escapen algunos caracteres con un carácter de barra diagonal inversa ( ) cuando se usan en una ruta de acceso de \\ LDAP Active Directory Service Interfaces (ADSI).</span><span class="sxs-lookup"><span data-stu-id="7c304-104">The Lightweight Directory Access Protocol (LDAP) requires that you escape some characters with a backslash (\\) character when you use them in an LDAP Active Directory Service Interfaces (ADSI) path.</span></span>

<span data-ttu-id="7c304-105">,=+<>\# ; \\ "</span><span class="sxs-lookup"><span data-stu-id="7c304-105">,=+<>\#;\\"</span></span>

<span data-ttu-id="7c304-106">El carácter de escape solo es necesario para el valor de la propiedad **ADSIPath.**</span><span class="sxs-lookup"><span data-stu-id="7c304-106">The escape character is only required for the **ADSIPath** property value.</span></span>

<span data-ttu-id="7c304-107">En el ejemplo siguiente se muestra cómo definir la **propiedad ADSIPath.**</span><span class="sxs-lookup"><span data-stu-id="7c304-107">The following example shows how to define the **ADSIPath** property.</span></span> <span data-ttu-id="7c304-108">Tenga en cuenta que \# el carácter del valor de la propiedad **CN** de abc tiene caracteres \# de escape.</span><span class="sxs-lookup"><span data-stu-id="7c304-108">Note that the \# character in the **CN** property value of abc\# is escaped.</span></span>


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
> <span data-ttu-id="7c304-109">Para obtener más información sobre la compatibilidad y la instalación de este componente en un sistema operativo específico, vea Disponibilidad del sistema operativo [de componentes WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="7c304-109">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



