---
title: Detectar si el rol Servicios de Escritorio remoto está instalado
description: Ejemplo de código C\ que muestra un método que devuelve True si el rol de servidor Servicios de Escritorio remoto está instalado y en ejecución o false en caso contrario, a partir de Windows Server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cf7ac1932c32ea797783d04f4e279bab03339c9b7620c11e72d4b755f084736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871765"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>Detectar si el rol Servicios de Escritorio remoto está instalado

Puede usar la clase [**WMI \_ ServerFeature de Win32**](/windows/desktop/WmiSdk/win32-serverfeature) para detectar si el rol Servicios de Escritorio remoto servidor está instalado.

En el siguiente ejemplo de C# se muestra un método que devuelve **True** si el rol de servidor Servicios de Escritorio remoto está instalado y en ejecución o **false** de lo contrario. Dado que la clase WMI [**\_ ServerFeature de Win32**](/windows/desktop/WmiSdk/win32-serverfeature) solo está disponible a partir de Windows Server 2008, este código no es compatible con versiones anteriores de Windows.


```CSharp
static void Main(string[] args)
{
    // 14 is the identifier of the Remote Desktop Services role.
    HasServerFeatureById(14);
}

static bool HasServerFeatureById(UInt32 roleId)
{
    try
    {
        ManagementClass serviceClass = new ManagementClass("Win32_ServerFeature");
        foreach (ManagementObject feature in serviceClass.GetInstances())
        {
            if ((UInt32)feature["ID"] == roleId)
            {
                return true;
            }
        }

        return false;
    }
    catch (ManagementException)
    {
        // The most likely cause of this is that this is being called from an 
        // operating system that is not a server operating system.
    }

    return false;
}

```



 

 