---
description: Puede usar los métodos de un objeto SWbemServices para realizar operaciones en un espacio de nombres en un host local o en un host remoto. La llamada CreateObject de VBScript no puede crear este objeto.
ms.assetid: 7fcfa404-2fe6-42e5-85ac-64536f6d2a44
ms.tgt_platform: multiple
title: Objeto SWbemServices (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices
- ISWbemServices
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4303b3226acc6d773ed35e77176e05e3a58c567d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465589"
---
# <a name="swbemservices-object"></a>Objeto SWbemServices

Puede usar los métodos de un objeto **SWbemServices** para realizar operaciones en un espacio de nombres en un host local o en un host remoto. La llamada **CreateObject** de VBScript no puede crear este objeto.

## <a name="members"></a>Members

El **objeto SWbemServices** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SWbemServices** tiene estos métodos.



| Método                                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociatorsOf**](swbemservices-associatorsof.md)                           | Recupera las instancias de recursos administrados que están asociados a un recurso especificado a través de una o varias clases de asociación. Proporcione la ruta de acceso del objeto para el punto de conexión de origen y [**AssociatorsOf**](swbemservices-associatorsof.md) devuelve los recursos administrados en el extremo opuesto. El **método AssociatorsOf** realiza la misma función que la consulta WQL "ASSOCIATORS OF".<br/>                                                                           |
| [**AssociatorsOfAsync**](swbemservices-associatorsofasync.md)                 | Devuelve de forma asincrónica una colección de objetos (clases o instancias) que están asociados a un objeto especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**Eliminar**](swbemservices-delete.md)                                         | Elimina una instancia de un recurso administrado (o una definición de clase del repositorio CIM).<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**DeleteAsync**](swbemservices-deleteasync.md)                               | Elimina de forma asincrónica la clase o instancia que se especifica en la ruta de acceso del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecMethod**](swbemservices-execmethod.md)                                 | Proporciona una manera alternativa de ejecutar un método definido por una definición de clase de recurso administrada. Se usa principalmente en situaciones en las que el lenguaje de scripting no admite parámetros out. Por ejemplo, JScript no admite parámetros out.<br/>                                                                                                                                                                                                                                            |
| [**ExecMethodAsync**](swbemservices-execmethodasync.md)                       | Ejecuta de forma asincrónica un método exportado por un proveedor de métodos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)           | Ejecuta una consulta de suscripción de eventos para recibir eventos. Una consulta de suscripción de eventos es una consulta que define un cambio en el entorno administrado que desea supervisar. Cuando se produce el cambio, la infraestructura WMI entrega un evento que describe el cambio en el script de llamada.<br/>                                                                                                                                                                                                        |
| [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) | Ejecuta de forma asincrónica una consulta para recibir eventos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecQuery**](swbemservices-execquery.md)                                   | Ejecuta una consulta para recuperar una colección de instancias de recursos administrados por WMI (o definiciones de clase). [**ExecQuery**](swbemservices-execquery.md) se puede usar para recuperar una colección filtrada de instancias que coinciden con los criterios definidos en la consulta que se pasa a **ExecQuery.**<br/>                                                                                                                                                                                                           |
| [**ExecQueryAsync**](swbemservices-execqueryasync.md)                         | Ejecuta de forma asincrónica una consulta para recuperar objetos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtener**](swbemservices-get.md)                                               | Recupera una única instancia de un recurso administrado (o definición de clase) basada en una ruta de acceso de objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Getasync**](swbemservices-getasync.md)                                     | Recupera de forma asincrónica un objeto , que es una definición de clase o una instancia de , basándose en la ruta de acceso del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**InstancesOf**](swbemservices-instancesof.md)                               | Recupera todas las instancias de un recurso administrado en función de un nombre de clase. De forma predeterminada, [**InstancesOf**](swbemservices-instancesof.md) realiza una recuperación en profundidad. Es decir, **InstancesOf** recupera las instancias del recurso identificado por el nombre de clase pasado al método y también recupera todas las instancias de todos los recursos que son subclases (definidas debajo) de la clase de destino.<br/>                                                                                       |
| [**InstancesOfAsync**](swbemservices-instancesofasync.md)                     | Devuelve de forma asincrónica las instancias de una clase especificada según los criterios de selección especificados por el usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**ReferencesTo**](swbemservices-referencesto.md)                             | Devuelve todas las asociaciones que hacen referencia a un recurso especificado. La mejor manera de entender [**ReferencesTo**](swbemservices-referencesto.md) es compararlo con el [**método AssociatorsOf.**](swbemservices-associatorsof.md) **AssociatorsOf** devuelve los recursos dinámicos que se encuentran en el extremo opuesto de una asociación. **ReferencesTo** devuelve la propia asociación. El **método ReferencesTo** realiza la misma función que la consulta WQL "REFERENCES OF".<br/> |
| [**ReferencesToAsync**](swbemservices-referencesto.md)                        | Devuelve de forma asincrónica una colección de todas las clases o instancias de asociación que hacen referencia a una clase o instancia específica.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**SubclassesOf**](swbemservices-subclassesof.md)                             | Recupera todas las subclases de una clase especificada del repositorio CIM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SubclassesOfAsync**](swbemservices-subclassesofasync.md)                   | Devuelve de forma asincrónica una colección de subclases para una clase especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

