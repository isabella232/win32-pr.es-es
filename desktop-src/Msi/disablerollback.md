---
description: Si esta directiva del sistema se establece en 1, el instalador no almacena los archivos de reversión durante la instalación y deshabilita la reversión de la instalación.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158537"
---
# <a name="disablerollback"></a>DisableRollback

Si esta [directiva del sistema](system-policy.md) se establece en 1, el instalador no almacena los archivos de reversión durante la instalación y deshabilita la reversión de la instalación. De forma predeterminada, la reversión está habilitada. Se recomienda a los administradores no usar esta directiva a menos que sea absolutamente esencial. Para obtener más información, vea [Rollback Installation](rollback-installation.md).

## <a name="registry-key"></a>Clave del Registro

Para deshabilitar la reversión de instalaciones por usuario, establezca **DisableRollback** en 1 en la siguiente clave del Registro:

**HKEY \_ Directivas \_ de** \\ **software de USUARIO** \\ **ACTUAL** \\ **Instalador de** \\ **Windows** \\ **Microsoft**

Para deshabilitar la reversión de instalaciones por equipo, establezca **DisableRollback** en 1 en la siguiente clave del Registro.

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 



