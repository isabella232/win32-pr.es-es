---
description: El moniker de cola se usa para activar un componente en cola mediante programación.
ms.assetid: d3d22ae6-7d16-4f25-9f15-21b2163cb0f5
title: Uso del Moniker de cola
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938b4c0c8afc19e953d7f62f17f95bbd63f387e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473691"
---
# <a name="using-the-queue-moniker"></a>Uso del Moniker de cola

El moniker de cola se usa para activar un componente en cola mediante programación. El moniker de cola requiere que reciba el identificador de clase (CLSID) del objeto que se va a invocar desde el nuevo moniker directamente a la derecha. Cuando tiene el prefijo a la izquierda, el nuevo moniker pasa el CLSID al moniker a la izquierda.

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

No corresponde.

## <a name="visual-basic"></a>Visual Basic

El parámetro de nombre para mostrar GetObject es "queue:/new:", seguido del identificador de programa o guid de forma de cadena, con o sin llaves, del objeto de servidor del que se va a crear una instancia. En los ejemplos siguientes se muestran tres activaciones válidas de un componente con el moniker de cola:

1.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:QCShip.Ship")
    ```

2.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}")
    ```

3.  ``` syntax
    Set objMyQC = GetObject ("queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE")
    ```

## <a name="cc"></a>C/C++

El parámetro de nombre para mostrar [**CoGetObject**](https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-cogetobject) es "queue:/new:", seguido del identificador de programa o guid de forma de cadena, con o sin llaves, del objeto de servidor del que se va a crear una instancia. En los ejemplos siguientes se muestran tres activaciones válidas de un componente con el moniker de cola:

1.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:QCShip.Ship",
      NULL, IID_IShip, (void**)&pShip);
    ```

2.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:{812DF40E-BD88-11D0-8A6D-00C04FC340EE}", 
      NULL, IID_IShip, (void**)&pShip);
    ```

3.  ``` syntax
    hr = CoGetObject (
      L"queue:/new:812DF40E-BD88-11D0-8A6D-00C04FC340EE",
      NULL, IID_IShip, (void**)&pShip);
    ```

## <a name="remarks"></a>Comentarios

El moniker de cola acepta parámetros opcionales que modifican las propiedades del mensaje enviado a Message Queuing. Por ejemplo, para hacer que el mensaje de Message Queuing se envíe con una prioridad 6, el componente en cola se activaría de la siguiente manera:

``` syntax
hr = CoGetObject (
  L"queue:Priority=6,ComputerName=MyComp/new:QCShip.Ship",
  NULL, IID_IShip, (void**)&pShip);
```

En la tabla siguiente se enumeran los parámetros del moniker de cola que afectan a la cola de destino.




| Parámetro | Descripción | 
|-----------|-------------|
| <em>nombreDeEquipo</em><br /> | Especifica la parte del nombre de equipo de un nombre de ruta de acceso de cola de Message Queuing. El nombre de la ruta de acceso de cola de Message Queuing tiene el formato <em>NombreDeEquipo</em> \<em> QueueName </em> . Si no se especifica, se usa el nombre de equipo asociado a la aplicación configurada.<br /> | 
| <em>QueueName</em><br /> | Especifica el nombre de la cola de Message Queuing. El nombre de la ruta de acceso de cola de Message Queuing tiene el formato <em>NombreDeEquipo</em> \<em> QueueName </em> . Si no se especifica, se usa el nombre de cola asociado a la aplicación configurada.<br /> Para obtener una cola no transaccional, puede especificar primero el nombre de la cola y, a continuación, crear una aplicación COM+ con el mismo nombre.<br /> | 
| <em>PathName</em><br /> | Especifica el nombre completo de la ruta de acceso de la cola de Message Queuing. Si no se especifica, se usa el nombre de la ruta de acceso de cola de Message Queuing asociada a la aplicación configurada. Para invalidar el nombre de destino, la ruta de acceso se puede especificar con el formato siguiente para una instalación de grupo de trabajo de Message Queuing:<br /> Cola:<em>PathName</em> = <em>NombreDeEquipo</em>\PRIVATE$\AppName/new:Myproject.CMyClass<br /><blockquote>[!Note]<br />Los lenguajes de programación C y Microsoft Visual C++ requieren dos barras diagonales inversas para representar una barra diagonal inversa dentro de literales de cadena, por ejemplo, la nómina de \\ Chicago.</blockquote><br /> | 
| <em>FormatName</em><br /> | Al marcar una aplicación COM+ como en cola, COM+ crea una cola de Message Queuing cuyo nombre es el mismo que la aplicación. El nombre de formato de Message Queuing de esa cola está en el catálogo de COM+, asociado a la aplicación COM+. Para invalidar el nombre de destino, el nombre de formato se puede especificar con el formato siguiente para una instalación de grupo de trabajo de Message Queuing:<br /> Cola:<em>FormatName</em>=DIRECT=OS:<em>NombreDeEquipo</em>\PRIVATE$\AppName/new:ProgId<br /> En una configuración Active Directory, no se especifica "PRIVATE$" como parte del nombre de la cola. <br /> | 




 

> [!Note]  
> Los parámetros opcionales del moniker de cola se procesan de izquierda a derecha. Especifique cada palabra clave solo una vez. Al especificar el *parámetro PathName* se reemplazan los parámetros *ComputerName* y *QueueName.* Un parámetro *FormatName* específico elimina los conocimientos previos de un parámetro *ComputerName,* *QueueName* *y PathName.*

 

## <a name="associating-the-queued-components-listener-with-a-specific-private-queue"></a>Asociación del agente de escucha de componentes en cola a una cola privada específica

