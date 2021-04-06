---
description: Cuando se llama a entryPoints de un ensamblado, se recomienda usar el mismo contexto de activación que estaba activo al buscar el ensamblado.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Llamar a ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002186"
---
# <a name="calling-into-assemblies"></a>Llamar a ensamblados

Cuando se llama a entryPoints de un ensamblado, se recomienda usar el mismo contexto de activación que estaba activo al buscar el ensamblado. Como mínimo, asegúrese de que el componente que carga el ensamblado no obtiene accidentalmente el contexto de activación que está usando la aplicación. La pérdida de contexto de activación a través de los límites de DLL puede provocar dependencias inesperadas. Esto no es un problema si la aplicación compila el reconocimiento de \_ aislamiento \_ habilitado porque, en ese caso, no hay ningún contexto de activación activo de forma predeterminada. Si no compila con el reconocimiento de \_ aislamiento \_ habilitado definido, debe activar el contexto de activación **null** o el mismo contexto de activación que se usó para cargar el ensamblado.

En el ejemplo siguiente se garantiza que la DLL hospedada se ejecuta en un contexto que reconoce:

``` syntax
ULONG_PTR ulpCookie;
ActivateActCtx(hTheActCtxForMyDll, &ulpCookie);
__try 
{
        MyDllIsolatedFunction();
    myDllIsolatedComInterface->Funct();
}
__finally 
{
    DeactivateActCtx(0, ulpCookie);
}
```

 

 



