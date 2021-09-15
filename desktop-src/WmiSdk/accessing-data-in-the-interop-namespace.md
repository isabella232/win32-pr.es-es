---
description: Los proveedores de asociación permiten Windows de Instrumental de administración de recursos (WMI) atraviesan y recuperan perfiles e instancias de clase asociadas de distintos espacios de nombres.
ms.assetid: 00c654d1-a5de-40c5-a190-99382949486a
ms.tgt_platform: multiple
title: Acceso a datos en el espacio de nombres Interop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a217a7a44651b1a6c94476b53193eedac7f0d43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465782"
---
# <a name="accessing-data-in-the-interop-namespace"></a>Acceso a datos en el espacio de nombres Interop

Los proveedores de asociación permiten Windows de Instrumental de administración de recursos (WMI) atraviesan y recuperan perfiles e instancias de clase asociadas de distintos espacios de nombres.

Los proveedores y clases de asociación residen en el espacio \\ \\ de nombres de \\ interoperabilidad raíz. Para obtener más información, vea [Cross Namespace Association Traversal (Recorrido de asociación entre espacios de](cross-namespace-association-traversal.md) nombres) y Writing an Association Provider [(Escribir un proveedor de asociaciones).](writing-an-association-provider-for-interop.md)

Los proveedores de asociaciones exponen perfiles estándar, como un perfil de energía. En los ejemplos siguientes se usa el perfil de energía para ilustrar cómo detectar y acceder a los datos a través del espacio de nombres de interoperabilidad.

Windows PowerShell proporciona un mecanismo sencillo para recorrer la asociación adecuada, recuperar un perfil de dispositivo y llamar a un método.

## <a name="enumerating-profiles-in-the-rootinterop-namespace"></a>Enumeración de perfiles en el espacio de nombres root/interop

El siguiente comando Windows PowerShell enumera los perfiles admitidos por el Grupo de tareas de administración distribuida[(DMTF)](https://www.dmtf.org/standards/wsman)en un Windows 7:


```PowerShell
Get-WmiObject CIM_RegisteredProfile  -namespace root\interop
```



## <a name="retrieving-instances-of-a-specific-device-profile"></a>Recuperación de instancias de un perfil de dispositivo específico

El siguiente comando Windows PowerShell devuelve todas las instancias de un perfil especificado a través de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)):


```PowerShell
Get-WmiObject -namespace root\interop -query "Associators of {CIM_RegisteredProfile.InstanceID='Power Supply'}"
```



## <a name="assigning-the-power-profile-to-a-variable"></a>Asignación del perfil de energía a una variable

El siguiente Windows PowerShell asigna la instancia del perfil de energía a una variable:


```PowerShell
$pplan = Get-WmiObject -query "Select * from Win32_PowerPlan" -Namespace root\cimv2\power
```



## <a name="enumerating-the-power-plans-on-a-computer"></a>Enumeración de los planes de energía en un equipo

El siguiente Windows PowerShell enumera los planes de perfil de energía disponibles:


```PowerShell
$pplan
```



## <a name="calling-a-method"></a>Llamar a un método

El siguiente comando Windows PowerShell llama al [**método Activate**](/previous-versions/windows/desktop/powerwmiprov/activate-win32-powerplan) para el plan de energía:


```PowerShell
$pplan[2].Activate()
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recorrido de asociación entre espacios de nombres](cross-namespace-association-traversal.md)
</dt> <dt>

[Escribir un proveedor de asociación](writing-an-association-provider-for-interop.md)
</dt> <dt>

[**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))
</dt> <dt>

[**Win32 \_ PowerPlan**](/previous-versions/windows/desktop/legacy/dd904531(v=vs.85))
</dt> </dl>

 

 
