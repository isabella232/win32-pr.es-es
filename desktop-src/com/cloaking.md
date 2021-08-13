---
title: Afición (COM)
description: La protección es una funcionalidad de seguridad COM que determina qué identidad proyecta el cliente hacia el servidor durante la suplantación.
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b5d36ec4561b0cc3290f21f4c46dc338b6df455bc694464812f2274b8c1345f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462985"
---
# <a name="cloaking-com"></a>Afición (COM)

La protección es una funcionalidad de seguridad COM que determina qué identidad proyecta el cliente hacia el servidor durante la suplantación. Cuando se establece la protección, el servidor intermedio enmascara su propia identidad y presenta la identidad del cliente al servidor al que llama en nombre del cliente. Básicamente; la identidad de cliente que ve el servidor es la identidad asociada al proxy. La identidad del proxy viene determinada por varios factores, uno de los cuales es el tipo de protección que se establece (si existe). El proveedor de seguridad de Schannel no admite la protección.

En los temas siguientes se proporciona más información sobre la protección:

-   [Tipos de contrabando](#types-of-cloaking)
-   [Cómo afecta la protección a la identidad de cliente](#how-cloaking-affects-client-identity)
-   [Establecimiento de la creación de un escenario](#setting-cloaking)
-   [Niveles de suplantación y suplantación](#cloaking-and-impersonation-levels)
-   [Escenarios de desarroba](#cloaking-scenarios)
-   [Temas relacionados](#related-topics)

## <a name="types-of-cloaking"></a>Tipos de contrabando

Hay dos tipos de contrabando: *el arrobamiento estático* y el *arroba* dinámico:

-   Con el arroba estático (EOAC STATIC ESTACIONES), el servidor ve el token de subproceso de la primera llamada de \_ \_ un cliente al servidor. Para la primera llamada, si la identidad de proxy se estableció previamente durante una llamada a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), se usa esa identidad de proxy. Sin embargo, si la identidad de proxy no se estableció previamente, se usa el token de subproceso. Si no hay ningún token de subproceso, se usa el token de proceso. Para todas las llamadas futuras, se usa la identidad establecida en la primera llamada.
-   Con el arroba dinámico (EOAC DYNAMIC ESTACIONES), en cada llamada se usa el token de subproceso actual (si hay un token de subproceso) para determinar la identidad \_ \_ del cliente. Si no hay ningún token de subproceso, se usa el token de proceso. Esto significa que los servidores a los que se llamó en nombre del cliente durante la suplantación ven la identidad del cliente COM que originó la llamada, que suele ser el comportamiento deseado. (Por supuesto, para que la suplantación se haga correctamente, el cliente debe haber dado la autoridad del servidor para suplantar estableciendo un nivel de suplantación adecuado. Para obtener más información, vea [Niveles de suplantación).](impersonation-levels.md) Este tipo de contrabando es costoso.

## <a name="how-cloaking-affects-client-identity"></a>Cómo afecta la protección a la identidad de cliente

Cuando se realiza una llamada cifrada y el servidor solicita al cliente su identidad, normalmente obtiene la identidad vinculada al proxy. (A veces, el servicio de autenticación realiza una traducción de la identidad real, pero generalmente la identidad de proxy es la identidad que ve el servidor). El proxy presenta una identidad al servidor que depende del tipo de protección que se establezca y otros factores.

En resumen, la identidad del cliente es una función del conjunto de marcas de protección, el token de proceso, la presencia o ausencia de un token de subproceso y si la identidad del proxy se ha establecido previamente. En la tabla siguiente se muestra la identidad de proxy resultante (identidad de cliente) cuando estos factores varían.



| Marcas de distintivo                     | Presencia de token de subproceso  | Identidad de proxy establecida previamente | Identidad de proxy (identidad de cliente)                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| No se establece el ajuste<br/>        | No le importa<br/>  | No le importa<br/>         | Token de proceso o identidad de autenticación<br/> |
| \_ARROBA ESTÁTICA DE EOAC \_<br/>  | Presente<br/>     | No<br/>                 | Token de subproceso<br/>                             |
| \_ARROBA ESTÁTICA DE EOAC \_<br/>  | Presente<br/>     | Sí<br/>                | Identidad de proxy actual<br/>                   |
| \_ARROBA ESTÁTICA DE EOAC \_<br/>  | No está presente<br/> | No<br/>                 | Token de proceso<br/>                            |
| \_ARROBA ESTÁTICA DE EOAC \_<br/>  | No está presente<br/> | Sí<br/>                | Identidad de proxy actual<br/>                   |
| \_ARROBA DINÁMICA DE EOAC \_<br/> | Presente<br/>     | No le importa<br/>         | Token de subproceso<br/>                             |
| \_ARROBA DINÁMICA DE EOAC \_<br/> | No está presente<br/> | No le importa <br/>        | Token de proceso<br/>                            |



 

En el diagrama de flujo siguiente se muestra cómo se determina la identidad del proxy en distintas situaciones.

![Diagrama que muestra el flujo para determinar la identidad del proxy.](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>Establecimiento de la creación de un escenario

La creación se establece como una marca de funcionalidad en una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), que establece el arroba para todo el proceso. A continuación, la funcionalidad de ocultación se establece hasta que el cliente la cambia a través de una llamada a IClientSecurity::[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o [**a CoSetProxyBlanket),**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)que establece el reanquiso para el proxy.

De forma predeterminada, no se establece el ajuste. Para establecerlo, pase EOAC \_ \_ STATICINITING o EOAC \_ \_ DYNAMICINITING al *parámetro pCapabilities* en [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket).

Cuando se habilita la creación estática mediante [**CoInitializeSecurity,**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)cada proxy toma un token (subproceso o proceso) la primera vez que realiza una llamada en el proxy. Cuando se habilita la estática mediante [**SetBlanket,**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket)el proxy recoge el token en el subproceso en ese momento. Si no hay ningún token de subproceso disponible cuando se llama a **SetBlanket,** el token de proceso se usa para la identidad del proxy. Básicamente, **SetBlanket** corrige la identidad del proxy.

Con la protección dinámica, la identidad del proxy se determina de la misma manera, independientemente de si la representación dinámica se establece mediante [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**con SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). El token de subproceso actual se usa si hay uno; De lo contrario, se usa el token de proceso.

Si se establece la creación para todo el proceso a través de una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y desea realizar llamadas con el token de proceso, no suplante al realizar llamadas.

## <a name="cloaking-and-impersonation-levels"></a>Niveles de suplantación y suplantación

Como se mencionó anteriormente, la funcionalidad de protección determina qué identidad se presenta a un servidor durante la suplantación. La protección proporciona una manera de que un servidor proyecte una identidad que no sea la suya propia a otro servidor al que llama en nombre del cliente. El nivel de suplantación indica cuánta autoridad ha dado el cliente al servidor.

La suplantación sin desaprobación funciona, pero puede que no sea la mejor opción porque, en algunos casos, el servidor final debe conocer la identidad del autor de la llamada inicial. Esto no se puede lograr sin usar la protección, ya que es difícil asegurarse de que solo los clientes autorizados puedan acceder a un equipo remoto. Cuando se usa la suplantación sin desenlazamiento, la identidad que se presenta a un servidor de bajada es la del proceso de llamada inmediato.

Sin embargo, la suplantación no resulta útil sin suplantación. La suplantación solo tiene sentido cuando el cliente ha establecido un nivel de suplantación de suplantación o delegado. (Con niveles de suplantación inferiores, el servidor no puede realizar llamadas desasistidos). Si la organización es correcta depende del número de límites del equipo cruzados y del nivel de suplantación, lo que indica cuánta autoridad tiene el servidor para actuar en nombre del cliente.

En algunas situaciones, tiene sentido que el servidor establezca la suplantación cuando el cliente establece el nivel de suplantación en RPC \_ C \_ IMP LEVEL \_ \_ IMPERSONATE. Sin embargo, hay ciertas limitaciones en vigor. Si el cliente original establece el nivel de suplantación en RPC \_ C \_ IMP LEVEL \_ IMPERSONATE, el servidor intermedio (que actúa como cliente en el mismo equipo) solo puede cruzar un límite \_ de equipo. Esto se debe a que un token de suplantación de nivel de suplantación solo se puede pasar a través de un límite de equipo. Una vez que se ha cruzado el límite del equipo, solo se puede acceder a los recursos locales. La identidad presentada al servidor depende del tipo de protección que se establezca. Si no se establece ninguna protección, la identidad presentada a un servidor será la del proceso que realiza la llamada inmediata.

Para pasar por encima de varios límites de equipo, debe especificar tanto una marca de funcionalidad de protección adecuada como una suplantación de nivel de delegado. Con este tipo de suplantación, las credenciales locales y de red del cliente se dan al servidor, por lo que el token de suplantación puede cruzar cualquier número de límites del equipo. Una vez más, la identidad presentada al servidor depende del tipo de protección que se establezca. Si no se establece ninguna suplantación de nivel de delegado, la identidad que se presenta a un servidor es la del proceso que realiza la llamada.

Por ejemplo, suponga que el proceso A llama a B y B llama a C. B ha establecido la suplantación y A ha establecido el nivel de suplantación para suplantar. Si A, B y C están en el mismo equipo, el paso del token de suplantación de A a B y, a continuación, a C funcionará. Pero si A y C están en el mismo equipo y B no, pasar el token funcionará entre A y B, pero no de B a C. Se producirá un error en la llamada de B a C porque B no puede llamar a C mientras se está desasoyendo. Sin embargo, si A establece el nivel de suplantación para delegar, el token se puede pasar de B a C y la llamada puede realizarse correctamente.

## <a name="cloaking-scenarios"></a>Escenarios de desarroba

En la siguiente ilustración, el proceso A llama a B, llama a C y llama a D cuando no se establece la desarroba. Como resultado, cada proceso intermedio ve la identidad del proceso que lo llamó.

![Diagrama en el que se muestra el proceso cuando no se establece el proceso de creación.](images/0d2eb6cf-97d6-4c4e-b97e-abad854b1120.png)

Con la estática, el servidor ve la identidad de proxy que se estableció durante la primera llamada del cliente al servidor. En la ilustración siguiente se muestra un ejemplo de la identidad de proxy que se establece durante una llamada de B a C. En una llamada posterior, el proceso D ve la identidad de B cuando B y C establecen el arroba estático.

![Diagrama que muestra el proceso de creación estática.](images/520938e0-c4a6-4ac1-937d-02baf2007a27.png)

Con la protección dinámica, la identidad del autor de la llamada durante la suplantación se basa en el token del subproceso actual, si lo hay. En la ilustración siguiente se muestra la situación en la que B y C establecen la dinámica y D ve la identidad de A, a pesar de una llamada anterior de B a C.

![Diagrama que muestra el proceso de creación dinámica.](images/d0848465-82f3-4d5a-851e-566d7800ada0.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Delegación y suplantación](delegation-and-impersonation.md)
</dt> </dl>

 

