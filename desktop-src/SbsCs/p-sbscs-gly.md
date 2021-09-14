---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: P (aplicaciones aisladas y ensamblados en paralelo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c70c0775af4a6245e74de474413c3741625456
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071346"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a>P (aplicaciones aisladas y ensamblados en paralelo)

[A](a-sbscs-gly.md) B C [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M N](m-sbscs-gly.md) O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T U V W X Y Z

<dl> <dt>

<span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**configuración por aplicación**
</dt> <dd>

Configuración que puede invalidar la configuración de la aplicación global de un ensamblado específico. Un archivo de manifiesto de configuración de aplicación instalado en la misma carpeta que el archivo ejecutable especifica una configuración por aplicación. El archivo de manifiesto describe la versión o el intervalo de versiones de los ensamblados en paralelo que va a usar la aplicación. La configuración por aplicación se puede usar cuando una nueva versión de un ensamblado no es compatible con una aplicación. En este caso, la configuración predeterminada o global de la aplicación se puede invalidar para un ensamblado en paralelo específico.

</dd> <dt>

<span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**ensamblado en paralelo privado**
</dt> <dd>

Un ensamblado privado en paralelo solo es visible para una aplicación especificada. Se instala localmente en una aplicación aislada y el código del ensamblado se convierte en privado para el contexto de la aplicación. Las dependencias de un ensamblado privado en paralelo se describen en el archivo de manifiesto de aplicación. Los ensamblados privados en paralelo se pueden usar para compensar los efectos negativos del uso compartido de ensamblados, como conflictos de DLL, y para facilitar la implementación de aplicaciones.

</dd> <dt>

<span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**token de clave pública**
</dt> <dd>

Cadena hexadecimal de 16 caracteres que representa los últimos 8 bytes del hash SHA-1 de la clave pública con la que se firma el ensamblado. La clave pública usada para firmar el catálogo debe ser de 2048 bits o superior. Se requiere para todos los ensamblados en paralelo compartidos.

</dd> </dl>

 

 



