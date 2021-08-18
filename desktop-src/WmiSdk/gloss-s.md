---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 223cfe51-8b1d-4965-b7b1-acc3cd5619f0
ms.tgt_platform: multiple
title: S (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7089d3b4e7714b84dc02f6491da1c0a8d21d1b83c1729ac9fe04824c83a6789e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993195"
---
# <a name="s-wmi"></a>S (WMI)

[A](gloss-a.md) B [C](gloss-c.md) [D](gloss-d.md) [E](gloss-e.md) [F](gloss-f.md) G H [](gloss-h.md) [I](gloss-i.md) J [K](gloss-k.md) [L](gloss-l.md) M [N](gloss-m.md) [O](gloss-n.md) [](gloss-o.md) [P](gloss-p.md) [Q](gloss-q.md) [R](gloss-r.md) S [T](gloss-t.md) U V [W](gloss-w.md) X Y Z

<dl> <dt>

<span id="wmi.gloss_schema"></span><span id="WMI.GLOSS_SCHEMA"></span>**Esquema**
</dt> <dd>

Colección de definiciones de clase que describen [*objetos administrados*](gloss-m.md) en un entorno específico.

</dd> <dt>

<span id="wmi.gloss_security_descriptor"></span><span id="WMI.GLOSS_SECURITY_DESCRIPTOR"></span>**descriptor de seguridad**
</dt> <dd>

Estructura de datos que contiene la información de seguridad de un objeto protegible, como un recurso compartido, un archivo, un receptor o un filtro de eventos.

</dd> <dt>

<span id="wmi.gloss_security_identifier"></span><span id="WMI.GLOSS_SECURITY_IDENTIFIER"></span>**identificador de seguridad (SID)**
</dt> <dd>

Estructura de datos que identifica cuentas de usuario, grupo y equipo.

</dd> <dt>

<span id="wmi.gloss_semi_synchronous"></span><span id="WMI.GLOSS_SEMI_SYNCHRONOUS"></span>**semi sincrónico**
</dt> <dd>

Vea *el método semisincronoso*.

</dd> <dt>

<span id="wmi.gloss_semi__synchronous"></span><span id="WMI.GLOSS_SEMI__SYNCHRONOUS"></span>**semi sincrónico**
</dt> <dd>

Vea *el método semisincronoso*.

</dd> <dt>

<span id="wmi.gloss_semisynchronous"></span><span id="WMI.GLOSS_SEMISYNCHRONOUS"></span>**método semisincronoso**
</dt> <dd>

Llamada al método que devuelve inmediatamente y permite que la aplicación o el script enumeren los objetos devueltos como una colección.

</dd> <dt>

<span id="gloss_servicesid"></span><span id="GLOSS_SERVICESID"></span>**SID de servicio**
</dt> <dd>

Un *SID único que* se crea para cada contexto de seguridad; es decir, uno para "LocalService" y otro para "NetworkService". Solo el *SID de servicio* tiene permisos para los recursos, como subprocesos y eventos, creados por el proceso de host del proveedor WMI (wmiprvse.exe).

</dd> <dt>

<span id="wmi.gloss_sid"></span><span id="WMI.GLOSS_SID"></span>**Sid**
</dt> <dd>

Vea identificador *de seguridad*.

</dd> <dt>

<span id="wmi.gloss_singleton_class"></span><span id="WMI.GLOSS_SINGLETON_CLASS"></span>**singleton (clase)**
</dt> <dd>

Clase WMI que admite una sola instancia.

</dd> <dt>

<span id="wmi.gloss_sink"></span><span id="WMI.GLOSS_SINK"></span>**Fregadero**
</dt> <dd>

Objeto COM que actúa como destino de entrega física para los resultados de una operación asincrónica o una notificación de eventos. Un receptor implementado por un [*consumidor permanente*](gloss-p.md) admite la [**interfaz IWbemUnboundObjectSink.**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) Un receptor implementado por un consumidor [*temporal*](gloss-t.md) o aplicaciones que hacen llamadas asincrónicas admite la [**interfaz IWbemObjectSink.**](iwbemobjectsink.md)

Los clientes de scripting pueden usar el objeto [**SWbemSink**](swbemsink.md) y los eventos, como [**OnObjectReady**](swbemsink-onobjectready.md), para recibir devoluciones de llamada resultantes de llamadas asincrónicas.

</dd> <dt>

<span id="wmi.gloss_standard_consumer"></span><span id="WMI.GLOSS_STANDARD_CONSUMER"></span>**consumidor estándar**
</dt> <dd>

Consumidor permanente [](gloss-p.md) preinstalado que realiza una acción, como enviar un mensaje de correo electrónico o escribir en un registro cuando se configura mediante un archivo [*Managed Object Format (MOF)*](gloss-m.md) o un script.

</dd> <dt>

<span id="wmi.gloss_standard_provider"></span><span id="WMI.GLOSS_STANDARD_PROVIDER"></span>**proveedor estándar**
</dt> <dd>

Proveedor [*integrado*](gloss-p.md) en WMI, que es diferente de un proveedor de terceros o personalizado.

</dd> <dt>

<span id="wmi.gloss_standard_qualifier"></span><span id="WMI.GLOSS_STANDARD_QUALIFIER"></span>**calificador estándar**
</dt> <dd>

[*Calificador*](gloss-q.md) que el [*Administrador de objetos CIM*](gloss-c.md) asocia automáticamente a una clase, instancia, propiedad, método o parámetro de un método.

</dd> <dt>

<span id="wmi.gloss_standard_schema"></span><span id="WMI.GLOSS_STANDARD_SCHEMA"></span>**esquema estándar**
</dt> <dd>

Un marco conceptual común que organiza y relaciona las clases que representan el estado operativo actual de un sistema, red o aplicación. El [*Grupo de tareas de administración distribuida (DMTF)*](gloss-d.md) define el esquema estándar en Modelo de información común [*(CIM).*](gloss-c.md)

</dd> <dt>

<span id="wmi.gloss_static_class"></span><span id="WMI.GLOSS_STATIC_CLASS"></span>**static (clase)**
</dt> <dd>

Definición de clase CIM que rara vez cambia y se almacena en el [*repositorio CIM*](gloss-c.md) hasta que se elimina explícitamente. El [*Administrador de objetos CIM*](gloss-c.md) puede proporcionar una definición de una clase estática sin un [*proveedor*](gloss-p.md). Una clase estática puede admitir instancias *estáticas* [*o dinámicas.*](gloss-d.md)

</dd> <dt>

<span id="wmi.gloss_static_instance"></span><span id="WMI.GLOSS_STATIC_INSTANCE"></span>**instancia estática**
</dt> <dd>

Instancia de una clase CIM que se almacena de forma persistente en el repositorio [*CIM*](gloss-c.md) y sigue siendo válida hasta que se elimina explícitamente, incluso entre reinicios del sistema.

</dd> <dt>

<span id="wmi.gloss_static_method"></span><span id="WMI.GLOSS_STATIC_METHOD"></span>**método estático**
</dt> <dd>

Método definido en una clase CIM que se ejecuta recuperando la definición de clase en lugar de recuperar una instancia de la clase .

</dd> <dt>

<span id="wmi.gloss_subschema"></span><span id="WMI.GLOSS_SUBSCHEMA"></span>**subschema**
</dt> <dd>

Parte de un *esquema* que pertenece a una organización específica. [*Win32schema*](gloss-w.md) es un ejemplo de un subesquema.

</dd> <dt>

<span id="wmi.gloss_system_class"></span><span id="WMI.GLOSS_SYSTEM_CLASS"></span>**system (clase)**
</dt> <dd>

Clase que [*el*](gloss-c.md) Administrador de objetos CIM define para admitir características básicas como la notificación de eventos, la seguridad y la localización. Una clase del sistema se define automáticamente en cada espacio de [*nombres*](gloss-n.md). Una clase del sistema se deriva de la clase base abstracta [**\_ \_ SystemClass**](--systemclass.md).

</dd> <dt>

<span id="wmi.gloss_system_monitor"></span><span id="WMI.GLOSS_SYSTEM_MONITOR"></span>**Monitor de sistema**
</dt> <dd>

Una utilidad (CIM) que es la GUI para la supervisión del rendimiento.

</dd> <dt>

<span id="wmi.gloss_system_property"></span><span id="WMI.GLOSS_SYSTEM_PROPERTY"></span>**propiedad del sistema**
</dt> <dd>

Propiedad que [*el*](gloss-c.md) Administrador de objetos CIM define para proporcionar información que se aplica a cada clase, por ejemplo, nombre, derivación y espacio de [*nombres*](gloss-n.md).

</dd> </dl>

 

 



