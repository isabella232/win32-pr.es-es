---
description: Instale un paquete Windows Installer con privilegios elevados (sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159145"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated

Puede usar la directiva AlwaysInstallElevated para instalar un paquete Windows Installer con privilegios elevados (sistema).

**Advertencia: **

Esta opción equivale a conceder derechos administrativos completos, lo que puede suponer un riesgo de seguridad masivo. Microsoft desaconseja encarecidamente el uso de esta configuración.

Para instalar un paquete con privilegios elevados (sistema), establezca el valor AlwaysInstallElevated en "1" en las dos claves del Registro siguientes:

**HKEY \_ Directivas \_ de** \\ **software de USUARIO** \\ **ACTUAL** \\ **Instalador de** \\ **Windows** \\ **Microsoft**

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

Si el valor AlwaysInstallElevated no está establecido en "1" en las dos claves del Registro anteriores, el instalador usa privilegios elevados para instalar aplicaciones administradas y usa el nivel de privilegios del usuario actual para las aplicaciones no administradas.

Dado que esta directiva permite a los usuarios instalar aplicaciones que requieren acceso a directorios y claves del Registro para las que es posible que el usuario no tenga permiso para ver o cambiar, debe considerar si proporciona a los usuarios un nivel de seguridad adecuado. Al establecer esta directiva, Windows instalador use permisos del sistema al instalar la aplicación en el sistema. Si no se establece esta directiva, las aplicaciones no distribuidas por el administrador se instalan con los privilegios del usuario y solo las aplicaciones administradas obtienen privilegios elevados.

Tenga en cuenta que una vez habilitada la directiva por equipo para AlwaysInstallElevated, cualquier usuario puede establecer su configuración por usuario.

## <a name="remarks"></a>Observaciones

Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, vea [Managing Installation Sources](managing-installation-sources.md).

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 



