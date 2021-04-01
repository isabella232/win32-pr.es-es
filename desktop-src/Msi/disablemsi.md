---
description: Si el valor de esta Directiva del sistema por equipo se establece en &\# 0034; 2&\# 0034; el instalador está siempre deshabilitado para todas las aplicaciones. Si este valor de Directiva se establece en &\# 0034; 1&\# 0034;, el instalador está deshabilitado para las aplicaciones no administradas, pero aún está habilitado para las aplicaciones administradas.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082785"
---
# <a name="disablemsi"></a>DisableMSI

Si el valor de esta [Directiva del sistema](system-policy.md) por equipo se establece en "2", el instalador está siempre deshabilitado para todas las aplicaciones. Si este valor de Directiva se establece en "1", el instalador está deshabilitado para las aplicaciones no administradas, pero todavía está habilitado para las aplicaciones administradas.

En la tabla siguiente se enumeran las posibles configuraciones.



| DisableMSI | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Valor predeterminado*  | En Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 y Windows Server 2008 R2, si el valor de la Directiva es null, está ausente o cualquier número distinto de 1 o 2, el Windows Installer está habilitado para las aplicaciones administradas. Las instalaciones de aplicaciones no administradas están bloqueadas.<br/> En Windows XP, Windows Vista y Windows 7, la Windows Installer está habilitada para todas las aplicaciones. Se permiten todas las operaciones de instalación.<br/> |
| 0          | Windows Installer está habilitada para todas las aplicaciones. Se permiten todas las operaciones de instalación.                                                                                                                                                                                                                                                                                                                                                      |
| 1          | El Windows Installer está deshabilitado para las aplicaciones no administradas, pero todavía está habilitado para las aplicaciones administradas. Las instalaciones por usuario no elevadas están bloqueadas. Se permiten las instalaciones con privilegios elevados por usuario y por equipo.                                                                                                                                                                                                                        |
| 2          | Windows Installer está siempre deshabilitada para todas las aplicaciones. No se permite ninguna instalación, como reparaciones, reinstalaciones o instalaciones a petición.                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




