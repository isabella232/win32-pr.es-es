---
title: Cloaking (COM)
description: La ocultación es una funcionalidad de seguridad COM que determina qué identidad proyecta el cliente hacia el servidor durante la suplantación.
ms.assetid: 5b97d9d6-8fa9-4da2-8351-64772227d9a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588651cfa37def4e174ef0f2fdba9b79b0c60ca8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "103913934"
---
# <a name="cloaking-com"></a>Cloaking (COM)

La ocultación es una funcionalidad de seguridad COM que determina qué identidad proyecta el cliente hacia el servidor durante la suplantación. Cuando se establece Cloaking, el servidor intermedio enmascara su propia identidad y presenta la identidad del cliente al servidor al que llama en nombre del cliente. Básicamente la identidad del cliente que detecta el servidor es la identidad asociada con el proxy. La identidad del proxy viene determinada por varios factores, uno de los cuales es el tipo de Cloaking que se establece (si existe). La ocultación no es compatible con el proveedor de seguridad Schannel.

En los temas siguientes se proporciona más información acerca de la ocultación:

-   [Tipos de Cloaking](#types-of-cloaking)
-   [Cómo afecta la ocultación a la identidad del cliente](#how-cloaking-affects-client-identity)
-   [Establecer Cloaking](#setting-cloaking)
-   [Ocultación y niveles de suplantación](#cloaking-and-impersonation-levels)
-   [Escenarios de ocultación](#cloaking-scenarios)
-   [Temas relacionados](#related-topics)

## <a name="types-of-cloaking"></a>Tipos de Cloaking

Hay dos tipos de Cloaking: ocultación *estática* y ocultación *dinámica* :

-   Con el Cloaking estático (EOAC \_ static \_ Cloaking), el servidor Ve el token de subproceso de la primera llamada de un cliente al servidor. En la primera llamada, si la identidad del proxy se estableció previamente durante una llamada a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket), se utiliza esa identidad del proxy. Sin embargo, si la identidad del proxy no se estableció previamente, se utiliza el token de subproceso. Si no hay ningún token de subproceso, se utiliza el token de proceso. Para todas las llamadas futuras, se usa la identidad establecida en la primera llamada.
-   Con el Cloaking dinámico (EOAC \_ Dynamic \_ Cloaking), se usa en cada llamada el token del subproceso actual (si hay un token de subproceso) para determinar la identidad del cliente. Si no hay ningún token de subproceso, se utiliza el token de proceso. Esto significa que los servidores a los que se llama en nombre del cliente durante la suplantación ven la identidad del cliente COM que originó la llamada, que suele ser el comportamiento deseado. (Por supuesto, para que la suplantación se realice correctamente, el cliente debe haber proporcionado la entidad de servidor para suplantar mediante el establecimiento de un nivel de suplantación adecuado. Para obtener más información, vea [niveles de suplantación](impersonation-levels.md)). Este tipo de Cloaking es caro.

## <a name="how-cloaking-affects-client-identity"></a>Cómo afecta la ocultación a la identidad del cliente

Cuando se realiza una llamada cifrada y el servidor pide su identidad al cliente, normalmente obtiene la identidad asociada al proxy. (A veces, el servicio de autenticación realiza una traducción de la identidad real, pero generalmente la identidad del proxy es la identidad que el servidor ve). El proxy presenta una identidad al servidor que depende del tipo de Cloaking que se establece y de otros factores.

En Resumen, la identidad del cliente es una función del conjunto de marcas de ocultación, el token de proceso, la presencia o ausencia de un token de subproceso, y si la identidad del proxy se ha establecido previamente. En la tabla siguiente se muestra la identidad del proxy resultante (identidad del cliente) cuando estos factores varían.



| Ocultar marcas                     | Presencia de token de subproceso  | Identidad de proxy previamente establecida | Identidad del proxy (identidad del cliente)                    |
|------------------------------------|------------------------|-------------------------------|-----------------------------------------------------|
| Cloaking no establecido<br/>        | No importa<br/>  | No importa<br/>         | Identidad de autenticación o token de proceso<br/> |
| EOAC \_ estático de \_ Cloaking<br/>  | Presente<br/>     | No<br/>                 | Token de subproceso<br/>                             |
| EOAC \_ estático de \_ Cloaking<br/>  | Presente<br/>     | Sí<br/>                | Identidad del proxy actual<br/>                   |
| EOAC \_ estático de \_ Cloaking<br/>  | No está presente<br/> | No<br/>                 | Token de proceso<br/>                            |
| EOAC \_ estático de \_ Cloaking<br/>  | No está presente<br/> | Sí<br/>                | Identidad del proxy actual<br/>                   |
| \_Cloaking dinámico de EOAC \_<br/> | Presente<br/>     | No importa<br/>         | Token de subproceso<br/>                             |
| \_Cloaking dinámico de EOAC \_<br/> | No está presente<br/> | No importa <br/>        | Token de proceso<br/>                            |



 

En el diagrama de flujo siguiente se muestra cómo se determina la identidad del proxy en diferentes situaciones.

![Diagrama que muestra el flujo para determinar la identidad del proxy.](images/9e8409b7-8475-4824-bdff-cf6b09c139c5.png)

## <a name="setting-cloaking"></a>Establecer Cloaking

La ocultación se establece como una marca de capacidad en una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), que establece la ocultación para todo el proceso. A continuación, se establece la capacidad de Cloaking hasta que el cliente la cambia a través de una llamada a IClientSecurity::[**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) (o a [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)), que establece la ocultación del proxy.

De forma predeterminada, no se establece la ocultación. Para establecerlo, pase EOAC \_ static \_ CLOAKING o EOAC \_ Dynamic \_ Cloaking al parámetro *pCapabilities* de [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket).

Cuando se habilita el Cloaking estático mediante [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity), cada proxy toma un token (subproceso o proceso) la primera vez que realiza una llamada en el proxy. Cuando se habilita el Cloaking estático mediante [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket), el proxy recoge el token en el subproceso en ese momento. Si no hay ningún token de subproceso disponible cuando se llama a **SetBlanket** , el token de proceso se usa para la identidad del proxy. Básicamente, **SetBlanket** corrige la identidad del proxy.

Con el Cloaking dinámico, la identidad del proxy se determina de la misma manera independientemente de si el Cloaking dinámico se establece mediante [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o con [**SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket). El token de subproceso actual se utiliza si hay alguno; de lo contrario, se utiliza el token de proceso.

Si se establece la ocultación para todo el proceso a través de una llamada a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y desea realizar llamadas con el token de proceso, no suplantar mientras realiza llamadas.

## <a name="cloaking-and-impersonation-levels"></a>Ocultación y niveles de suplantación

Como se mencionó anteriormente, la funcionalidad de ocultación determina qué identidad se presenta a un servidor durante la suplantación. La ocultación proporciona una forma para que un servidor pueda proyectar una identidad que no sea la suya propia en otro servidor al que llama en nombre del cliente. El nivel de suplantación indica cuánta autoridad ha proporcionado el cliente al servidor.

La suplantación sin Cloaking funciona, pero puede que no sea la mejor opción porque, en algunos casos, el servidor final debe conocer la identidad del autor de la llamada inicial. Esto no se puede lograr sin usar la ocultación, ya que es difícil asegurarse de que solo los clientes autorizados puedan tener acceso a un equipo remoto. Cuando la suplantación se utiliza sin Cloaking, la identidad presentada a un servidor de nivel inferior es la del proceso de llamada inmediata.

Sin embargo, el Cloaking no resulta útil sin la suplantación. La ocultación solo tiene sentido cuando el cliente ha establecido un nivel de suplantación de Impersonate o Delegate. (Con niveles de suplantación inferiores, el servidor no puede realizar llamadas escondidas). El hecho de que la ocultación sea correcta depende del número de límites de equipo cruzados y en el nivel de suplantación, lo que indica cuánta autoridad debe actuar el servidor en nombre del cliente.

En algunas situaciones, tiene sentido que el servidor establezca la ocultación cuando el cliente establece el nivel de suplantación en la \_ \_ suplantación de nivel Imp de RPC C \_ \_ . Sin embargo, hay algunas limitaciones en vigor. Si el cliente original establece el nivel de suplantación en \_ el \_ nivel Imp de RPC C \_ \_ , el servidor intermedio (que actúa como cliente en el mismo equipo) puede esconder solo en un límite de equipo. Esto se debe a que un token de suplantación de nivel de suplantación solo se puede pasar a través de un límite de equipo. Una vez que se ha cruzado el límite del equipo, solo se puede tener acceso a los recursos locales. La identidad presentada al servidor depende del tipo de Cloaking que se establece. Si no se establece ningún Cloaking, la identidad presentada a un servidor será la del proceso que realiza la llamada inmediata.

Para esconder varios límites de equipo, debe especificar tanto una marca de capacidad de ocultación adecuada como la suplantación de nivel de delegado. Con este tipo de suplantación, las credenciales locales y de red del cliente se asignan al servidor, por lo que el token de suplantación puede cruzar cualquier número de límites del equipo. De nuevo, la identidad presentada al servidor depende del tipo de Cloaking que se establece. Si no se establece ningún Cloaking con la suplantación de nivel de delegado, la identidad presentada a un servidor es la del proceso que realiza la llamada.

Por ejemplo, supongamos que el proceso A llama a B y B llama a C. B ha establecido el Cloaking y un ha establecido el nivel de suplantación en Impersonate. Si A, B y C están en el mismo equipo, pasando el token de suplantación de a a B y después a C funcionará. Pero si A y C están en el mismo equipo y B no lo es, pasar el token funcionará entre A y B, pero no de B a C. Se producirá un error en la llamada de B a C porque B no puede llamar a C mientras se oculta. Sin embargo, si un establece el nivel de suplantación en Delegate, el token se puede pasar de B a C y la llamada puede realizarse correctamente.

## <a name="cloaking-scenarios"></a>Escenarios de ocultación

En la ilustración siguiente, el proceso A llama a B, llama a C, llama a D cuando no se establece la ocultación. Como resultado, cada proceso intermedio ve la identidad del proceso que lo llamó.

![Diagrama que muestra el proceso cuando no se establece la ocultación.](images/0d2eb6cf-97d6-4c4e-b97e-abad854b1120.png)

Con el Cloaking estático, el servidor ve la identidad del proxy que se estableció durante la primera llamada desde el cliente al servidor. En la siguiente ilustración se muestra un ejemplo de la identidad del proxy que se establece durante una llamada de B a C. En una llamada posterior, el proceso D ve la identidad de B cuando la ocultación estática está establecida por B y C.

![Diagrama que muestra el proceso de Cloaking estático.](images/520938e0-c4a6-4ac1-937d-02baf2007a27.png)

Con el Cloaking dinámico, la identidad del autor de la llamada durante la suplantación se basa en el token del subproceso actual, si hay alguno. En la ilustración siguiente se muestra la situación en la que B y C establecen la ocultación dinámica y D ven la identidad de un, a pesar de una llamada anterior de B a C.

![Diagrama que muestra el proceso de Cloaking dinámico.](images/d0848465-82f3-4d5a-851e-566d7800ada0.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Delegación y suplantación](delegation-and-impersonation.md)
</dt> </dl>

 

