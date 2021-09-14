---
description: Esta configuración crea una asociación de seguridad (SA) de IPsec entre dos hosts de la misma subred para realizar la autenticación mediante el encabezado de autenticación (AH) y el algoritmo hash message digest 5 (MD5).
ms.assetid: ed88d8ee-ac65-4310-a988-ead50ff743fd
title: 'Configuración 3: Uso de IPsec entre dos hosts de vínculo local'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994e7a760b6ae1ba87678d6061881e5eb80faf88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068290"
---
# <a name="configuration-3-using-ipsec-between-two-local-link-hosts"></a>Configuración 3: Uso de IPsec entre dos hosts de vínculo local

Esta configuración crea una asociación de seguridad (SA) de IPsec entre dos hosts de la misma subred para realizar la autenticación mediante el encabezado de autenticación (AH) y el algoritmo hash message digest 5 (MD5). En este ejemplo, la configuración mostrada protege todo el tráfico entre dos hosts vecinos: Host 1, con la dirección local de vínculo FE80::2AA:FF:FE53:A92C y Host 2, con la dirección local de vínculo FE80::2AA:FF:FE92:D0F1.

**Para usar IPsec entre dos hosts de vínculo local**

1.  En el host 1, cree archivos de asociación de seguridad en blanco (SAD) y de directiva de seguridad (SPD) mediante el comando c de ipsec6. En este ejemplo, el Ipsec6.exe es ipsec6 c test. Esto crea dos archivos para configurar manualmente las asociaciones de seguridad (Test.sad) y las directivas de seguridad (Test.spd).
2.  En el host 1, edite el archivo SPD para agregar una directiva de seguridad que proteja todo el tráfico entre el host 1 y el host 2.

    En la tabla siguiente se muestra la directiva de seguridad agregada al archivo Test.spd antes de la primera entrada de este ejemplo (no se modificó la primera entrada del archivo Test.spd).

    | Nombre del campo de archivo SPD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **Directiva**          | 2                          |
    | **RemoteIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocolo**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **AH**                     |
    | **IPSecMode**       | **TRANSPORTE**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Dirección**       | **BIDIRECT**               |
    | **Acción**          | **APLICAR**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta directiva de seguridad. Las entradas de directiva deben colocarse en orden numérico decreciente.

3.  En el host 1, edite el archivo SAD y agregue entradas sa para proteger todo el tráfico entre el host 1 y el host 2. Se deben crear dos asociaciones de seguridad, una para el tráfico al host 2 y otra para el tráfico del host 2.

    En la tabla siguiente se muestra la primera entrada de SA agregada al archivo Test.sad para este ejemplo (para el tráfico al host 2).

    | Nombre del campo de archivo SAD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **DestIPAddr**      | **DIRECTIVA**                 |
    | **SrcIPAddr**       | **DIRECTIVA**                 |
    | **Protocolo**        | **DIRECTIVA**                 |
    | **DestPort**        | **DIRECTIVA**                 |
    | **SrcPort**         | **DIRECTIVA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Dirección**       | **SALIENTE**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque un punto y coma al final de la línea que configura este SA.

    En la tabla siguiente se muestra la segunda entrada de SA agregada al archivo Test.sad para este ejemplo (para el tráfico del host 2).

    | Nombre del campo de archivo SAD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **DestIPAddr**      | **DIRECTIVA**                 |
    | **SrcIPAddr**       | **DIRECTIVA**                 |
    | **Protocolo**        | **DIRECTIVA**                 |
    | **DestPort**        | **DIRECTIVA**                 |
    | **SrcPort**         | **DIRECTIVA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Dirección**       | **ENTRANTES**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque un punto y coma al final de la línea que configura este SA. Las entradas sa deben colocarse en orden numérico decreciente.

4.  En el host 1, cree un archivo de texto que contenga una cadena de texto que se usa para autenticar las SAs creadas con el host 2. En este ejemplo, el archivo Test.key se crea con el contenido "This is a test". Debe incluir comillas dobles alrededor de la cadena de clave para que la herramienta ipsec6 lea la clave.

    Microsoft IPv6 Technology Preview solo admite claves configuradas manualmente para la autenticación de saE de IPsec. Las claves manuales se configuran mediante la creación de archivos de texto que contienen la cadena de texto de la clave manual. En este ejemplo, se usa la misma clave para las as en ambas direcciones. Puede usar claves diferentes para LAS entrantes y salientes mediante la creación de diferentes archivos de clave y la referencia a ellos con el campo KeyFile del archivo SAD.

5.  En el host 2, cree archivos de asociación de seguridad (SAD) y de directiva de seguridad (SPD) en blanco mediante el comando c de ipsec6. En este ejemplo, el Ipsec6.exe comando es ipsec6 c test. Esto crea dos archivos con entradas en blanco para configurar manualmente las asociaciones de seguridad (Test.sad) y las directivas de seguridad (Test.spd).

    Para simplificar el ejemplo, se usan los mismos nombres de archivo para los archivos SAD y SPD en el host 2. Puede elegir usar nombres de archivo diferentes en cada host.

