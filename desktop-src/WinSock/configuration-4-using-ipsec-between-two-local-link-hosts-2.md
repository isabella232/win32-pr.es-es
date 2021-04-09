---
description: Esta configuración crea una asociación de seguridad (SA) de IPsec entre dos hosts de la misma subred para realizar la autenticación mediante el encabezado de autenticación (AH) y el algoritmo hash de síntesis del mensaje 5 (MD5).
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 'Configuración 3: uso de IPsec entre dos hosts de vínculo local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e7a760b6ae1ba87678d6061881e5eb80faf88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154295"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a>Configuración 3: uso de IPsec entre dos hosts de vínculo local

Esta configuración crea una asociación de seguridad (SA) de IPsec entre dos hosts de la misma subred para realizar la autenticación mediante el encabezado de autenticación (AH) y el algoritmo hash de síntesis del mensaje 5 (MD5). En este ejemplo, la configuración mostrada protege todo el tráfico entre dos hosts vecinos: host 1, con la dirección local del vínculo FE80:: 2AA: FF: FE53: A92C y el host 2, con la dirección local del vínculo FE80:: 2AA: FF: FE92: D0F1.

**Para usar IPsec entre dos hosts de vínculo local**

1.  En el host 1, cree archivos de Asociación de seguridad (SAD) y de directiva de seguridad (SPD) en blanco mediante el comando IPSEC6 c. En este ejemplo, el comando Ipsec6.exe es prueba de IPSEC6 c. Esto crea dos archivos para configurar manualmente las asociaciones de seguridad (test. Sad) y las directivas de seguridad (test. SPD).
2.  En el host 1, edite el archivo SPD para agregar una directiva de seguridad que proteja todo el tráfico entre el host 1 y el host 2.

    En la tabla siguiente se muestra la Directiva de seguridad agregada al archivo test. SPD antes de la primera entrada de este ejemplo (la primera entrada del archivo test. SPD no se modificó).

    | Nombre del campo del archivo SPD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **Directiva**          | 2                          |
    | **RemoteIPAddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocolo**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **ENCABEZADO**                     |
    | **IPSecMode**       | **Porta**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Dirección**       | **Bidireccionales**               |
    | **Acción**          | **APLICA**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta directiva de seguridad. Las entradas de la Directiva deben colocarse en orden numérico decreciente.

3.  En el host 1, edite el archivo SAD y agregue entradas SA para proteger todo el tráfico entre el host 1 y el host 2. Se deben crear dos asociaciones de seguridad, una para el tráfico al host 2 y otra para el tráfico del host 2.

    En la tabla siguiente se muestra la primera entrada SA agregada al archivo test. Sad para este ejemplo (para el tráfico al host 2).

    | Nombre del campo de archivo SAD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **DestIPAddr**      | **DIRECTIVA**                 |
    | **SrcIPAddr**       | **DIRECTIVA**                 |
    | **Protocolo**        | **DIRECTIVA**                 |
    | **DestPort**        | **DIRECTIVA**                 |
    | **SrcPort**         | **DIRECTIVA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Prueba. clave**               |
    | **Dirección**       | **SALIDA**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta SA.

    En la tabla siguiente se muestra la segunda entrada SA agregada al archivo test. Sad para este ejemplo (para el tráfico del host 2).

    | Nombre del campo de archivo SAD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **DestIPAddr**      | **DIRECTIVA**                 |
    | **SrcIPAddr**       | **DIRECTIVA**                 |
    | **Protocolo**        | **DIRECTIVA**                 |
    | **DestPort**        | **DIRECTIVA**                 |
    | **SrcPort**         | **DIRECTIVA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Prueba. clave**               |
    | **Dirección**       | **ENTRADA**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta SA. Las entradas SA deben colocarse en orden numérico decreciente.

4.  En el host 1, cree un archivo de texto que contenga una cadena de texto que se usa para autenticar la SAs creada con el host 2. En este ejemplo, el archivo test. Key se crea con el contenido "This is a test". Debe incluir comillas dobles alrededor de la cadena de clave para que la herramienta IPSEC6 Lea la clave.

    Microsoft IPv6 Technology Preview solo admite claves configuradas manualmente para la autenticación de las SA de IPsec. Las claves manuales se configuran creando archivos de texto que contienen la cadena de texto de la tecla manual. En este ejemplo, se usa la misma clave para la SAs en ambas direcciones. Puede usar claves diferentes para las SA de entrada y salida mediante la creación de diferentes archivos de clave y la referencia a ellos con el campo KeyFile en el archivo SAD.

