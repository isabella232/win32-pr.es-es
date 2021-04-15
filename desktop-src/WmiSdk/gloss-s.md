---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 223cfe51-8b1d-4965-b7b1-acc3cd5619f0
ms.tgt_platform: multiple
title: S (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48473c58a1c9aae3f3c9e67f7723167b46df0285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688530"
---
# <a name="s-wmi"></a>S (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G [H](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) [M](gloss-m.md) [N](gloss-n.md) [o](gloss-o.md) [p](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) s [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_schema"></span><span id="WMI.GLOSS_SCHEMA"></span>**esquema**
</dt> <dd>

Colección de definiciones de clase que describen [*objetos administrados*](gloss-m.md) en un entorno específico.

</dd> <dt>

<span id="wmi.gloss_security_descriptor"></span><span id="WMI.GLOSS_SECURITY_DESCRIPTOR"></span>**descriptor de seguridad**
</dt> <dd>

Una estructura de datos que contiene la información de seguridad para un objeto protegible, como un recurso compartido, un archivo, un receptor o un filtro de eventos.

</dd> <dt>

<span id="wmi.gloss_security_identifier"></span><span id="WMI.GLOSS_SECURITY_IDENTIFIER"></span>**identificador de seguridad (SID)**
</dt> <dd>

Una estructura de datos que identifica las cuentas de usuario, de grupo y de equipo.

</dd> <dt>

<span id="wmi.gloss_semi_synchronous"></span><span id="WMI.GLOSS_SEMI_SYNCHRONOUS"></span>**semisincrónico**
</dt> <dd>

Vea *método semisincrónico*.

</dd> <dt>

<span id="wmi.gloss_semi__synchronous"></span><span id="WMI.GLOSS_SEMI__SYNCHRONOUS"></span>**semisincrónico**
</dt> <dd>

Vea *método semisincrónico*.

</dd> <dt>

<span id="wmi.gloss_semisynchronous"></span><span id="WMI.GLOSS_SEMISYNCHRONOUS"></span>**método semisincrónico**
</dt> <dd>

Llamada al método que devuelve inmediatamente y permite a la aplicación o script enumerar los objetos devueltos como una colección.

</dd> <dt>

<span id="gloss_servicesid"></span><span id="GLOSS_SERVICESID"></span>**SID de servicio**
</dt> <dd>

*SID* único que se crea para cada contexto de seguridad; es decir, uno para "LocalService" y otro para "NetworkService". Solo el *SID del servicio* tiene permisos para recursos, como subprocesos y eventos, creados por el proceso de host del proveedor WMI (wmiprvse.exe).

</dd> <dt>

<span id="wmi.gloss_sid"></span><span id="WMI.GLOSS_SID"></span>**Junction**
</dt> <dd>

Consulte *identificador de seguridad*.

</dd> <dt>

<span id="wmi.gloss_singleton_class"></span><span id="WMI.GLOSS_SINGLETON_CLASS"></span>**singleton (clase)**
</dt> <dd>

Una clase WMI que admite una sola instancia.

</dd> <dt>

<span id="wmi.gloss_sink"></span><span id="WMI.GLOSS_SINK"></span>**receptor**
</dt> <dd>

Objeto COM que actúa como destino de entrega física para los resultados de una operación asincrónica o una notificación de eventos. Un receptor implementado por un [*consumidor permanente*](gloss-p.md) es compatible con la interfaz [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . Un receptor implementado por un [*consumidor temporal*](gloss-t.md) o aplicaciones que realizan llamadas asincrónicas admiten la interfaz [**IWbemObjectSink**](iwbemobjectsink.md) .

Los clientes de scripting pueden usar el objeto [**SWbemSink**](swbemsink.md) y los eventos, como [**OnObjectReady**](swbemsink-onobjectready.md), para recibir devoluciones de llamada que resultan de llamadas asincrónicas.

</dd> <dt>

<span id="wmi.gloss_standard_consumer"></span><span id="WMI.GLOSS_STANDARD_CONSUMER"></span>**consumidor estándar**
</dt> <dd>

Los [*consumidores permanentes*](gloss-p.md) preinstalados que realizan una acción, como enviar un mensaje de correo electrónico o escribir en un registro cuando se configuran mediante un archivo [*Managed Object Format (MOF)*](gloss-m.md) o un script.

</dd> <dt>

<span id="wmi.gloss_standard_provider"></span><span id="WMI.GLOSS_STANDARD_PROVIDER"></span>**proveedor estándar**
</dt> <dd>

[*Proveedor*](gloss-p.md) integrado en WMI, que es diferente de un proveedor personalizado o de otro fabricante.

</dd> <dt>

<span id="wmi.gloss_standard_qualifier"></span><span id="WMI.GLOSS_STANDARD_QUALIFIER"></span>**calificador estándar**
</dt> <dd>

[*Calificador*](gloss-q.md) que el [*Administrador de objetos CIM*](gloss-c.md) asocia automáticamente a una clase, instancia, propiedad, método o parámetro de un método.

</dd> <dt>

<span id="wmi.gloss_standard_schema"></span><span id="WMI.GLOSS_STANDARD_SCHEMA"></span>**esquema estándar**
</dt> <dd>

Marco conceptual común que organiza y relaciona las clases que representan el estado operativo actual de un sistema, red o aplicación. El [*equipo de tareas de administración distribuida (DMTF)*](gloss-d.md) define el esquema estándar en el [*modelo de información común (CIM)*](gloss-c.md).

</dd> <dt>

<span id="wmi.gloss_static_class"></span><span id="WMI.GLOSS_STATIC_CLASS"></span>**clase estática**
</dt> <dd>

Una definición de clase CIM que rara vez cambia y se almacena en el [*repositorio CIM*](gloss-c.md) hasta que se elimina explícitamente. El [*Administrador de objetos CIM*](gloss-c.md) puede proporcionar una definición de una clase estática sin un [*proveedor*](gloss-p.md). Una clase estática puede admitir instancias *estáticas* o [*dinámicas*](gloss-d.md).

</dd> <dt>

<span id="wmi.gloss_static_instance"></span><span id="WMI.GLOSS_STATIC_INSTANCE"></span>**instancia estática**
</dt> <dd>

Instancia de una clase CIM que se almacena de forma persistente en el [*repositorio CIM*](gloss-c.md) y sigue siendo válida hasta que se elimina explícitamente, incluso a través de los reinicios del sistema.

</dd> <dt>

<span id="wmi.gloss_static_method"></span><span id="WMI.GLOSS_STATIC_METHOD"></span>**método estático**
</dt> <dd>

Un método definido en una clase CIM que se ejecuta recuperando la definición de clase en lugar de recuperar una instancia de la clase.

</dd> <dt>

<span id="wmi.gloss_subschema"></span><span id="WMI.GLOSS_SUBSCHEMA"></span>**subesquema**
</dt> <dd>

Parte de un *esquema* que pertenece a una organización específica. [*Win32schema*](gloss-w.md) es un ejemplo de subesquema.

</dd> <dt>

<span id="wmi.gloss_system_class"></span><span id="WMI.GLOSS_SYSTEM_CLASS"></span>**System (clase)**
</dt> <dd>

Una clase que define el [*Administrador de objetos CIM*](gloss-c.md) para admitir características principales como la notificación de eventos, la seguridad y la localización. Una clase del sistema se define automáticamente en cada [*espacio de nombres*](gloss-n.md). Una clase del sistema deriva de la clase base abstracta [**\_ \_ SystemClass**](--systemclass.md).

</dd> <dt>

<span id="wmi.gloss_system_monitor"></span><span id="WMI.GLOSS_SYSTEM_MONITOR"></span>**Monitor de sistema**
</dt> <dd>

Una utilidad (CIM) que es la GUI para la supervisión del rendimiento.

</dd> <dt>

<span id="wmi.gloss_system_property"></span><span id="WMI.GLOSS_SYSTEM_PROPERTY"></span>**propiedad del sistema**
</dt> <dd>

Propiedad que define el [*Administrador de objetos CIM*](gloss-c.md) para proporcionar información que se aplica a cada clase, por ejemplo, nombre, derivación y [*espacio de nombres*](gloss-n.md).

</dd> </dl>

 

 



