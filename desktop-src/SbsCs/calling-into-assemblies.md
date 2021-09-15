---
description: Al llamar a los puntos de entrada de un ensamblado, se recomienda usar el mismo contexto de activación que estaba activo al buscar el ensamblado.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Llamar a ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03e4742b19ea47e03fac5f7d0318248ea167182e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271692"
---
# <a name="calling-into-assemblies"></a>Llamar a ensamblados

Al llamar a los puntos de entrada de un ensamblado, se recomienda usar el mismo contexto de activación que estaba activo al buscar el ensamblado. Como mínimo, asegúrese de que el componente que carga el ensamblado no obtiene accidentalmente el contexto de activación que usa la aplicación. La pérdida de contexto de activación a través de los límites de DLL puede provocar dependencias inesperadas. Esto no es un problema si la aplicación compila ISOLATION AWARE ENABLED porque, en ese caso, no hay ningún contexto de activación \_ \_ activo de forma predeterminada. Si no compila con ISOLATION AWARE ENABLED definido, debe activar el contexto de activación NULL o el mismo contexto de activación que se usó para \_ \_ cargar el ensamblado. 

En el ejemplo siguiente se garantiza que el archivo DLL hospedado se ejecuta en un contexto que reconoce:

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

 

 



