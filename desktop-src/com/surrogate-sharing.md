---
title: Uso compartido suplente
description: Los servidores DLL compartirán un suplente si tienen identidades de seguridad que coincidan y comparten el mismo valor de AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127253167"
---
# <a name="surrogate-sharing"></a>Uso compartido suplente

Los servidores DLL compartirán un suplente si tienen identidades de seguridad que coincidan y comparten el mismo valor de AppID.

Los servidores DLL se cargan, de forma predeterminada, en su propio proceso suplente. Para cargar otros servidores DLL en un suplente existente para que admita más de un servidor DLL, hay dos requisitos:

-   Los servidores DLL deben tener el mismo valor de AppID.
-   El contexto de seguridad de los servidores DLL debe ser el mismo.

Si se van a iniciar dos servidores DLL con identidades de seguridad diferentes, deben estar en suplentes diferentes, independientemente de si sus AppID coinciden.

A continuación se muestra un ejemplo de administración del uso compartido suplente con appIDs:

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

Los dos CLSID para los componentes dll comp1.dll y comp2.dll se han configurado para compartir un AppID. La [clave AppID](appid-key.md) especifica que el servidor DLL se puede cargar en un suplente especificando el [valor DllSurrogate.](dllsurrogate.md) En este ejemplo, el valor **DllSurrogate** es una cadena vacía, lo que indica que se debe usar la implementación predeterminada del sistema del suplente dll.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Requisitos del servidor DLL](dll-server-requirements.md)
</dt> <dt>

[Registro del servidor DLL para la activación suplente](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




