---
description: En esta guía se proporciona la información necesaria para permitir que la aplicación Microsoft Windows use la próxima generación de protocolo de Internet, versión 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guía de IPv6 para aplicaciones de Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154272"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>Guía de IPv6 para aplicaciones de Windows Sockets

En esta guía se proporciona la información necesaria para permitir que la aplicación Microsoft Windows use la próxima generación de protocolo de Internet, versión 6 (IPv6). Agregar funcionalidad IPv6 a la aplicación no es necesariamente un proceso de portabilidad. Para trasladar una aplicación, se recomienda modificar el código para que funcione en una plataforma diferente, lo que implica la salida de la plataforma anterior. Esta guía está específicamente estructurada para ayudar a agregar funcionalidad IPv6 a una aplicación a la vez que se conserva la funcionalidad de IPv4.

En esta guía se describen los problemas asociados con la adición de la funcionalidad IPv6 y, a continuación, se destinan a las áreas de desarrollo más afectadas por la transición. Cada área recibe una explicación detallada de los problemas que se deben tener en cuidado, las estrategias sugeridas para evitarlos y sugerencias sobre cómo hacer el mejor uso de los nuevos elementos de programación de [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (funciones y estructuras). Para obtener información adicional sobre IPv6, consulte [compatibilidad con IPv6](ipv6-support-2.md).

En esta guía también se proporcionan ejemplos de código para ofrecerle experiencia práctica y representaciones visuales de los problemas que podría encontrar al modificar las aplicaciones. Los ejemplos provienen de ejemplos completos y funcionales de una sencilla aplicación de Windows Sockets que se ha modificado para admitir tanto IPv4 como IPv6. El código fuente de estos ejemplos de trabajo se incluye en su totalidad en dos apéndices al final de este documento: [apéndice a: el código fuente solo IPv4](appendix-a-ipv4-only-source-code-2.md) incluye el código fuente de una aplicación antes de que se modifique para admitir IPv6; [Apéndice B: código fuente independiente de la versión de IP](appendix-b-ip-version-agnostic-source-code-2.md) proporciona el código fuente una vez que la aplicación se ha habilitado para IPv6.

Microsoft proporciona una utilidad llamada Checkv4.exe que le ayuda a encontrar código potencialmente sensible a la migración en el código de la aplicación y también hace recomendaciones para las correcciones. La utilidad de Checkv4.exe se muestra en este documento, mediante la aplicación de ejemplo incluida en los apéndices, junto con las capturas de pantalla que muestran la salida que produce la utilidad de Checkv4.exe. Para obtener más información, vea [usar la utilidad Checkv4.exe](using-the-checkv4-exe-utility-2.md).

Las áreas de programación que se tratan en esta guía son:

-   [Cambiar las estructuras de datos para IPv6 Winsock Appications](changing-data-structures-2.md)
-   [Llamadas de función para aplicaciones Winsock de IPv6](function-calls-2.md)
-   [Uso de direcciones IPv4 codificadas](use-of-hardcoded-ipv4-addresses-2.md)
-   [Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6](user-interface-issues-2.md)
-   [Protocolos subyacentes para aplicaciones Winsock de IPv6](underlying-protocols-2.md)
-   [Sockets de doble pila para aplicaciones Winsock de IPv6](dual-stack-sockets.md)

Dado que no hay ninguna secuencia uniforme de eventos, las secciones que abordan los problemas de habilitación de IPv6 no se organizan de forma secuencial, por lo que puede hacer referencia a cualquier sección en cualquier momento. Se recomienda encarecidamente que revise cada sección mientras agrega funcionalidad IPv6 a la aplicación. También es aconsejable leer sobre la utilidad de Checkv4.exe, ya que incluye sugerencias sobre el orden en que se deben tratar los problemas de habilitación de IPv6.

Para consultar la utilidad de Checkv4.exe y revisar el orden en el que debe abordar el proceso de portabilidad de las aplicaciones, consulte [usar la utilidad Checkv4.exe](using-the-checkv4-exe-utility-2.md). En esta sección se incluye información sobre una marca de tiempo de compilación que comprueba estrictamente si hay elementos de programación incompatibles con IPv6.

Para ir directamente a la aplicación de ejemplo, vea el [Apéndice A: código fuente solo IPv4](appendix-a-ipv4-only-source-code-2.md) y [Apéndice B: código fuente independiente de la versión de IP](appendix-b-ip-version-agnostic-source-code-2.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protocolo de Internet versión 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Compatibilidad con IPv6](ipv6-support-2.md)
</dt> <dt>

[IPv6 Technology Preview para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Usar la utilidad Checkv4.exe](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[Apéndice A: código fuente solo IPv4](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[Apéndice B: código fuente independiente de la versión de IP](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



