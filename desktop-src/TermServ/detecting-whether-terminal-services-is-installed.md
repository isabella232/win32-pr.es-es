---
title: Detectar si está instalado el rol de Servicios de Escritorio remoto
description: C \ ejemplo de código que muestra un método que devuelve true si la función de servidor Servicios de Escritorio remoto está instalada y en ejecución, o false en caso contrario, a partir de Windows Server 2008.
ms.assetid: 53ef8d43-2141-4df7-b9e6-baf0677924ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49f7d094f88271346c97f8d0467b48a266c865d5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421186"
---
# <a name="detecting-whether-the-remote-desktop-services-role-is-installed"></a>Detectar si está instalado el rol de Servicios de Escritorio remoto

Puede usar la clase [**WMI \_ ServerFeature de Win32**](/windows/desktop/WmiSdk/win32-serverfeature) para detectar si está instalado el rol de servidor servicios de escritorio remoto.

En el siguiente ejemplo de C# se muestra un método que devuelve **true** si la función de servidor servicios de escritorio remoto está instalada y en ejecución, o bien **false** en caso contrario. Dado que la clase WMI [**\_ ServerFeature de Win32**](/windows/desktop/WmiSdk/win32-serverfeature) solo está disponible a partir de Windows Server 2008, este código no es compatible con versiones anteriores de Windows.


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



 

 