---
description: Instale un paquete de Windows Installer con privilegios elevados (sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c07e705e3e46a28049b6fb85eda96930d645a867
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104545195"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated

Puede usar la Directiva AlwaysInstallElevated para instalar un paquete de Windows Installer con privilegios elevados (sistema).

* * ADVERTENCIA: * *

Esta opción es equivalente a conceder derechos administrativos completos, lo que puede suponer un riesgo de seguridad masivo. Microsoft no recomienda encarecidamente el uso de esta opción.

Para instalar un paquete con privilegios elevados (sistema), establezca el valor de AlwaysInstallElevated en "1" en las dos claves del registro siguientes:

**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Si el valor AlwaysInstallElevated no se establece en "1" en las dos claves del registro anteriores, el instalador usa privilegios elevados para instalar las aplicaciones administradas y usa el nivel de privilegios del usuario actual para las aplicaciones no administradas.

Dado que esta directiva permite a los usuarios instalar aplicaciones que requieren acceso a directorios y claves del registro para los que es posible que el usuario no tenga permiso para ver o cambiar, debe considerar si proporciona a los usuarios un nivel de seguridad adecuado. La configuración de esta directiva indica a Windows Installer que use permisos del sistema cuando instale la aplicación en el sistema. Si no se establece esta Directiva, las aplicaciones que el administrador no distribuya se instalarán con los privilegios del usuario y solo las aplicaciones administradas obtendrán privilegios elevados.

Tenga en cuenta que una vez habilitada la Directiva por equipo para AlwaysInstallElevated, cualquier usuario puede establecer su configuración por usuario.

## <a name="remarks"></a>Observaciones

Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, consulte [Administración de orígenes de instalación](managing-installation-sources.md).

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

 

 



