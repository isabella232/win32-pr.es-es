---
description: De forma predeterminada, el instalador ejecuta acciones personalizadas con privilegios de usuario para limitar el acceso de las acciones personalizadas al sistema.
ms.assetid: 62a3d103-a786-4727-b757-3a8229c8a53f
title: Seguridad de la acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7d36e0e5c6cecc61730144fb7efdeed63ba0fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361551"
---
# <a name="custom-action-security"></a>Seguridad de la acción personalizada

De forma predeterminada, el instalador ejecuta acciones personalizadas con privilegios de usuario para limitar el acceso de las acciones personalizadas al sistema. El instalador puede ejecutar acciones personalizadas con privilegios elevados si se instala una aplicación administrada o si se ha especificado la Directiva del sistema para privilegios elevados.

Debe usar la propiedad [**MsiHiddenProperties**](msihiddenproperties.md) y **msidbCustomActionTypeHideTarget** para evitar el registro de información confidencial utilizada por la acción personalizada. Para obtener más información sobre **MsidbCustomActionTypeHideTarget** , consulte la [opción de destino oculto de acción personalizada](custom-action-hidden-target-option.md).

Desactive la propiedad CustomActionData después de establecerla para asegurarse de que los datos confidenciales ya no estén disponibles. El código de ejemplo siguiente es un fragmento de código usado por una acción personalizada de DLL inmediata que está configurando datos para su uso por una acción personalizada diferida llamada "MyDeferredCA":


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



Tenga en cuenta que solo [las acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md) pueden usar el atributo **msidbCustomActionTypeNoImpersonate** . Para obtener más información, consulte [acción personalizada In-Script opciones de ejecución](custom-action-in-script-execution-options.md).

Si no se establece el bit **msidbCustomActionTypeNoImpersonate** para una acción personalizada, el instalador ejecuta la acción personalizada con privilegios de nivel de usuario. Para obtener más información, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

Si se establece el bit **msidbCustomActionTypeNoImpersonate** y se instala una aplicación administrada con permisos de administrador, el instalador puede ejecutar la acción personalizada con privilegios elevados. Sin embargo, si un usuario intenta instalar la aplicación administrada sin permiso de administrador, el instalador ejecuta la aplicación con privilegios de nivel de usuario independientemente de si **msidbCustomActionTypeNoImpersonate** está establecido.

Tenga en cuenta que una acción personalizada se puede ejecutar con privilegios del sistema aunque no se haya establecido el bit **msidbCustomActionTypeNoImpersonate** . Esto sucede si un administrador instala la aplicación para todos los usuarios de un servidor que ejecuta el servicio de rol de Terminal Server mediante Windows 2000 y la acción no está marcada con **msidbCustomActionTypeTSAware**. Una acción personalizada también puede ejecutarse con privilegios del sistema si la instalación se invoca cuando no hay ningún contexto de usuario. Por ejemplo, si no hay ningún usuario que haya iniciado sesión actualmente durante una instalación invocada por la implementación de la aplicación 2000 de Windows.

Al crear sus propias acciones personalizadas, debe crear siempre la acción personalizada mediante métodos seguros. Para obtener más información, consulte [directrices para proteger las acciones personalizadas](guidelines-for-securing-custom-actions.md).

 

 



