---
description: Uno de los cambios más obvios de IPv4 a IPv6 es el tamaño de la dirección IP. Muchas interfaces de usuario proporcionan cuadros de diálogo que permiten a los usuarios escribir una dirección IP, como se indica en la ilustración siguiente.
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03305073687cdd77e17c529d70ffe5959df40960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706945"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a>Problemas de la interfaz de usuario para las aplicaciones Winsock de IPv6

Uno de los cambios más obvios de IPv4 a IPv6 es el tamaño de la dirección IP. Muchas interfaces de usuario proporcionan cuadros de diálogo que permiten a los usuarios escribir una dirección IP, como se indica en la ilustración siguiente.

![cuadro de dirección IPv4 común en una interfaz de usuario](images/portingguide001.jpg)

El direccionamiento en IPv6, debido a muchos factores, como la longitud, la complejidad y la importancia de las secciones del espacio de direcciones IPv6, no es favorable para la modificación o la especificación de los usuarios. Por lo tanto, se reduce la necesidad de proporcionar a los usuarios la capacidad de especificar su propia dirección. Además, debido a la complejidad asociada al direccionamiento IPv6, no es probable que los administradores con la capacidad de especificar la información de la dirección IPv6 se produzcan por nodo.

Mostrar una dirección IPv6 en la interfaz de usuario no es inconcebible y, por lo tanto, los desarrolladores deben tener en cuenta la variabilidad del tamaño de una dirección IPv6 al modificar una aplicación para que admita IPv6.

En el resto de esta sección se describe la diferencia entre las consideraciones de predicción de longitud de dirección IPv4 y de longitud de direcciones IPv6. En esta sección se da por supuesto que las direcciones IPv6 se muestran en su representación hexadecimal.

Las direcciones IPv4 son predecibles en tamaño, ya que siguen la notación decimal con puntos, como se muestra en el siguiente ejemplo de dirección:

``` syntax
10.10.256.1
```

Las direcciones IPv6 no son tan predecibles, debido a la Convención de direcciones IPv6 que permite el uso de dos puntos dobles (::) para representar una serie de ceros. Como tal, las representaciones de direcciones IPv6 siguientes equivalen a la misma dirección IPv6:

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

La capacidad de representar una serie de ceros con dos puntos dobles da como resultado una longitud imprevisible para cualquier IPv6 determinado, que requiere que los programadores tomen esta capacidad en cuenta al crear las visualizaciones de la interfaz de usuario de las direcciones IPv6. En realidad, los desarrolladores deben asegurarse de que la interfaz de usuario es capaz de mostrar las direcciones IP que no usan un signo de dos puntos para representar una serie de ceros (la primera dirección que aparece a continuación), así como poder mostrar la dirección IPv6 más larga posible (segunda dirección a continuación, con la dirección IPv4 incrustada) al crear su interfaz de usuario compatible con IPv6. Tenga en cuenta también que agregar el identificador de ámbito (ID.) a la dirección siguiente aumentaría su longitud en un máximo de once caracteres:

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

Otra consideración importante es si las direcciones basadas en nombres son más adecuadas que las direcciones IPv6 basadas en números. Si las direcciones basadas en nombres son más adecuadas, tenga en cuenta que las convenciones de nomenclatura deben estar integradas en la interfaz de usuario, incluida la comprobación de errores de entrada adecuada para la tarea.

Hay otras complejidades asociadas a la visualización de las direcciones IPv6 que los desarrolladores deben tener en cuenta al modificar su aplicación y al diseñar representaciones de interfaz de usuario de direcciones IPv6. Algunas de estas consideraciones son las siguientes:

-   ¿Debe contener todas las secuencias de ceros la dirección o usar la notación de dos puntos dobles?
-   ¿Es más adecuado usar una representación de dirección basada en números o una representación basada en el nombre?
-   ¿El usuario está interesado en discernir un aspecto determinado del esquema de direccionamiento, como el prefijo de subred, el identificador de ámbito u otros subcampos?
-   ¿El usuario está interesado en determinar otros aspectos de la dirección, como el identificador de TLA, el identificador NLA o el identificador del contrato de nivel de servicio?
-   ¿La interfaz de usuario podrá distinguir las direcciones IPv6 incrustadas y, si es así, ¿cómo se controlarán y se mostrarán? ¿Se puede distinguir entre las direcciones compatibles con IPv4 y las direcciones IPv6 asignadas por IPv4 al Mostrar información de dirección al usuario?

También hay otras consideraciones, y los desarrolladores deben considerar detenidamente la audiencia del cliente al desarrollar interfaces de usuario de dirección IP.

Prácticas recomendadas

-   Los desarrolladores deben tener en cuenta el enfoque adecuado para cada interfaz de usuario al modificar la aplicación para que admita IPv6. Asegurarse de que la interfaz de usuario contenga la longitud suficiente para mostrar las direcciones IPv6 es fundamental, al igual que determina si esa dirección se basa en el número o en el nombre.
-   Siempre que sea posible, use las funciones auxiliares de Winsock y IP existentes al usar direcciones IPv6 en lugar de volver a implementar esta lógica. Por ejemplo, las funciones [**RtlIpv6AddressToString**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa), [**RtlIpv6AddressToStringEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw), [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)y [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) se pueden usar para realizar conversiones entre las direcciones IPv6 y las representaciones de cadena de estas direcciones IPv6.

Código que se debe evitar

-   Los elementos de la interfaz de usuario que dependen de una dirección de tamaño IPv4 deben someterse a los análisis y parte de ese escrutinio debe incluir si la información que estaba proporcionando (en IPv4) es adecuada para IPv6.
-   La capacidad de especificar una dirección IP también debe depender de si IPv4 está en uso o IPv6 está disponible. Si IPv6 está disponible, ¿es adecuado especificar direcciones basadas en números (hexadecimales) o direcciones basadas en nombres?

Tareas de codificación

**Para revisar la base de código existente de IPv4 a IPv4 e IPv6: interoperabilidad**

1.  Realice una revisión visual de la interfaz de usuario buscando cualquier elemento que dependa de una longitud concreta para la cadena de dirección IP. Los controles con la notación decimal con puntos de cuatro secciones identificada fácilmente son fáciles de identificar, pero otros no. Puede haber lugares en los que se puedan mostrar las direcciones IP, como en los cuadros de diálogo, donde una dirección IPv6 podría quedarse sin espacio para mostrar.
2.  Tras encontrar cualquiera de estos controles, examine si es adecuado mostrar la dirección al usar IPv6. Si es posible que IPv4 o IPv6 esté en uso, asegúrese de que la interfaz de usuario puede alojar cualquiera de las dos opciones. Reemplazar o aumentar los controles con controles de interfaz de usuario que pueden mostrar una dirección IPv6 completa.
3.  Siga las pruebas de la interfaz de usuario para asegurarse de que los cambios que habilitan la visualización de direcciones IPv6 mantienen la facilidad de uso prevista al usar direcciones IPv4. Además, pruebe las ubicaciones de presentación de la dirección de protocolo, como los cuadros de diálogo informativos, para asegurarse de que administran correctamente las direcciones IPv6.

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

[Uso de direcciones IPv4 codificadas](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Protocolos subyacentes para aplicaciones Winsock de IPv6](underlying-protocols-2.md)
</dt> </dl>

 

 