### <a name="properties"></a>Propiedades

El **objeto SWbemServices** tiene estas propiedades.



| Propiedad                                                 | Tipo de acceso          | Descripción                                                                          |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------|
| [**Seguridad\_**](swbemservices-security-.md)<br/> | Solo lectura<br/> | Se usa para obtener o establecer la configuración de seguridad de **un objeto SWbemServices.**<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede llamar a los métodos en modo sincrónico, modo asincrónico o modo semisincronoso. Para obtener más información, [vea Llamar a un método](calling-a-method.md).

**Información general**

**SWbemServices tiene** dos roles principales. En primer lugar, **el objeto SWbemServices** representa una conexión autenticada a un espacio de nombres WMI en un equipo de destino. En segundo **lugar, SWbemServices** es el objeto de Automation que se usa para recuperar recursos administrados por WMI. Puede obtener una referencia a un **objeto SWbemServices** de cualquiera de estas dos maneras:

-   Como se muestra en la mayoría de los scripts WMI presentados hasta ahora, puede usar la función [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) de VBScript en combinación con el moniker WMI "winmgmts:". El ejemplo siguiente es la forma más sencilla de una conexión WMI. El ejemplo se conecta al espacio de nombres predeterminado (normalmente \\ "ROOT CIMv2") en el equipo local:

    `Set objSWbemServices = GetObject("winmgmts:")`

-   También puede usar el método [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) del objeto [**SWbemLocator**](swbemlocator.md) para obtener una referencia a un **objeto SWbemServices.**

Después de obtener una referencia a un objeto **SWbemServices,** use la referencia de objeto para llamar a 1 de los 18 métodos disponibles mediante **SWbemServices**. **SWbemServices** puede devolver uno de los tres objetos de biblioteca de scripting wmi diferentes [**(SWbemObjectSet,**](swbemobjectset.md) [**SWbemObject**](swbemobject.md)o [**SWbemEventSource),**](swbemeventsource.md)en función del método al que llame. Conocer el tipo de objeto que devuelve cada método le ayudará a determinar el siguiente paso que debe realizar el script. Por ejemplo, si obtiene un **SWbemObjectSet**, debe enumerar la colección para tener acceso a cada **SWbemObject** de la colección. Si obtiene un **objeto SWbemObject**, puede acceder inmediatamente a los métodos y propiedades del objeto sin enumerar primero la colección.

**Modos de funcionamiento**

**SWbemServices admite** tres modos de funcionamiento: sincrónico, asincrónico y semisincronoso.