5.  En el host 2, cree archivos de Asociación de seguridad (SAD) y de directiva de seguridad (SPD) en blanco mediante el comando IPSEC6 c. En este ejemplo, el comando Ipsec6.exe es prueba de IPSEC6 c. Esto crea dos archivos con entradas en blanco para la configuración manual de las asociaciones de seguridad (test. Sad) y las directivas de seguridad (test. SPD).

    Para simplificar el ejemplo, se usan los mismos nombres de archivo para los archivos SAD y SPD en el host 2. Puede optar por utilizar nombres de archivo diferentes en cada host.

6.  En el host 2, edite el archivo SPD para agregar una directiva de seguridad que proteja todo el tráfico entre el host 2 y el host 1.

    En la tabla siguiente se muestra la entrada de la Directiva de seguridad agregada antes de la primera entrada al archivo test. SPD para este ejemplo (la primera entrada del archivo test. SPD no se modificó).

    | Nombre del campo del archivo SPD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **Directiva**          | 2                          |
    | **RemoteIPAddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocolo**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **ENCABEZADO**                     |
    | **IPSecMode**       | **Porta**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Dirección**       | **Bidireccionales**               |
    | **Acción**          | **APLICA**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta directiva de seguridad. Las entradas de la Directiva deben colocarse en orden numérico decreciente.

7.  En el host 2, edite el archivo SAD y agregue entradas SA para proteger todo el tráfico entre el host 2 y el host 1. Se deben crear dos asociaciones de seguridad: una para el tráfico al host 1 y otra para el tráfico desde el host 1.

    En la tabla siguiente se muestra la primera SA agregada al archivo test. Sad para este ejemplo (para el tráfico desde el host 1).

    | Nombre del campo de archivo SAD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE92: D0F1** |
    | **DestIPAddr**      | **DIRECTIVA**                 |
    | **SrcIPAddr**       | **DIRECTIVA**                 |
    | **Protocolo**        | **DIRECTIVA**                 |
    | **DestPort**        | **DIRECTIVA**                 |
    | **SrcPort**         | **DIRECTIVA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Prueba. clave**               |
    | **Dirección**       | **ENTRADA**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta SA.

    En la tabla siguiente se muestra la segunda entrada SA agregada al archivo test. Sad para este ejemplo (para el tráfico al host 1).

    | Nombre del campo de archivo SAD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80:: 2AA: FF: FE53: A92C** |
    | **DestIPAddr**      | **DIRECTIVA**                 |
    | **SrcIPAddr**       | **DIRECTIVA**                 |
    | **Protocolo**        | **DIRECTIVA**                 |
    | **DestPort**        | **DIRECTIVA**                 |
    | **SrcPort**         | **DIRECTIVA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Prueba. clave**               |
    | **Dirección**       | **SALIDA**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta SA. Las entradas SA deben colocarse en orden numérico decreciente.

8.  En el host 2, cree un archivo de texto que contenga una cadena de texto que se usa para autenticar la SAs creada con el host 1. En este ejemplo, el archivo test. Key se crea con el contenido "This is a test". Debe incluir comillas dobles alrededor de la cadena de clave para que la herramienta IPSEC6 Lea la clave.
9.  En el host 1, agregue las directivas de seguridad configuradas y las SA desde los archivos SPD y SAD mediante el comando IPSEC6 a. En este ejemplo, se ejecuta el comando IPSEC6 a test en el host 1.
10. En el host 2, agregue las directivas de seguridad configuradas y las SA desde los archivos SPD y SAD mediante el comando IPSEC6 a. En este ejemplo, se ejecuta el comando IPSEC6 a test en el host 2.
11. Haga ping al host 1 desde el host 2 con el comando ping6.

    Si captura el tráfico mediante Monitor de red de Microsoft u otro rastreador de paquetes, debería ver el intercambio de mensajes de solicitud de eco ICMPv6 y de respuesta de eco con un encabezado de autenticación entre el encabezado IPv6 y el encabezado ICMPv6.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones recomendadas para IPv6](recommended-configurations-2.md)
</dt> <dt>

[Subred única con direcciones locales de vínculo](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Tráfico IPv6 entre nodos en distintas subredes de una red IPv4 (6to4)](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



