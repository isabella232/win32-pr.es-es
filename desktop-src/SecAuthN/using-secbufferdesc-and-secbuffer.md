---
description: A menudo, la comunicación implica grandes cantidades de datos o datos de longitud desconocida.
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: Usar SecBufferDesc y SecBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ca7d8155a610263838d2baf2a7d1c8fc96ec874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911854"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>Usar SecBufferDesc y SecBuffer

A menudo, la comunicación implica grandes cantidades de datos o datos de longitud desconocida. El envío y la recepción de datos se realizan de manera similar o idéntica en ambos casos. Para tratar con una longitud desconocida y potencialmente grandes cantidades de datos, la comunicación SSPI se realiza con dos estructuras, [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) y [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).

Una estructura [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) es un contenedor para una matriz de estructuras [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) . Una estructura **SecBufferDesc** tiene los siguientes miembros:

-   Número de versión
-   Número de elementos [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)
-   Dirección de la matriz de estructuras [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Una estructura [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) contiene los tres miembros siguientes:

-   Número de bytes en el búfer
-   Tipo de información contenida en el elemento de datos
-   Los propios bytes

Un mensaje SSPI completo se compone a menudo de una matriz de estructuras [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) .

Los siguientes tipos de datos de búfer se definen como se indica a continuación.



| Tipo de búfer                | Significado                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ vacío           | Undefined, reemplazado por la función de [*paquete de seguridad*](../secgloss/s-gly.md) |
| datos de SECBUFFER \_            | Datos de paquetes                                                                                                                            |
| \_token SECBUFFER           | Token de seguridad                                                                                                                         |
| PARÁMETROS de SECBUFFER \_ pkg \_     | Parámetros específicos del paquete                                                                                                            |
| \_falta SECBUFFER         | Falta el indicador de datos                                                                                                                 |
| SECBUFFER \_ extra           | Datos adicionales                                                                                                                             |
| \_flujo SECBUFFER          | Datos de flujo de seguridad                                                                                                                   |
| \_finalizador de flujo SECBUFFER \_ | Finalizador de flujo de seguridad                                                                                                                |
| SECBUFFER \_ encabezado de secuencia \_  | Encabezado de flujo de seguridad                                                                                                                 |



 

Los tipos de búfer anteriores se pueden combinar mediante **una operación OR bit a bit** con cualquiera de los siguientes tipos de búfer.



| Tipo de búfer         | Significado                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| SECBUFFER \_ ATTRMASK | Enmascara los atributos de seguridad separando las marcas de atributo del tipo de búfer. |
| SECBUFFER \_ ReadOnly | El búfer es de solo lectura                                                              |



 

Antes de cada llamada a una API SSPI que requiere un parámetro [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) , se declaran e inicializan uno o varios elementos de la matriz [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) . Por ejemplo, puede haber dos búferes de seguridad: uno que contenga los datos de los mensajes de entrada y el otro para el token de seguridad opaco de salida devuelto por el paquete de seguridad. El orden de los búferes de seguridad en el descriptor del búfer de seguridad no es importante, pero cada búfer se debe etiquetar con su tipo adecuado. Se puede usar una etiqueta de solo lectura con cualquier búfer de entrada que no deba modificar el [*paquete de seguridad*](../secgloss/s-gly.md).

Es importante el tamaño del búfer de salida que se espera que contenga el token de seguridad. Una aplicación puede encontrar el tamaño máximo del token de un paquete de seguridad durante la configuración inicial. La llamada a [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) devuelve una matriz de punteros a la información del paquete de seguridad. La estructura de información de paquetes de seguridad contiene el tamaño máximo de los tokens para cada paquete. En el ejemplo, la información está en el miembro **cbMaxToken** de la estructura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) . La misma información se puede obtener posteriormente mediante [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa).

La aplicación inicializa los punteros y tamaños de búfer en la descripción del búfer para indicar dónde se pueden encontrar los datos del mensaje y otra información.

Para obtener más información, consulte el [código de ejemplo SecBuffer y SecBufferDesc](secbuffer-and-secbufferdesc-example-code.md).

 

 
