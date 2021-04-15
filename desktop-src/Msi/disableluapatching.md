---
description: Si esta Directiva del sistema por equipo está establecida en &\# 0034; 1&\# 0034;, el instalador impide que los usuarios que no sean administradores usen la aplicación de revisiones del control de cuentas de usuario (UAC) para cualquier aplicación instalada en el equipo.
ms.assetid: b122d6f4-2be6-4b9b-b8e0-ca08fe9c4f94
title: DisableLUAPatching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b76357211523d0a69a56ab2a047623a63f211df9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669999"
---
# <a name="disableluapatching"></a>DisableLUAPatching

Si esta Directiva del sistema por equipo se establece en "1", el instalador impide que los usuarios que no sean administradores utilicen la aplicación de [revisiones del control de cuentas de usuario (UAC)](user-account-control--uac--patching.md) para cualquier aplicación instalada en el equipo. Cuando la Directiva del sistema por equipo no se establece o se establece en 0, los usuarios que no son administradores pueden aplicar revisiones de usuario con privilegios mínimos a las aplicaciones habilitadas para la aplicación de revisiones de cuenta de usuario con privilegios mínimos.

Use la propiedad [**MSIDISABLELUAPATCHING**](msidisableluapatching.md) para evitar la aplicación de revisiones con privilegios mínimos de una aplicación.

La Directiva DisableLUAPatching está disponible a partir de Windows Installer versión 3,0.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



