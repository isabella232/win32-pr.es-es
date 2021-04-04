---
title: Recomendaciones de implementación de RPC sobre HTTP
description: En esta sección se documentan los procedimientos recomendados y las configuraciones de implementación recomendadas para lograr la máxima seguridad y rendimiento cuando se usa RPC a través de HTTP.
ms.assetid: 83938a7d-77d0-45e8-b0a3-7b32ef768d83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8871686d1fc8b87bcd6fb7ac4314b1977252f23a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076179"
---
# <a name="rpc-over-http-deployment-recommendations"></a>Recomendaciones de implementación de RPC sobre HTTP

En esta sección se documentan los procedimientos recomendados y las configuraciones de implementación recomendadas para lograr la máxima seguridad y rendimiento cuando se usa RPC a través de HTTP. Las distintas configuraciones que se encuentran en este documento se aplican a diferentes organizaciones en función de los distintos tamaños, presupuestos y requisitos de seguridad. Cada configuración también proporciona consideraciones de implementación útiles para determinar cuál es la mejor opción para un escenario determinado.

Para obtener información sobre escenarios de RPC a través de HTTP de gran volumen, consulte [equilibrio de carga de Microsoft RPC](rpc-load-balancing.md).

Las siguientes recomendaciones se aplican a todas las configuraciones:

