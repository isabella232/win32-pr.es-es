---
description: Esta Directiva del sistema por equipo se puede usar para especificar que el Windows Installer pasar todas las propiedades públicas al servidor durante una instalación administrada con privilegios elevados.
ms.assetid: 437ceef2-730f-47ae-9b1f-dfc7c6d2d132
title: EnableUserControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 257496be3815a20bbc855b456bb74e4cc8f61684
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155532"
---
# <a name="enableusercontrol"></a>EnableUserControl

En el caso de una instalación administrada, es posible que el autor del paquete tenga que limitar las propiedades públicas que se pasan al lado servidor y que un usuario que no es administrador del sistema puede cambiar. Normalmente, algunas restricciones son necesarias para mantener un entorno seguro cuando la instalación requiere que el instalador use privilegios elevados.

Si esta [Directiva del sistema](system-policy.md) por equipo se establece en "1", el instalador puede pasar todas [las propiedades públicas](public-properties.md) al servidor durante una instalación administrada con privilegios elevados. La configuración de esta directiva tiene el mismo efecto que establecer la propiedad **EnableUserControl** . La configuración de esta directiva permite que se pasen todas las propiedades públicas al servicio y que los usuarios no administrativos puedan modificarlas. De forma predeterminada, esta Directiva no está habilitada; solo las propiedades públicas restringidas se pasan al lado del servidor y pueden ser modificadas por un usuario no administrativo. Se omiten todas las demás propiedades públicas.

Si el sistema operativo es Windows 2000, el usuario no es un administrador del sistema y la aplicación o el producto se instala con privilegios elevados, un usuario que no es administrador del sistema solo puede invalidar una lista aprobada de propiedades públicas restringidas. Para obtener más información, consulte [propiedades públicas restringidas](restricted-public-properties.md).

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

 

 



