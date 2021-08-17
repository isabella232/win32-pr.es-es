---
description: Al llamar a en los puntos de entrada de un ensamblado, se recomienda usar el mismo contexto de activación que estaba activo al buscar el ensamblado.
ms.assetid: 8b2de5f5-ea95-441f-9345-b64de53ea05f
title: Llamar a ensamblados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6f785c9d68aa0dbf4bec24927d9f2a1443aed1fb7fe65ec9244616fce8feec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142428"
---
# <a name="calling-into-assemblies"></a>Llamar a ensamblados

Al llamar a en los puntos de entrada de un ensamblado, se recomienda usar el mismo contexto de activación que estaba activo al buscar el ensamblado. Como mínimo, asegúrese de que el componente que carga el ensamblado no obtiene accidentalmente el contexto de activación que usa la aplicación. La pérdida del contexto de activación entre los límites de DLL puede provocar dependencias inesperadas. Esto no es un problema si la aplicación compila ISOLATION AWARE ENABLED porque, en ese caso, no hay ningún contexto de activación \_ \_ activo de forma predeterminada. Si no compila con ISOLATION AWARE ENABLED definido, debe activar el contexto de activación NULL o el mismo contexto de activación que se usó para \_ \_ cargar el ensamblado. 

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

 

 



