---
description: En esta guía se proporciona la información necesaria para permitir que la aplicación microsoft Windows use la próxima generación del protocolo de Internet, versión 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guía de IPv6 para Windows sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c52d86dfcdfa06df80dc71a3f3313de19f9201c7421a3f27f094589a6656dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741119"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a>Guía de IPv6 para Windows sockets

En esta guía se proporciona la información necesaria para permitir que la aplicación microsoft Windows use la próxima generación del protocolo de Internet, versión 6 (IPv6). Agregar la funcionalidad IPv6 a la aplicación no es necesariamente un proceso de porte. Para portabilidad de una aplicación, sugiere modificar el código para que funcione en una plataforma diferente, lo que implica dejar atrás la plataforma anterior. Esta guía está estructurada específicamente para ayudar a agregar la funcionalidad IPv6 a una aplicación y conservar la funcionalidad IPv4.

En esta guía se de abordan los problemas asociados con la adición de la funcionalidad IPv6 y, a continuación, se dirige a las áreas de desarrollo más afectadas por la transición. Cada área recibe una explicación exhaustiva de los problemas que se deben tener en cuenta, las estrategias sugeridas para evitarlos y sugerencias sobre cómo hacer el mejor uso de los nuevos elementos de programación de [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (funciones y estructuras). Para obtener más información sobre IPv6, vea [Compatibilidad con IPv6.](ipv6-support-2.md)

En esta guía también se proporcionan ejemplos de código para ofrecer experiencia práctica y representaciones visuales de los problemas que pueden surgir al modificar las aplicaciones. Los ejemplos proceden de ejemplos completos y prácticos de una sencilla aplicación Windows Sockets que se ha modificado para admitir IPv4 e IPv6. El código fuente de estos ejemplos de trabajo se incluye en su totalidad en dos apéndices al final de este documento: Apéndice A: Código fuente solo [IPv4](appendix-a-ipv4-only-source-code-2.md) incluye el código fuente de una aplicación antes de que se modifique para admitir IPv6; [Apéndice B: Código fuente](appendix-b-ip-version-agnostic-source-code-2.md) independiente de la versión IP proporciona el código fuente después de que la aplicación se haya habilitado para IPv6.

Microsoft proporciona una utilidad denominada Checkv4.exe que le ayuda a encontrar código potencialmente sensible a la porción en el código de la aplicación y también hace recomendaciones para correcciones. La Checkv4.exe se muestra en este documento, mediante la aplicación de ejemplo incluida en los apéndices, junto con capturas de pantalla que muestran la salida que genera la utilidad Checkv4.exe. Para obtener más información, [vea Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).

Las áreas de programación a las que se dirige esta guía son:

-   [Cambio de estructuras de datos para aplicaciones Winsock de IPv6](changing-data-structures-2.md)
-   [Llamadas de función para aplicaciones IPv6 Winsock](function-calls-2.md)
-   [Uso de direcciones IPv4 codificadas de forma rígida](use-of-hardcoded-ipv4-addresses-2.md)
-   [Interfaz de usuario problemas de aplicaciones IPv6 Winsock](user-interface-issues-2.md)
-   [Protocolos subyacentes para aplicaciones IPv6 Winsock](underlying-protocols-2.md)
-   [Sockets de pila doble para aplicaciones Winsock IPv6](dual-stack-sockets.md)

Dado que no hay ninguna secuencia uniforme de eventos, las secciones que abordan problemas de habilitación de IPv6 no se organizan de forma secuencialmente significativa, por lo que puede hacer referencia a cualquier sección en cualquier momento. Se recomienda encarecidamente revisar cada sección al agregar la funcionalidad IPv6 a la aplicación. También es aconsejable leer sobre la utilidad Checkv4.exe, ya que incluye sugerencias sobre el orden en el que abordar los problemas de habilitación de IPv6.

Para ver la utilidad Checkv4.exe y revisar el orden en el que debe abordar el proceso de porte en las aplicaciones, consulte Uso de la [utilidad Checkv4.exe .](using-the-checkv4-exe-utility-2.md) En esta sección se incluye información sobre una marca en tiempo de compilación que comprueba estrictamente los elementos de programación incompatibles con IPv6.

Para ir directamente a la aplicación de ejemplo, vea Apéndice A: Código fuente solo [IPv4](appendix-a-ipv4-only-source-code-2.md) y Apéndice [B:](appendix-b-ip-version-agnostic-source-code-2.md)Código fuente independiente de la versión IP .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Protocolo de Internet versión 6 (IPv6)](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[Compatibilidad con IPv6](ipv6-support-2.md)
</dt> <dt>

[IPv6 Technology Preview para Windows 2000](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[Uso de la utilidad Checkv4.exe datos](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[Apéndice A: Código fuente solo IPv4](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[Apéndice B: Código fuente independiente de la versión ip](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



