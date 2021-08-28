---
description: Instale un paquete Windows Installer con privilegios elevados (sistema).
ms.assetid: 0bbec06a-0a2b-430a-a361-317a319da615
title: AlwaysInstallElevated
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc015dad8096db16d8b70238a5fd7e07544b83f9a9e3d1a5045be9d12bbb30cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650245"
---
# <a name="alwaysinstallelevated"></a>AlwaysInstallElevated

Puede usar la directiva AlwaysInstallElevated para instalar un paquete Windows Installer con privilegios elevados (sistema).

**Advertencia: **

Esta opción equivale a conceder derechos administrativos completos, lo que puede suponer un riesgo de seguridad masivo. Microsoft desaconseja encarecidamente el uso de esta configuración.

Para instalar un paquete con privilegios elevados (sistema), establezca el valor AlwaysInstallElevated en "1" en las dos claves del Registro siguientes:

**HKEY \_ Directivas \_ de** \\ **software de USUARIO** \\ **ACTUAL** \\ **Instalador de** \\ **Windows** \\ **Microsoft**

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

Si el valor AlwaysInstallElevated no se establece en "1" en las dos claves del Registro anteriores, el instalador usa privilegios elevados para instalar aplicaciones administradas y usa el nivel de privilegios del usuario actual para las aplicaciones no administradas.

Dado que esta directiva permite a los usuarios instalar aplicaciones que requieren acceso a directorios y claves del Registro para las que es posible que el usuario no tenga permiso para ver o cambiar, debe considerar si proporciona a los usuarios un nivel de seguridad adecuado. Al establecer esta directiva, Windows instalador debe usar permisos del sistema cuando instala la aplicación en el sistema. Si no se establece esta directiva, las aplicaciones no distribuidas por el administrador se instalan con los privilegios del usuario y solo las aplicaciones administradas obtienen privilegios elevados.

Tenga en cuenta que una vez habilitada la directiva por equipo para AlwaysInstallElevated, cualquier usuario puede establecer su configuración por usuario.

## <a name="remarks"></a>Comentarios

Para obtener información sobre la interacción de esta directiva con los orígenes de instalación, vea [Administrar orígenes de instalación](managing-installation-sources.md).

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 