El agente de escucha de componentes en cola de COM+ solo recibe de las colas asociadas a la aplicación COM+ marcada como en cola. Al marcar una aplicación COM+ como en cola, COM+ crea una cola de Message Queuing cuyo nombre es el mismo que la aplicación. El nombre de formato de Message Queuing de esa cola está en el catálogo de COM+, asociado a la aplicación COM+. Cuando se inicia la aplicación COM+ y se marca como escucha, se inicia un agente de escucha en el proceso de aplicación COM+ y se abre la cola. En la tabla siguiente se enumeran los parámetros del moniker de cola que afectan al mensaje de Message Queuing.




| Parámetro | Descripción | 
|-----------|-------------|
| <em>AppSpecific</em><br /> | Especifica un entero sin signo, por ejemplo, AppSpecific=12345.<br /> | 
| <em>AuthLevel</em><br /> | Especifica el nivel de autenticación del mensaje. Un mensaje autenticado está firmado digitalmente y requiere un certificado para el usuario que envía el mensaje. Valores aceptables:<br /><ul><li>MQMSG_AUTH_LEVEL_NONE,0</li><li>MQMSG_AUTH_LEVEL_ALWAYS,1</li></ul> | 
| <em>Entrega.</em><br /> | Especifica la opción de entrega de mensajes. Este valor se omite para las colas transaccionales. Valores aceptables:<br /><ul><li>MQMSG_DELIVERY_EXPRESS,0</li><li>MQMSG_DELIVERY_RECOVERABLE,1</li></ul> | 
| <em>EncryptAlgorithm</em><br /> | Especifica el algoritmo de cifrado que va a usar Message Queuing para cifrar y descifrar el mensaje. Valores aceptables:<br /><ul><li>CALG_RC2, CALG_RC4</li><li>Cualquier valor entero que sea aceptable para Message Queuing para <em>encryptAlgorithm</em>.</li></ul> | 
| <em>HashAlgorithm</em><br /> | Especifica una función hash criptográfica. Valores aceptables:<br /><ul><li>CALG_MD2, CALG_MD4, CALG_MD5, CALG_SHA, CALG_SHA1, CALG_MAC, CALG_SSL3_SHAMD5, CALG_HMAC, CALG_TLS1PRF</li><li>Cualquier valor entero que sea aceptable para Message Queuing para <em>hashAlgorithm</em>.</li></ul> | 
| Diario<br /> | Especifica la opción de diario de mensajes de Message Queuing. Valores aceptables:<br /><ul><li>MQMSG_JOURNAL_NONE,0</li><li>MQMSG_DEADLETTER,1</li><li>MQMSG_JOURNAL,2</li></ul> | 
| <em>Label</em><br /> | Especifica una cadena de etiqueta de mensaje hasta MQ_MAX_MSG_LABEL_LEN caracteres. <br /> | 
| <em>MaxTimeToReachQueue</em><br /> | Especifica un tiempo máximo, en segundos, para que el mensaje llegue a la cola. <br /> Valores aceptables:<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Número de segundos</li></ul> | 
| <em>MaxTimeToReceive</em><br /> | Especifica un tiempo máximo, en segundos, para que la aplicación de destino reciba el mensaje. Valores aceptables:<br /><ul><li>INFINITE</li><li>LONG_LIVED</li><li>Número de segundos</li></ul> | 
| <em>Prioridad</em><br /> | Especifica un nivel de prioridad de mensaje, dentro de los valores de Message Queuing permitidos.<br /> Valores aceptables:<br /><ul><li>MQ_MIN_PRIORITY,0</li><li>MQ_MAX_PRIORITY,7</li><li>MQ_DEFAULT_PRIORITY,3</li><li>Número entre 0 y 7</li></ul> | 
| <em>PrivLevel</em><br /> | Especifica un nivel de privacidad, que se usa para cifrar los mensajes.<br /> Valores aceptables:<br /><ul><li>MQMSG_PRIV_LEVEL_NONE, NONE, 0</li><li>MQMSG_PRIV_LEVEL_BODY, CUERPO,</li><li>MQMSG_PRIV_LEVEL_BODY_BASE, BODY_BASE, 1</li><li>MQMSG_PRIV_LEVEL_BODY_ENHANCED, BODY_ENHANCED, 3</li></ul> | 
| <em>Seguimiento</em><br /> | Especifica las opciones de seguimiento, que se usan en el seguimiento del enrutamiento de Message Queuing.<br /> Valores aceptables:<br /><ul><li>MQMSG_TRACE_NONE,0</li><li>MQMSG_SEND_ROUTE_TO_REPORT_QUEUE,1</li></ul> | 




 

El conjunto completo de funciones del SDK administrativo de COM+ está disponible mediante objetos COM. Esto permite que cualquier programa inicie y detenga aplicaciones COM+ según sea necesario.

> [!Note]  
> Cuando se inicia una aplicación COM+, es la aplicación que se ejecuta, no los componentes individuales dentro de la aplicación. Si una aplicación llama a un componente que no está en cola, se inicia la aplicación COM+ que contiene el componente. Si la casilla del agente de escucha está habilitada, el agente de escucha también se inicia y comienza a procesar los mensajes de los componentes en cola. Aunque el servicio de componentes en cola se puede iniciar de esta manera, si empaqueta componentes en cola y no en cola en una sola aplicación COM+, asegúrese de que realmente desea que los componentes en cola se inicien si se ejecuta un componente que no está en cola. Si este no es el caso, empaquete los componentes en cola en una aplicación COM+ independiente de los demás componentes.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Activación de colas de componentes](activating-component-queues.md)
</dt> </dl>

 

 




