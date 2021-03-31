---
description: Si esta Directiva del sistema está establecida en 1, el instalador no almacena los archivos de reversión durante la instalación y deshabilita la reversión de la instalación.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001295"
---
# <a name="disablerollback"></a>DisableRollback

Si esta [Directiva del sistema](system-policy.md) está establecida en 1, el instalador no almacena los archivos de reversión durante la instalación y deshabilita la reversión de la instalación. De forma predeterminada, la reversión está habilitada. Es aconsejable que los administradores no utilicen esta directiva a menos que sea absolutamente imprescindible. Para obtener más información, consulte [reversión de instalación](rollback-installation.md).

## <a name="registry-key"></a>Clave del Registro

Para deshabilitar la reversión de las instalaciones por usuario, establezca **DisableRollback** en 1 en la siguiente clave del registro:

**HKEY \_ \_** Directivas de software de usuario actual \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

Para deshabilitar la reversión en instalaciones por equipo, establezca **DisableRollback** en 1 en la siguiente clave del registro.

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

 

 



