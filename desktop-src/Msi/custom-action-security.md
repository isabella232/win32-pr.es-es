---
description: El instalador ejecuta acciones personalizadas con privilegios de usuario de forma predeterminada para limitar el acceso de acciones personalizadas al sistema.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Seguridad de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7d36e0e5c6cecc61730144fb7efdeed63ba0fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158709"
---
# <a name="custom-action-security"></a>Seguridad de acciones personalizadas

El instalador ejecuta acciones personalizadas con privilegios de usuario de forma predeterminada para limitar el acceso de acciones personalizadas al sistema. El instalador puede ejecutar acciones personalizadas con privilegios elevados si se instala una aplicación administrada o si se ha especificado la directiva del sistema para privilegios elevados.

Debe usar la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) y **msidbCustomActionTypeHideTarget para** evitar el registro de información confidencial usada por la acción personalizada. Para obtener más información sobre **msidbCustomActionTypeHideTarget,** vea [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).

Borre la propiedad CustomActionData después de establecerla para asegurarse de que la información confidencial ya no está disponible. El código de ejemplo siguiente es un fragmento de código usado por una acción personalizada de DLL inmediata que configura los datos para su uso por una acción personalizada diferida denominada "MyDeferredCA":


```C++
#include <windows.h>
#include <Msiquery.h>
#pragma comment(lib, "msi.lib")

UINT __stdcall MyImmediateCA(MSIHANDLE hInstall)
{
    // set up information for deferred custom action called MyDeferredCA
    const TCHAR szValue[] = TEXT("data");
    UINT uiStat = ERROR_INSTALL_FAILURE;
    if (ERROR_SUCCESS == MsiSetProperty(hInstall, TEXT("MyDeferredCA"), szValue))
    {
        uiStat = MsiDoAction(hInstall, TEXT("MyDeferredCA"));

        // clear CustomActionData property
        if (ERROR_SUCCESS != MsiSetProperty(hInstall, TEXT("MyDeferredCA"), TEXT("")))
            return ERROR_INSTALL_FAILURE;
    }

    return (uiStat == ERROR_SUCCESS) ? uiStat : ERROR_INSTALL_FAILURE;    
}
```



Tenga en cuenta que [solo las acciones personalizadas de ejecución diferida](deferred-execution-custom-actions.md) pueden usar el atributo **msidbCustomActionTypeNoImpersonate.** Para obtener más información, [vea Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

Si el bit **msidbCustomActionTypeNoImpersonate** no está establecido para una acción personalizada, el instalador ejecuta la acción personalizada con privilegios de nivel de usuario. Para obtener más información, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

Si se establece el bit **msidbCustomActionTypeNoImpersonate** y se instala una aplicación administrada con permiso de administrador, el instalador puede ejecutar la acción personalizada con privilegios elevados. Sin embargo, si un usuario intenta instalar la aplicación administrada sin permiso de administrador, el instalador ejecuta la aplicación con privilegios de nivel de usuario independientemente de si se establece **msidbCustomActionTypeNoImpersonate.**

Tenga en cuenta que una acción personalizada puede ejecutarse con privilegios del sistema incluso cuando el bit **msidbCustomActionTypeNoImpersonate** no está establecido. Esto ocurre si un administrador instala la aplicación para todos los usuarios en un servidor que ejecuta el servicio de rol de Terminal Server mediante Windows 2000 y la acción no está marcada con **msidbCustomActionTypeTSAware**. Una acción personalizada también puede ejecutarse con privilegios del sistema si se invoca la instalación cuando no hay contexto de usuario. Por ejemplo, si no hay ningún usuario que haya iniciado sesión actualmente durante una instalación invocada por Windows implementación de aplicaciones de 2000.

Al crear sus propias acciones personalizadas, siempre debe crear la acción personalizada mediante métodos seguros. Para obtener más información, vea [Directrices para proteger acciones personalizadas.](guidelines-for-securing-custom-actions.md)

 

 



