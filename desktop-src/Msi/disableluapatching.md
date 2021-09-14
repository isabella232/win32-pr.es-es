---
description: Si esta directiva de sistema por equipo está establecida en &\# 0034;1&0034;, el instalador impide que los usuarios que no son administradores usen la aplicación de revisiones de control de cuentas de usuario (UAC) para cualquier aplicación instalada en \# el equipo.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158550"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Si esta directiva de sistema por equipo se establece en "1", el instalador impide que los usuarios que no son administradores usen la aplicación de revisiones de control de cuentas de usuario [(UAC)](user-account-control--uac--patching.md) para cualquier aplicación instalada en el equipo. Cuando la directiva del sistema por máquina no se establece en 0, los usuarios que no son administradores pueden aplicar revisiones de usuario con privilegios mínimos a las aplicaciones habilitadas para la aplicación de revisiones de cuentas de usuario con privilegios mínimos.

Use la [**propiedad MSIDISABLELUAPATCHING**](msidisableluapatching.md) para evitar la aplicación de revisiones con privilegios mínimos.

La directiva DisableLUAPatching está disponible a partir de Windows Installer versión 3.0.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



