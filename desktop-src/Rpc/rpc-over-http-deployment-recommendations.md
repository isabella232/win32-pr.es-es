---
title: Rpc a través de la implementación de HTTP Recomendaciones
description: En esta sección se documenta los procedimientos recomendados y las configuraciones de implementación recomendadas para lograr la máxima seguridad y rendimiento al usar RPC a través de HTTP.
ms.assetid: 83938a7d-77d0-45e8-b0a3-7b32ef768d83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faf05808b90c4c0809341a846c4f5aa9684fec27fb26425342ec7e25fa98076b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018405"
---
# <a name="rpc-over-http-deployment-recommendations"></a>Rpc a través de la implementación de HTTP Recomendaciones

En esta sección se documenta los procedimientos recomendados y las configuraciones de implementación recomendadas para lograr la máxima seguridad y rendimiento al usar RPC a través de HTTP. Las distintas configuraciones que se encuentran en este documento se aplican a distintas organizaciones en función de los distintos requisitos de tamaño, presupuesto y seguridad. Cada configuración también proporciona consideraciones de implementación útiles para determinar cuál es la mejor opción para un escenario determinado.

Para obtener información sobre escenarios de RPC a través de HTTP de gran volumen, consulte [Equilibrio de carga de RPC de Microsoft.](rpc-load-balancing.md)

Las siguientes recomendaciones se aplican a todas las configuraciones:

-   Use versiones de Windows que admiten RPC a través de HTTP v2.
-   Coloque IIS en el equipo que ejecuta el proxy RPC en modo IIS 6.0.
-   No permitir el acceso anónimo al directorio virtual del proxy RPC.
-   No habilite nunca la clave del Registro AllowAnonymous.
-   Haga que los clientes RPC a través de HTTP usen **certificateSubjectField** (consulte [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) para obtener más información) para comprobar que el proxy RPC al que se conectó es el proxy RPC que espera.
-   Configure la **clave del Registro ValidPorts** para que contenga solo las máquinas a las que se conectarán los clientes RPC a través de HTTP.
-   No use caracteres comodín en la **clave ValidPorts;** Si lo hace, puede ahorrar tiempo, pero una máquina completamente inesperada también puede ajustarse al carácter comodín.
-   Use SSL en RPC a través de clientes HTTP. Si se siguen las instrucciones establecidas en estas secciones, el cliente RPC a través de HTTP no podrá conectarse sin usar SSL.
-   Configure RPC a través de clientes HTTP para que usen el cifrado RPC además de usar SSL. Si el cliente RPC a través de HTTP no puede llegar al KDC, solo puede usar Negotiate y NTLM.
-   Configure las máquinas cliente para que usen NTLMv2. Establezca la **clave del Registro LMCompatibilityLevel** en 2 o superior. Consulte **msdn.microsoft.com** para obtener más información sobre la **clave LMCompatibilityLevel.**
-   Ejecute una granja de servidores web de máquinas de proxy RPC con la configuración descrita anteriormente.
-   Implemente un firewall entre Internet y el proxy RPC.
-   Para obtener un rendimiento óptimo, configure IIS para enviar una respuesta breve para los códigos de error no correctos. Dado que el consumidor de la respuesta de IIS es un proceso automatizado, no es necesario que se envíen explicaciones fáciles de usar al cliente. Simplemente el cliente RPC a través de HTTP los omitirá.

Los objetivos básicos del proxy RPC desde una perspectiva de seguridad, rendimiento y manejabilidad son los siguientes:

