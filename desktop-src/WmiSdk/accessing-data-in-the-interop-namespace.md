---
description: Los proveedores de asociación permiten a los clientes de Instrumental de administración de Windows (WMI) atravesar y recuperar perfiles y las instancias de clase asociadas de distintos espacios de nombres.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Obtener acceso a los datos en el espacio de nombres Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002832"
---
# <a name="accessing-data-in-the-interop-namespace"></a>Obtener acceso a los datos en el espacio de nombres Interop

Los proveedores de asociación permiten a los clientes de Instrumental de administración de Windows (WMI) atravesar y recuperar perfiles y las instancias de clase asociadas de distintos espacios de nombres.

Los proveedores y las clases de asociación residen en el \\ \\ espacio de nombres de \\ interoperabilidad raíz. Para obtener más información, vea cruce seguro de la [asociación entre espacios de nombres](cross-namespace-association-traversal.md) y [escritura de un proveedor de asociaciones](writing-an-association-provider-for-interop.md).

Los proveedores de asociación exponen perfiles estándar, como un perfil de energía. En los ejemplos siguientes se usa el perfil de energía para mostrar cómo detectar y obtener acceso a los datos a través del espacio de nombres de interoperabilidad.

Windows PowerShell proporciona un mecanismo sencillo para atravesar la Asociación adecuada, recuperar un perfil de dispositivo y llamar a un método.

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>Enumerar perfiles en el espacio de nombres root/Interop

El siguiente comando de Windows PowerShell enumera los perfiles compatibles con el forzado de la tarea de administración distribuida ([DMTF](https://www.dmtf.org/standards/wsman)) en un equipo con Windows 7:


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>Recuperación de instancias de un perfil de dispositivo específico

El siguiente comando de Windows PowerShell devuelve todas las instancias de un perfil especificado a través de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>Asignación del perfil de energía a una variable

El siguiente comando de Windows PowerShell asigna la instancia de Perfil de energía a una variable:


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>Enumerar los planes de energía de un equipo

El siguiente comando de Windows PowerShell enumera los planes de Perfil de energía disponibles:


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>Llamar a un método

El siguiente comando de Windows PowerShell llama al método [**Activar**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) para el plan de energía:


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cruce seguro de la asociación entre espacios de nombres](cross-namespace-association-traversal.md)
</dt> <dt>

[Escribir un proveedor de asociación](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**\_REGISTEREDPROFILE CIM**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**Win32 \_ PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
