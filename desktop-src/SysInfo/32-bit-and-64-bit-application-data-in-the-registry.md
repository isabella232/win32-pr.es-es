---
description: En el Windows de 64 bits, las partes de las entradas del Registro se almacenan por separado para aplicaciones de 32 bits y aplicaciones de 64 bits y se asignan a vistas de registro lógicas independientes mediante el redirector del Registro y la reflexión del Registro, ya que la versión de 64 bits de una aplicación puede usar diferentes claves y valores del Registro que la versión de 32 bits. También hay claves del Registro compartidas que no se redirigen ni reflejan.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Datos de aplicación de 32 y 64 bits en el Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d5177eb48a5497e321b47bb0da96874a0e6522360f2dc519dc72df3dcdf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764989"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>Datos de aplicación de 32 y 64 bits en el Registro

En el Windows de 64 bits, las partes de las entradas del Registro se almacenan por separado para aplicaciones de 32 bits y aplicaciones de 64 bits y se asignan a vistas de registro lógicas independientes mediante el redirector del Registro y la reflexión del Registro [,](/windows/desktop/WinProg64/registry-reflection)ya que la versión de 64 bits de una aplicación puede usar claves y valores del Registro diferentes a los de la versión de 32 bits. [](/windows/desktop/WinProg64/registry-redirector) También hay claves [del Registro compartidas](/windows/desktop/WinProg64/shared-registry-keys) que no se redirigen ni reflejan.

El elemento primario de cada nodo del Registro de 64 bits es Image-Specific nodo o ISN. El redirector del registro dirige de forma transparente el acceso del registro de una aplicación al subnodo ISN adecuado. El componente WOW64 crea automáticamente los subnodos de redireccionamiento del árbol del Registro con el nombre **Wow6432Node**. Como resultado, es esencial no nombrar ninguna clave del Registro que cree **Wow6432Node**.

Las marcas KEY \_ WOW64 64KEY y KEY WOW64 32KEY permiten el acceso explícito a la vista del Registro de 64 bits y a la vista de \_ \_ \_ 32 bits, respectivamente. Para obtener más información, vea [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).

Para deshabilitar y habilitar la reflexión del Registro para una clave determinada, use las funciones [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) y [**RegEnableReflectionKey.**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) Las aplicaciones deben deshabilitar la reflexión solo para las claves del Registro que crean y no intentar deshabilitar la reflexión para las claves predefinidas, como **HKEY \_ LOCAL \_ MACHINE** o **HKEY \_ CURRENT \_ USER**. Para determinar qué claves están en la lista de reflexión, use la [**función RegQueryReflectionKey.**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[redirector del registro](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[reflexión del registro](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
