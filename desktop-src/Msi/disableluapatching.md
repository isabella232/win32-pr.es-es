---
description: Si esta directiva de sistema por equipo se establece en \# &0034;1&0034;, el instalador impide que los usuarios que no son administradores usen la aplicación de revisión de control de cuentas de usuario (UAC) para cualquier aplicación instalada en \# el equipo.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821eb480ac09a2fc0416d7b3a54c0df5699a7096b45e56a843afe691886296f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637782"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Si esta directiva de sistema por equipo se establece en "1", el instalador impide que los usuarios que no son administradores usen la aplicación de revisión de control de cuentas de usuario [(UAC)](user-account-control--uac--patching.md) para cualquier aplicación instalada en el equipo. Cuando la directiva del sistema por máquina no se establece en 0, los usuarios que no son administradores pueden aplicar revisiones de usuario con privilegios mínimos a las aplicaciones habilitadas para la aplicación de revisiones de cuentas de usuario con privilegios mínimos.

Use la [**propiedad MSIDISABLELUAPATCHING**](msidisableluapatching.md) para evitar la aplicación de revisiones con privilegios mínimos.

La directiva DisableLUAPatching está disponible a partir de Windows installer versión 3.0.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



