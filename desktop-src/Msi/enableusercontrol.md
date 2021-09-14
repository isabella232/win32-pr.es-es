---
description: Esta directiva de sistema por equipo se puede usar para especificar que el instalador de Windows pase todas las propiedades públicas al lado servidor durante una instalación administrada mediante privilegios elevados.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158488"
---
# <a name="enableusercontrol"></a>EnableUserControl

En el caso de una instalación administrada, es posible que el autor del paquete tenga que limitar las propiedades públicas que se pasan al lado servidor y que puede cambiar un usuario que no sea administrador del sistema. Algunas restricciones son normalmente necesarias para mantener un entorno seguro cuando la instalación requiere que el instalador use privilegios elevados.

Si esta directiva [](system-policy.md) del sistema por equipo se establece en "1", el instalador puede pasar todas las propiedades públicas al lado servidor durante una instalación administrada con privilegios elevados. [](public-properties.md) Establecer esta directiva tiene el mismo efecto que establecer la **propiedad EnableUserControl.** Establecer esta directiva permite que todas las propiedades públicas se pasen al servicio y que los usuarios no administradores puedan cambiar. De forma predeterminada, esta directiva no está habilitada; solo las propiedades públicas restringidas se pasan al lado del servidor y un usuario no administrador puede cambiarla. Se omiten todas las demás propiedades públicas.

Si el sistema operativo es Windows 2000, el usuario no es un administrador del sistema y la aplicación o el producto se instala con privilegios elevados, un usuario que no sea un administrador del sistema solo puede invalidar una lista aprobada de propiedades públicas restringidas. Para obtener más información, [vea Propiedades públicas restringidas.](restricted-public-properties.md)

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

 

 