-   Usar versiones de Windows compatibles con RPC a través de HTTP V2.
-   Ponga IIS en el equipo que ejecuta el proxy RPC en modo IIS 6,0.
-   No permitir el acceso anónimo al directorio virtual del proxy RPC.
-   No habilite nunca la clave del registro AllowAnonymous.
-   Haga que los clientes RPC a través de HTTP usen **CertificateSubjectField** (consulte [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para obtener más información) para comprobar que el proxy RPC al que se ha conectado es el proxy RPC que espera.
-   Configure la clave del registro **ValidPorts** para que contenga solo los equipos a los que se conectarán los clientes RPC a través de http.
-   No utilice caracteres comodín en la clave **ValidPorts** ; Si lo hace, puede ahorrar tiempo, pero un equipo completamente inesperado también puede ajustar el carácter comodín.
-   Usar SSL en clientes RPC a través de HTTP. Si se siguen las directrices establecidas en estas secciones, el cliente RPC a través de HTTP no podrá conectarse sin usar SSL.
-   Configure los clientes RPC a través de HTTP para usar el cifrado RPC además de usar SSL. Si el cliente RPC a través de HTTP no puede tener acceso al KDC, solo puede usar Negotiate y NTLM.
-   Configure los equipos cliente para que usen NTLMv2. Establezca la clave del registro **LMCompatibilityLevel** en 2 o superior. Vea **msdn.Microsoft.com** para obtener más información sobre la clave **LMCompatibilityLevel** .
-   Ejecute una granja de servidores Web de máquinas proxy RPC con la configuración descrita anteriormente.
-   Implementar un firewall entre Internet y el proxy RPC.
-   Para obtener un rendimiento óptimo, configure IIS para que envíe una respuesta corta para los códigos de error que no se hayan realizado correctamente. Dado que el consumidor de la respuesta de IIS es un proceso automatizado, no es necesario que se envíen explicaciones fáciles de usar al cliente. simplemente se omitirán por el cliente RPC a través de HTTP.

Los objetivos básicos del proxy RPC desde el punto de vista de la seguridad, el rendimiento y la facilidad de administración son los siguientes:

-   Proporcionar un único punto de entrada para el tráfico de RPC a través de HTTP en la red del servidor. Tener un único punto de entrada para el tráfico de RPC a través de HTTP en una red de servidor tiene dos ventajas principales. En primer lugar, como el proxy RPC está orientado a Internet, la mayoría de las organizaciones aíslan esas máquinas en una red especial denominada red perimetral que no es de confianza, que es independiente de la red de la organización normal. Los servidores de una red perimetral que no es de confianza se administran, configuran y supervisan cuidadosamente para poder resistir ataques de Internet. Cuanto menor sea el número de máquinas en una red perimetral que no sea de confianza, más fácil será configurar, administrar, supervisar y mantener la seguridad. En segundo lugar, puesto que una sola granja de servidores web con servidores proxy RPC instalados puede atender cualquier número de servidores RPC a través de HTTP que residan en la red corporativa, tiene mucho sentido separar el proxy RPC del servidor RPC a través de HTTP y hacer que el proxy RPC se encuentre en una red perimetral que no es de confianza. Si el proxy RPC estaba en el mismo equipo que el servidor RPC a través de HTTP, se forzaría a las organizaciones a poner todos los servidores back-end en una red perimetral que no sea de confianza, lo que dificultaría la protección de la red perimetral que no es de confianza. Separar el rol del proxy RPC y el servidor RPC a través de HTTP ayuda a las organizaciones a mantener el número de equipos en una red perimetral que no es de confianza y, por tanto, más seguros.
-   Actúe como fusible de seguridad para la red del servidor. El proxy RPC está diseñado como un fusible que se va a asignar a la red del servidor; si algo sale mal en el proxy RPC, simplemente se queda fuera y, por tanto, se protege el servidor RPC real a través de HTTP. Si se han seguido los procedimientos recomendados descritos en esta sección, el tráfico de RPC a través de HTTP se cifra con el cifrado RPC además de SSL. El propio cifrado RPC se encuentra entre el cliente y el servidor, no entre el cliente y el proxy. Esto significa que el proxy no entiende y no puede descifrar el tráfico RPC que recibe. Solo entiende algunas secuencias de control que le envía el cliente que trabaja con el establecimiento de la conexión, el control de flujo y otros detalles de tunelización. No tiene acceso a los datos que el cliente RPC a través de HTTP envía al servidor. Además, el cliente RPC a través de HTTP debe autenticarse de forma independiente en el servidor proxy RPC y el servidor RPC a través de HTTP. Esto proporciona una defensa en profundidad. Si la máquina del proxy RPC se ve comprometida, debido a un error de configuración o a una infracción de seguridad de alguna ordenación, los datos que pasan a través de ella siguen siendo seguros contra la manipulación. Un atacante que obtenga el control del proxy RPC puede, como máximo, interrumpir el tráfico, pero no leerlo ni manipularlo. Aquí es donde entra en juego el rol del fusible del proxy RPC, es el que es más fácil sin la seguridad del tráfico de RPC a través de HTTP en peligro.
-   Distribuya algunas de las comprobaciones de acceso y el trabajo de descifrado entre varios equipos que ejecutan el proxy RPC en una granja de servidores Web. Al funcionar bien en una granja de servidores Web, el proxy RPC permite a las organizaciones descargar el descifrado SSL y algunas de las comprobaciones de acceso, con lo que se libera más capacidad en el servidor back-end para su procesamiento. El uso de una granja de servidores Web de máquinas proxy RPC también permite a una organización aumentar su capacidad para resistir ataques de denegación de servicio (DoS) al aumentar la capacidad en sus servidores front-end.

Dentro de las directrices establecidas hasta el momento, las organizaciones todavía tienen opciones. Cada organización tiene opciones y peligros entre las molestias de los usuarios, la seguridad y el costo:

-   **¿Usar la autenticación básica o la autenticación integrada de Windows para autenticarse en el proxy RPC?** RPC a través de HTTP admite actualmente solo NTLM; no es compatible con Kerberos. Además, si hay un proxy HTTP o un firewall entre el cliente RPC a través de HTTP y el proxy RPC que inserta el *a través* de pragma en el encabezado HTTP, la autenticación NTLM no funcionará. Si no es así, las organizaciones pueden elegir entre la autenticación básica y NTLM. La ventaja de la autenticación básica es que es más rápida y más sencilla y, por lo tanto, ofrece menos oportunidades de ataques de denegación de servicio. Pero NTLM es más seguro. En función de las prioridades de la organización, puede elegir básico, NTLM o permitir que los usuarios elijan entre los dos. Si solo se elige uno, es mejor desactivar el otro del directorio virtual del proxy RPC para reducir el riesgo de ataque.
-   **¿Usar el mismo conjunto de credenciales para el proxy RPC y el servidor RPC a través de HTTP, o bien usar credenciales diferentes para cada uno?** La desventaja de esta decisión es entre la comodidad y la seguridad del usuario. Pocos usuarios desean escribir varias credenciales. Sin embargo, si se produce una infracción de seguridad en una red perimetral que no es de confianza, tener conjuntos independientes de credenciales para el proxy RPC y el servidor RPC a través de HTTP proporciona protección adicional. Tenga en cuenta que si se usan credenciales independientes y un conjunto de credenciales son las credenciales de dominio del usuario, es aconsejable utilizar las credenciales de dominio del usuario para el servidor RPC a través de HTTP y no para el proxy RPC.

 

 




