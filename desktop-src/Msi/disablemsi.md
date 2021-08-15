---
description: Si el valor de esta directiva de sistema por máquina se establece en \# &0034;2&0034; el instalador siempre está deshabilitado para todas las \# aplicaciones. Si este valor de directiva se establece en \# &0034;1&0034;, el instalador está deshabilitado para las aplicaciones no administradas, pero todavía está habilitado para las aplicaciones \# administradas.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 846b8fb8c2c1127e59c82cce138a0956756d3447d6628cb61ef170a91e6290b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118378563"
---
# <a name="disablemsi"></a>DisableMSI

Si el valor de [](system-policy.md) esta directiva de sistema por equipo está establecido en "2", el instalador siempre está deshabilitado para todas las aplicaciones. Si este valor de directiva se establece en "1", el instalador está deshabilitado para las aplicaciones no administradas, pero todavía está habilitado para las aplicaciones administradas.

En la tabla siguiente se enumeran las configuraciones posibles.



| DisableMSI | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Valor predeterminado*  | En Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 y Windows Server 2008 R2, si el valor de directiva es Null, absent o cualquier número distinto de 1 o 2, el instalador de Windows está habilitado para las aplicaciones administradas. Las instalaciones de aplicaciones no administradas están bloqueadas.<br/> En Windows XP, Windows Vista y Windows 7, el instalador Windows está habilitado para todas las aplicaciones. Se permiten todas las operaciones de instalación.<br/> |
| 0          | Windows El instalador está habilitado para todas las aplicaciones. Se permiten todas las operaciones de instalación.                                                                                                                                                                                                                                                                                                                                                      |
| 1          | El Windows está deshabilitado para las aplicaciones no administradas, pero todavía está habilitado para las aplicaciones administradas. Las instalaciones por usuario no con privilegios elevados están bloqueadas. Se permiten las instalación por usuario con privilegios elevados y por equipo.                                                                                                                                                                                                                        |
| 2          | Windows El instalador siempre está deshabilitado para todas las aplicaciones. No se permite ninguna instalación, incluidas reparaciones, reinstalaciones o instalaciones a petición.                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




