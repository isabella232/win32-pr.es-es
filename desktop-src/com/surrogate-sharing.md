---
title: Uso compartido de suplentes
description: Los servidores DLL compartirán un suplente si tienen identidades de seguridad coincidentes y comparten el mismo valor de AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774959"
---
# <a name="surrogate-sharing"></a>Uso compartido de suplentes

Los servidores DLL compartirán un suplente si tienen identidades de seguridad coincidentes y comparten el mismo valor de AppID.

Los servidores DLL se cargan, de forma predeterminada, en su propio proceso suplente. Para cargar otros servidores DLL en un suplente existente para que admita más de un servidor DLL, existen dos requisitos:

-   Los servidores DLL deben tener el mismo valor de AppID.
-   El contexto de seguridad de los servidores DLL debe ser el mismo.

Si se van a iniciar dos servidores DLL con distintas identidades de seguridad, deben estar en distintos suplentes, independientemente de que AppIDs coincidan.

A continuación se proporciona un ejemplo de cómo administrar el uso compartido de suplentes con AppIDs:

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

Los dos CLSID para componentes DLL comp1.dll y comp2.dll se han configurado para compartir un AppID. La clave [AppID](appid-key.md) especifica que el servidor dll se puede cargar en un suplente especificando el valor de [DllSurrogate](dllsurrogate.md) . En este ejemplo, el valor de **DllSurrogate** es una cadena vacía, que indica que se debe usar la implementación del sistema predeterminada del suplente de la dll.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Requisitos del servidor DLL](dll-server-requirements.md)
</dt> <dt>

[Registrando el servidor DLL para la activación de suplentes](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




