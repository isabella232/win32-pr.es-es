---
description: La longevidad de IPv4 dio lugar a codificar de forma rígida muchas direcciones IPv4 conocidas, como las direcciones de bucle invertido (127. x.x. x), constantes enteras como la indirección \_ de bucle invertido, entre otras.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Uso de direcciones IPv4 codificadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360290"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a>Uso de direcciones IPv4 codificadas

La longevidad de IPv4 dio lugar a codificar de forma rígida muchas direcciones IPv4 conocidas, como las direcciones de bucle invertido (127. x.x. x), constantes enteras como la indirección \_ de bucle invertido, entre otras. La práctica de codificar de forma rígida estas direcciones presenta problemas obvios al modificar una aplicación existente para admitir IPv6 o crear nuevos programas independientes de la versión de IP.

Procedimiento recomendado

-   El mejor enfoque es evitar codificar cualquier dirección.

Código que se debe evitar

-   Evite el uso de direcciones codificadas en código.

**Para modificar la base de código existente de IPv4 a IPv4 e IPv6: interoperabilidad**

1.  Adquiera la utilidad *Checkv4.exe* . La utilidad de *Checkv4.exe* se instala como parte del kit de desarrollo de software (SDK) de Microsoft Windows publicado para Windows Vista y versiones posteriores. El Windows SDK está disponible a través de una suscripción a MSDN y también se puede descargar desde el sitio web de Microsoft ( https://msdn.microsoft.com) .
2.  Ejecute la utilidad *Checkv4.exe* en el código. Obtenga información acerca de cómo ejecutar la utilidad *Checkv4.exe* en los archivos de la sección sobre [el uso de la utilidad Checkv4.exe](using-the-checkv4-exe-utility-2.md).
3.  La utilidad de *Checkv4.exe* le alerta de la presencia de definiciones comunes para las direcciones IPv4, como la indirección de \_ bucle invertido. Modifique cualquier código que use cadenas literales con código independiente de la versión del protocolo.
4.  Busque en el código base otras posibles cadenas literales, según corresponda.

La utilidad *Checkv4.exe* puede ayudarle a encontrar cadenas literales comunes, pero puede haber otros que sean específicos de la aplicación. Debe realizar búsquedas y pruebas exhaustivas para asegurarse de que el código base ha erradicado los posibles problemas asociados a las cadenas literales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de IPv6 para aplicaciones de Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Cambiar las estructuras de datos para IPv6 Winsock Appications](changing-data-structures-2.md)
</dt> <dt>

[Sockets de doble pila para aplicaciones Winsock de IPv6](dual-stack-sockets.md)
</dt> <dt>

[Llamadas de función para aplicaciones Winsock de IPv6](function-calls-2.md)
</dt> <dt>

[Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocolos subyacentes para aplicaciones Winsock de IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 



