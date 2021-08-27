---
description: Uno de los cambios más obvios de IPv4 a IPv6 es el tamaño de la dirección IP. Muchas interfaces de usuario proporcionan cuadros de diálogo que permiten a un usuario escribir una dirección IP, como se muestra en la ilustración siguiente.
ms.assetid: e2d7fd41-297a-400b-ae59-5d67db2be6f6
title: Interfaz de usuario problemas de aplicaciones IPv6 Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae982504798789c928691bbf4932d5e6abdfabf1ba12077122bb6dab28eb47de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121195"
---
# <a name="user-interface-issues-for-ipv6-winsock-applications"></a>Interfaz de usuario problemas de aplicaciones IPv6 Winsock

Uno de los cambios más obvios de IPv4 a IPv6 es el tamaño de la dirección IP. Muchas interfaces de usuario proporcionan cuadros de diálogo que permiten a un usuario escribir una dirección IP, como se muestra en la ilustración siguiente.

![cuadro de dirección ipv4 común en una interfaz de usuario](images/portingguide001.jpg)

El direccionamiento en IPv6, debido a muchos factores como la longitud, la complejidad y la importancia de las secciones dentro del espacio de direcciones IPv6, no es conveniente para la modificación o especificación por parte de los usuarios. Por lo tanto, se reduce la necesidad de proporcionar a los usuarios la capacidad de especificar su propia dirección. Además, debido a la complejidad asociada con el direccionamiento IPv6, no es probable que se produzcan problemas por nodo para proporcionar a los administradores la capacidad de especificar información de direcciones IPv6.

Mostrar una dirección IPv6 en la interfaz de usuario no es inconcebible y, por tanto, los desarrolladores deben tener en cuenta la variabilidad en el tamaño de una dirección IPv6 al modificar una aplicación para admitir IPv6.

En el resto de esta sección se describe la diferencia entre las consideraciones de predicción de longitud de direcciones IPv4 y longitud de direcciones IPv6. En esta sección se supone que las direcciones IPv6 se muestran en su representación hexadecimal.

Las direcciones IPv4 son de tamaño predecible, porque siguen rígidamente la notación decimal con puntos, como se muestra en el ejemplo de dirección siguiente:

``` syntax
10.10.256.1
```

Las direcciones IPv6 no son tan predecibles, debido a la convención de direcciones IPv6 que permite el uso de dos puntos (::) para representar una serie de ceros. Por lo tanto, las siguientes representaciones de direcciones IPv6 equivalen a la misma dirección IPv6:

``` syntax
1040:0:0:0:0:0:0:1
1040::1
```

La capacidad de representar una serie de ceros con un signo de dos puntos da como resultado una longitud imprevisible para cualquier IPv6 determinado, lo que requiere que los programadores tomen en cuenta esta funcionalidad al crear pantallas de interfaz de usuario de direcciones IPv6. Por supuesto, los desarrolladores deben asegurarse de que la interfaz de usuario sea capaz de mostrar direcciones IP que no usan dos puntos para representar una serie de ceros (primera dirección a continuación), así como de ser capaces de mostrar la dirección IPv6 más larga posible (segunda dirección a continuación, con la dirección IPv4 insertadas) al crear su interfaz de usuario compatible con IPv6. Tenga en cuenta también que agregar el identificador de ámbito (id.) a la siguiente dirección aumentaría su longitud hasta otros once caracteres:

``` syntax
21DA:00D3:0010:2F3B:02AA:00FF:FE28:9C5A
0000:0000:0000:0000:0000:ffff:123.123.123.123
```

Otra consideración importante es si las direcciones basadas en nombres son más adecuadas que las direcciones IPv6 basadas en números. Si las direcciones basadas en nombres son más adecuadas, debe tenerse en cuenta las convenciones de nomenclatura en la interfaz de usuario, incluida la comprobación de errores de entrada adecuada para la tarea.

Hay otras complejidades asociadas a la visualización de direcciones IPv6 que los desarrolladores deben tener en cuenta al modificar su aplicación y al diseñar representaciones de interfaz de usuario de direcciones IPv6. Algunas de estas consideraciones son las siguientes:

