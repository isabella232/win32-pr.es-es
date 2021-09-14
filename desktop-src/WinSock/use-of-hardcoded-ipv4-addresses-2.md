---
description: La longevidad de IPv4 dio lugar a codificar de forma rígida muchas direcciones IPv4 conocidas, como las direcciones de bucleback (127.x.x.x), constantes de enteros como INADDR \_ LOOPBACK, entre otras.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Uso de direcciones IPv4 codificadas de forma rígida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361309"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>Uso de direcciones IPv4 codificadas de forma rígida

La longevidad de IPv4 dio lugar a codificar de forma rígida muchas direcciones IPv4 conocidas, como las direcciones de bucleback (127.x.x.x), constantes de enteros como INADDR \_ LOOPBACK, entre otras. La práctica de codificar de forma rígida estas direcciones presenta problemas obvios al modificar y la aplicación existente para admitir IPv6 o crear nuevos programas independientes de la versión de IP.

Procedimiento recomendado

-   El mejor enfoque es evitar lacoding de cualquier dirección.

Código que se debe evitar

-   Evite el uso de direcciones codificadas de forma rígida en el código.

**Para modificar la base de código existente de IPv4 a interoperabilidad IPv4 e IPv6**

1.  Adquiera la *utilidadCheckv4.exe.* La *utilidadCheckv4.exe* se instala como parte del Kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores. El SDK Windows está disponible a través de una suscripción a MSDN y también se puede descargar desde el sitio web de Microsoft ( https://msdn.microsoft.com) .
2.  Ejecute la *utilidadCheckv4.exe* en el código. Obtenga información sobre cómo ejecutar la *utilidadCheckv4.exe* en los archivos en la sección Uso de la utilidad [Checkv4.exe .](using-the-checkv4-exe-utility-2.md)
3.  La *Checkv4.exe* le avisa de la presencia de defineciones comunes para direcciones IPv4, como INADDR \_ LOOPBACK. Modifique cualquier código que use cadenas literales con código independiente de la versión del protocolo.
4.  Busque en la base de código otras cadenas literales potenciales, según corresponda.

La *Checkv4.exe* puede ayudarle a encontrar cadenas literales comunes, pero puede haber otras que sean específicas de la aplicación. Debe realizar búsquedas y pruebas exhaustivas para asegurarse de que la base de código tiene problemas potenciales asociados con cadenas literales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de IPv6 para aplicaciones Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Cambio de estructuras de datos para aplicaciones Winsock de IPv6](changing-data-structures-2.md)
</dt> <dt>

[Sockets de pila doble para aplicaciones Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Llamadas de función para aplicaciones IPv6 Winsock](function-calls-2.md)
</dt> <dt>

[Interfaz de usuario problemas de aplicaciones IPv6 Winsock](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subyacentes para aplicaciones IPv6 Winsock](underlying-protocols-2.md)
</dt> </dl>

 

 