-   **Synchronous**. En modo sincrónico, el script se bloquea (se pausa) hasta que se completa el método **SWbemServices.** No solo espera el script, sino que, en los casos en los que WMI recupera instancias de recursos administrados, WMI compila todo [**SWbemObjectSet**](swbemobjectset.md) en memoria antes de que el primer byte de datos se devuelva al script de llamada. Esto puede tener un efecto adverso en el rendimiento del script y en el equipo que ejecuta el script. Por ejemplo, recuperar sincrónicamente miles de eventos de Windows registros de eventos puede tardar mucho tiempo y usar mucha memoria. Por estos motivos, no se recomiendan operaciones sincrónicas excepto para los tres métodos [**(Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md)y [**Get)**](swbemservices-get.md)que son sincrónicos de forma predeterminada. Estos métodos no devuelven grandes conjuntos de datos, por lo que no se requiere una operación semisincronosa.
-   **Asincrónica** En modo asincrónico, el script llama a uno de los nueve métodos asincrónicos y devuelve inmediatamente. Es decir, en cuanto se llama al método asincrónico, el script reanuda la ejecución de la siguiente línea de código. Para usar un método asincrónico, el script debe crear primero un objeto [**SWbemSink**](swbemsink.md) y una subrutina especial denominada controlador de eventos. WMI realiza la operación asincrónica y notifica al script mediante una llamada a la subrutina del controlador de eventos cuando se completa la operación.
-   **Semisynchronous**. El modo semisincronoso es un riesgo entre sincrónico y asincrónico. Las operaciones semisincronosas ofrecen un mejor rendimiento que las operaciones sincrónicas, pero no requieren los pasos de scripting y conocimientos adicionales necesarios para controlar las operaciones asincrónicas. Este es el tipo de operación predeterminado para la mayoría de las consultas WMI.

    En modo semisincronoso, el script llama a uno de los seis métodos de recuperación de datos y devuelve inmediatamente. WMI recupera los recursos administrados en segundo plano a medida que el script continúa en ejecución. A medida que se recuperan los recursos, se devuelven inmediatamente al script mediante un SWbemObjectSet. Puede empezar a acceder a los recursos administrados sin tener que esperar a que se monte toda la colección.

    Hay una advertencia a las operaciones semisincronosas cuando se trabaja con recursos administrados que tienen muchas instancias (muchos significados mayores que 1000), como [**CIM \_ DataFile**](/windows/desktop/CIMWin32Prov/cim-datafile) y [**Win32 \_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent). La advertencia es el resultado de cómo WMI controla las instancias de recursos administrados. Para cada instancia de un recurso administrado, WMI crea y almacena en caché un [**objeto SWbemObject.**](swbemobject.md) Cuando existe un gran número de instancias para un recurso administrado, la recuperación de instancias puede acodizar los recursos disponibles, lo que reduce el rendimiento del script y del equipo.

    Para solucionar el problema, puede optimizar las llamadas a métodos semisincronosos mediante la **marca wbemFlagForwardOnly.** La **marca wbemFlagForwardOnly,** combinada con la marca **wbemFlagReturnImmediately** (la marca semisincronosa predeterminada), indica a WMI que devuelva un [**SWbemObjectSet**](swbemobjectset.md)de solo avance, lo que elimina el problema de rendimiento del conjunto de datos grande. Sin embargo, el **uso de la marca wbemFlagForwardOnly** tiene un costo. Un **SWbemObjectSet** de solo avance se puede enumerar una sola vez. Una vez que se tiene acceso a cada [**SWbemObject**](swbemobject.md) de un **SWbemObjectSet** de solo avance, se libera la memoria asignada a la instancia.

A excepción de los métodos [**asincrónicos Delete**](swbemservices-delete.md), [**ExecMethod,**](swbemservices-execmethod.md) [**Get**](swbemservices-get.md)y nine, semisynchronous es el modo de operación predeterminado y recomendado.

**Métodos de uso frecuente**

Los métodos que se usan con más frecuencia en los scripts de administración del sistema [**son InstancesOf**](swbemservices-instancesof.md), [**ExecQuery,**](swbemservices-execquery.md) [**Get**](swbemservices-get.md)y [**ExecNotificationQuery.**](swbemservices-execnotificationquery.md) Aunque se usa a menudo, **InstancesOf** no es necesariamente la manera recomendada de recuperar información (aunque es posible que sea la manera más fácil).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Objetos de API de scripting](scripting-api-objects.md)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