-   ¿La dirección debe contener todas las secuencias de ceros o usar la notación de dos puntos?
-   ¿Es más adecuado usar una representación de dirección basada en números o una representación basada en nombres?
-   ¿El usuario está interesado en distinguir un determinado aspecto del esquema de direccionamiento, como el prefijo de subred, el identificador de ámbito u otros subcampos?
-   ¿El usuario está interesado en determinar otros aspectos de la dirección, como el identificador de TLA, el identificador de NLA o el identificador del Acuerdo de Nivel de Servicio?
-   ¿La interfaz de usuario será capaz de distinguir direcciones IPv6 insertadas y, si es así, cómo se controlarán y mostrarán? ¿Distinguirá entre direcciones compatibles con IPv4 y direcciones IPv6 asignadas a IPv4 al mostrar información de direcciones al usuario?

También hay otras consideraciones, y los desarrolladores deben tener en cuenta cuidadosamente su audiencia de clientes al desarrollar interfaces de usuario de direcciones IP.

Prácticas recomendadas

-   Los desarrolladores deben tener en cuenta el enfoque adecuado para cada interfaz de usuario al modificar su aplicación para admitir IPv6. Asegurarse de que la interfaz de usuario contiene una longitud suficiente para mostrar direcciones IPv6 es imperativo, ya que determina si esa dirección se basa en el número o en el nombre.
-   Siempre que sea posible, use las funciones existentes winsock y del asistente de IP al usar direcciones IPv6 en lugar de volver a implementar esta lógica. Por ejemplo, las funciones [**RtlIpv6AddressToString,**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringa) [**RtlIpv6AddressToStringEx,**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6addresstostringexw) [**RtlIpv6StringToAddress**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressa)y [**RtlIpv6StringToAddressEx**](/windows/win32/api/ip2string/nf-ip2string-rtlipv6stringtoaddressexw) se pueden usar para convertir direcciones IPv6 y representaciones de cadena de estas direcciones IPv6.

Código que se debe evitar

-   Los elementos de la interfaz de usuario que dependen de una dirección de tamaño IPv4 deben someterse a examen y parte de ese examen debe incluir si la información que se proporciona (en IPv4) es adecuada para IPv6.
-   La capacidad de especificar una dirección IP también debe depender de si IPv4 está en uso o IPv6 está disponible. Si IPv6 está disponible, ¿es adecuado especificar direcciones basadas en números (hexadecimales) o direcciones basadas en nombres?

Tareas de codificación

**Para revisar la base de código existente de IPv4 a interoperabilidad IPv4 e IPv6**

1.  Realice una revisión visual de la interfaz de usuario, buscando cualquier elemento que dependa de una longitud específica para la cadena de dirección IP. Los controles con la notación decimal con puntos de cuatro secciones fácilmente identificada son fáciles de detectar, pero otros no. Puede haber lugares en los que se puedan mostrar direcciones IP, como en los cuadros de diálogo, donde una dirección IPv6 podría querse sin espacio para mostrar.
2.  Al encontrar cualquiera de estos controles, escrute si es adecuado mostrar la dirección cuando se usa IPv6. Si es posible que esté en uso IPv4 o IPv6, asegúrese de que la interfaz de usuario puede dar cabida a cualquiera de ellos. Reemplace o aumente los controles por controles de interfaz de usuario que puedan mostrar una dirección IPv6 completa.
3.  Realice un seguimiento de las pruebas de la interfaz de usuario para asegurarse de que los cambios que habilitan la presentación de direcciones IPv6 mantienen la facilidad de uso prevista al usar direcciones IPv4. Además, pruebe las ubicaciones de presentación de direcciones de protocolo, como los cuadros de diálogo informativos, para asegurarse de que controlan correctamente las direcciones IPv6.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Guía de IPv6 para Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Cambio de estructuras de datos para aplicaciones Winsock de IPv6](changing-data-structures-2.md)
</dt> <dt>

[Sockets de pila doble para aplicaciones Winsock IPv6](dual-stack-sockets.md)
</dt> <dt>

[Llamadas de función para aplicaciones IPv6 Winsock](function-calls-2.md)
</dt> <dt>

[Uso de direcciones IPv4 codificadas de forma rígida](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Protocolos subyacentes para aplicaciones IPv6 Winsock](underlying-protocols-2.md)
</dt> </dl>

 

 
