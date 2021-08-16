---
description: La comunicación suele implicar grandes cantidades de datos o datos de longitud desconocida.
ms.assetid: e7b12b9e-8caa-4dad-b81f-b609ccb92c9f
title: Uso de SecBufferDesc y SecBuffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ad12120414a1e0acb7a6b1cfe211b0ed1787d9e676e8329df1e16ecfef17cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785915"
---
# <a name="using-secbufferdesc-and-secbuffer"></a>Uso de SecBufferDesc y SecBuffer

La comunicación suele implicar grandes cantidades de datos o datos de longitud desconocida. El envío y la recepción de datos se realiza de forma similar o idéntica en ambos casos. Para tratar con longitud desconocida y cantidades potencialmente grandes de datos, la comunicación SSPI se realiza mediante dos estructuras, [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) y [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer).

Una [**estructura SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) es un contenedor para una matriz de [**estructuras SecBuffer.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) Una **estructura SecBufferDesc** tiene los siguientes miembros:

-   Número de la versión
-   Número de [**elementos SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)
-   Dirección de la matriz de [**estructuras SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Una [**estructura SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) contiene los tres miembros siguientes:

-   Número de bytes en el búfer
-   Tipo de información contenida en el elemento de datos
-   Los propios bytes

Un mensaje SSPI completo suele constar de una matriz de estructuras [**SecBuffer.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer)

Los siguientes tipos de datos de búfer se definen de la manera siguiente.



| Tipo de búfer                | Significado                                                                                                                                |
|----------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| SECBUFFER \_ EMPTY           | Sin definir, reemplazado por la función [*de paquete de*](../secgloss/s-gly.md) seguridad |
| DATOS \_ SECBUFFER            | Datos de paquetes                                                                                                                            |
| TOKEN DE \_ SECBUFFER           | Token de seguridad                                                                                                                         |
| SECBUFFER \_ PKG \_ PARAMS     | Parámetros específicos del paquete                                                                                                            |
| FALTA \_ SECBUFFER         | Indicador de datos que faltan                                                                                                                 |
| SECBUFFER \_ EXTRA           | Datos adicionales                                                                                                                             |
| SECUENCIA \_ SECBUFFER          | Datos de flujo de seguridad                                                                                                                   |
| FINALIZADOR DE \_ SECUENCIAS DE \_ SECBUFFER | Finalizador de flujo de seguridad                                                                                                                |
| SECBUFFER \_ STREAM \_ HEADER  | Encabezado de flujo de seguridad                                                                                                                 |



 

Los tipos de búfer anteriores se pueden combinar mediante una operación **OR** bit a bit con cualquiera de los siguientes tipos de búfer.



| Tipo de búfer         | Significado                                                                          |
|---------------------|----------------------------------------------------------------------------------|
| SECBUFFER \_ ATTRMASK | Enmascara los atributos de seguridad separando las marcas de atributo del tipo de búfer. |
| SECBUFFER \_ READONLY | El búfer es de solo lectura                                                              |



 

Antes de cada llamada a una API de SSPI que requiere un parámetro [**SecBufferDesc,**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) se declaran e inicializan uno o varios elementos de la matriz [**SecBuffer.**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) Por ejemplo, puede haber dos búferes de seguridad: uno que contiene los datos del mensaje de entrada y el otro para el token de seguridad opaco de salida devuelto por el paquete de seguridad. El orden de los búferes de seguridad en el descriptor del búfer de seguridad no es importante, pero cada búfer debe etiquetarse con su tipo adecuado. Se puede usar una etiqueta de solo lectura con cualquier búfer de entrada que el paquete de seguridad no deba [*modificar.*](../secgloss/s-gly.md)

El tamaño del búfer de salida que se espera que contenga el token de seguridad es importante. Una aplicación puede encontrar el tamaño máximo del token para un paquete de seguridad durante la instalación inicial. La llamada a [**EnumerateSecurityPackages**](/windows/desktop/api/Sspi/nf-sspi-enumeratesecuritypackagesa) devuelve una matriz de punteros a la información del paquete de seguridad. La estructura de información del paquete de seguridad contiene el tamaño máximo del token para cada paquete. En el ejemplo, la información está en el **miembro cbMaxToken** de la [**estructura SecPkgInfo.**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) La misma información se puede obtener más adelante mediante [**QuerySecurityPackageInfo**](/windows/desktop/api/Sspi/nf-sspi-querysecuritypackageinfoa).

La aplicación inicializa los punteros y tamaños de búfer en la descripción del búfer para indicar dónde se pueden encontrar los datos del mensaje y otra información.

Para obtener más información, [vea SecBuffer y SecBufferDesc Example Code](secbuffer-and-secbufferdesc-example-code.md).

 

 