-   Proporcione un único punto de entrada para el tráfico RPC a través de HTTP en la red del servidor. Tener un único punto de entrada para el tráfico RPC a través de HTTP en una red de servidor tiene dos ventajas principales. En primer lugar, dado que el proxy RPC está orientado a Internet, la mayoría de las organizaciones aíslan estas máquinas en una red especial denominada red perimetral que no es de confianza y que es independiente de la red organizativa normal. Los servidores de una red perimetral que no es de confianza se administran, configuran y supervisan con mucho cuidado para poder resistir ataques desde Internet. Entre menos máquinas de una red perimetral que no sea de confianza, más fácil es configurarlas, administrarlas, supervisarlas y mantenerlas seguras. En segundo lugar, dado que una única granja de servidores web con servidores proxy RPC instalados puede dar servicio a cualquier número de servidores RPC a través de HTTP que residen en la red corporativa, tiene mucho sentido separar el proxy RPC de RPC a través del servidor HTTP y hacer que el proxy RPC resida en una red perimetral que no sea de confianza. Si el proxy RPC estaba en la misma máquina que la RPC a través del servidor HTTP, las organizaciones se verían forzadas a colocar todos sus servidores back-end en una red perimetral que no es de confianza, lo que dificultaría mucho la protección de la red perimetral que no es de confianza. Separar el rol del proxy RPC y el servidor RPC sobre HTTP ayuda a las organizaciones a mantener el número de máquinas en una red perimetral que no es de confianza y, por tanto, más segura.
-   Sirve como un dispositivo de seguridad para la red del servidor. El proxy RPC está diseñado como un fuse prescindible para la red del servidor: si algo sale mal en el proxy RPC, simplemente sale y, por tanto, protege la RPC real sobre el servidor HTTP. Si se han seguido los procedimientos recomendados descritos en esta sección hasta ahora, el tráfico RPC a través de HTTP se cifra con cifrado RPC además de SSL. El propio cifrado RPC está entre el cliente y el servidor, no entre el cliente y el proxy. Esto significa que el proxy no entiende y no puede descifrar el tráfico RPC que recibe. Solo entiende algunas secuencias de control que le envía el cliente que trabaja con el establecimiento de la conexión, el control de flujo y otros detalles de tunelización. No tiene acceso a los datos que el cliente RPC a través de HTTP envía al servidor. Además, el cliente RPC a través de HTTP debe autenticarse de forma independiente en el proxy RPC y en el servidor RPC a través de HTTP. Esto proporciona defensa en profundidad. Si la máquina del proxy RPC se pone en peligro, debido a algún error de configuración o a una infracción de seguridad de algún tipo, los datos que pasan a través de ella siguen estando protegidos contra alteraciones. Un atacante que obtendría el control del proxy RPC puede, como máximo, interrumpir el tráfico, pero no leerlo ni alterarlo. Aquí es donde entra en juego el rol de fusión del proxy RPC: es prescindible sin que la seguridad de la RPC sobre el tráfico HTTP se vea comprometida.
-   Distribuya algunas de las comprobaciones de acceso y el trabajo de descifrado entre varias máquinas que ejecutan el proxy RPC en una granja de servidores web. Al funcionar bien en una granja de servidores web, el proxy RPC permite a las organizaciones descargar el descifrado SSL y algunas de las comprobaciones de acceso, lo que libera más capacidad en el servidor back-end para su procesamiento. El uso de una granja de servidores web de máquinas de proxy RPC también permite a una organización aumentar su capacidad para resistir ataques por denegación de servicio (DoS) al aumentar la capacidad en sus servidores front-end.

Dentro de las directrices establecidas hasta ahora, las organizaciones todavía tienen opciones. Cada organización tiene opciones y riesgos entre las molestias del usuario, la seguridad y el costo:

-   **¿Usa la autenticación básica Windows autenticación integrada para autenticarse en el proxy RPC?** RPC a través de HTTP actualmente solo admite NTLM; no admite Kerberos. Además, si hay un proxy HTTP o un firewall entre el cliente  RPC a través de HTTP y el proxy RPC que inserta a través de pragma en el encabezado HTTP, la autenticación NTLM no funcionará. Cuando ese no es el caso, las organizaciones pueden elegir entre la autenticación básica y la autenticación NTLM. La ventaja de la autenticación básica es que es más rápida y sencilla y, por tanto, ofrece menos oportunidades para ataques por denegación de servicio. Pero NTLM es más seguro. En función de las prioridades de una organización, puede elegir Básico, NTLM o permitir que sus usuarios elijan entre las dos. Si solo se elige una, es mejor desactivar la otra del directorio virtual del proxy RPC para reducir el riesgo de ataque.
-   **Use el mismo conjunto de credenciales para el proxy RPC y el servidor RPC sobre HTTP, o use credenciales diferentes para cada una de ellas.** El equilibrio para esta decisión es entre la comodidad y la seguridad del usuario. A pocos usuarios les gusta escribir varias credenciales. Sin embargo, si se produce una infracción de seguridad en una red perimetral que no es de confianza, tener conjuntos de credenciales independientes para el proxy RPC y el servidor RPC sobre HTTP proporciona protección adicional. Tenga en cuenta que si se usan credenciales independientes y un conjunto de credenciales son las credenciales de dominio del usuario, es aconsejable usar las credenciales de dominio del usuario para rpc a través del servidor HTTP y no para el proxy RPC.

 

 