6.  En host 2, edite el archivo SPD para agregar una directiva de seguridad que proteja todo el tráfico entre host 2 y host 1.

    En la tabla siguiente se muestra la entrada de directiva de seguridad agregada antes de la primera entrada al archivo Test.spd para este ejemplo (no se modificó la primera entrada del archivo Test.spd).

    | Nombre del campo de archivo SPD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **Directiva**          | 2                          |
    | **RemoteIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **LocalIPAddr**     | \*                         |
    | **RemotePort**      | \*                         |
    | **Protocolo**        | \*                         |
    | **LocalPort**       | \*                         |
    | **IPSecProtocol**   | **AH**                     |
    | **IPSecMode**       | **TRANSPORTE**              |
    | **RemoteGWIPAddr**  | \*                         |
    | **SABundleIndex**   | **NONE**                   |
    | **Dirección**       | **BIDIRECT**               |
    | **Acción**          | **APLICAR**                  |
    | **InterfaceIndex**  | 0                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta directiva de seguridad. Las entradas de directiva deben colocarse en orden numérico decreciente.

7.  En el host 2, edite el archivo SAD y agregue entradas sa para proteger todo el tráfico entre host 2 y host 1. Se deben crear dos asociaciones de seguridad: una para el tráfico al host 1 y otra para el tráfico del host 1.

    En la tabla siguiente se muestra el primer SA agregado al archivo Test.sad para este ejemplo (para el tráfico del host 1).

    | Nombre del campo de archivo SAD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 2                          |
    | **SPI**             | 3001                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE92:D0F1** |
    | **DestIPAddr**      | **DIRECTIVA**                 |
    | **SrcIPAddr**       | **DIRECTIVA**                 |
    | **Protocolo**        | **DIRECTIVA**                 |
    | **DestPort**        | **DIRECTIVA**                 |
    | **SrcPort**         | **DIRECTIVA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Dirección**       | **ENTRANTES**                |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta SA.

    En la tabla siguiente se muestra la segunda entrada de SA agregada al archivo Test.sad para este ejemplo (para el tráfico al host 1).

    | Nombre del campo de archivo SAD | Valor de ejemplo              |
    |---------------------|----------------------------|
    | **SAEntry**         | 1                          |
    | **SPI**             | 3000                       |
    | **SADestIPAddr**    | **FE80::2AA:FF:FE53:A92C** |
    | **DestIPAddr**      | **DIRECTIVA**                 |
    | **SrcIPAddr**       | **DIRECTIVA**                 |
    | **Protocolo**        | **DIRECTIVA**                 |
    | **DestPort**        | **DIRECTIVA**                 |
    | **SrcPort**         | **DIRECTIVA**                 |
    | **AuthAlg**         | **HMAC-MD5**               |
    | **KeyFile**         | **Test.key**               |
    | **Dirección**       | **SALIENTE**               |
    | **SecPolicyIndex**  | 2                          |

    

     

    Coloque un punto y coma al final de la línea que configura esta SA. Las entradas de SA deben colocarse en orden numérico decreciente.

8.  En el host 2, cree un archivo de texto que contenga una cadena de texto que se usa para autenticar las as creadas con el host 1. En este ejemplo, el archivo Test.key se crea con el contenido "This is a test". Debe incluir comillas dobles alrededor de la cadena de clave para que la herramienta ipsec6 lea la clave.
9.  En el host 1, agregue las directivas de seguridad y las SA configuradas desde los archivos SPD y SAD mediante el comando ipsec6 a. En este ejemplo, ipsec6 ejecuta un comando de prueba en el host 1.
10. En el host 2, agregue las directivas de seguridad y las SA configuradas desde los archivos SPD y SAD mediante el comando ipsec6 a. En este ejemplo, se ejecuta un comando de prueba ipsec6 en el host 2.
11. Haga ping al host 1 desde el host 2 con el comando ping6.

    Si captura el tráfico mediante Monitor de red de Microsoft u otro intercambio de paquetes, debería ver el intercambio de mensajes de solicitud de eco ICMPv6 y respuesta de eco con un encabezado de autenticación entre el encabezado IPv6 y el encabezado ICMPv6.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuraciones recomendadas para IPv6](recommended-configurations-2.md)
</dt> <dt>

[Subred única con direcciones locales de vínculo](configuration-1-single-subnet-with-link-local-addresses-2.md)
</dt> <dt>

[Tráfico IPv6 entre nodos en subredes diferentes de una red de internet IPv4 (6to4)](configuration-2-ipv6-traffic-between-nodes-on-different-subnets-of-an-ipv4-internetwork-6to4--2.md)
</dt> </dl>

 

 



