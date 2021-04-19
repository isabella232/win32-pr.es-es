---
description: Puede usar los métodos de un objeto SWbemServices para realizar operaciones en un espacio de nombres en un host local o en un host remoto. Este objeto no se puede crear mediante la llamada CreateObject de VBScript.
ms.assetid: 7fcfa404-2fe6-42e5-85ac-64536f6d2a44
ms.tgt_platform: multiple
title: Objeto SWbemServices (Wbemdisp. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715713"
---
# <a name="swbemservices-object"></a>Objeto SWbemServices

Puede usar los métodos de un objeto **SWbemServices** para realizar operaciones en un espacio de nombres en un host local o en un host remoto. Este objeto no se puede crear mediante la llamada **CreateObject** de VBScript.

## <a name="members"></a>Miembros

El objeto **SWbemServices** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SWbemServices** tiene estos métodos.



| Método                                                                         | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssociatorsOf**](swbemservices-associatorsof.md)                           | Recupera las instancias de recursos administrados que están asociadas a un recurso especificado a través de una o varias clases de asociación. Proporcione la ruta de acceso del objeto para el punto de conexión de origen y [**AssociatorsOf**](swbemservices-associatorsof.md) devuelve los recursos administrados en el extremo opuesto. El método **AssociatorsOf** realiza la misma función que realiza la consulta WQL "ASSOCIATORS of".<br/>                                                                           |
| [**AssociatorsOfAsync**](swbemservices-associatorsofasync.md)                 | Devuelve de forma asincrónica una colección de objetos (clases o instancias) que están asociados a un objeto especificado.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| [**Elimínelos**](swbemservices-delete.md)                                         | Elimina una instancia de un recurso administrado (o una definición de clase del repositorio CIM).<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**DeleteAsync**](swbemservices-deleteasync.md)                               | Elimina de forma asincrónica la clase o instancia que se especifica en la ruta de acceso del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecMethod**](swbemservices-execmethod.md)                                 | Proporciona una manera alternativa de ejecutar un método definido por una definición de clase de recurso administrada. Se utiliza principalmente en situaciones en las que el lenguaje de scripting no admite parámetros de salida. Por ejemplo, JScript no admite parámetros de salida.<br/>                                                                                                                                                                                                                                            |
| [**ExecMethodAsync**](swbemservices-execmethodasync.md)                       | Ejecuta de forma asincrónica un método exportado por un proveedor de métodos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**ExecNotificationQuery**](swbemservices-execnotificationquery.md)           | Ejecuta una consulta de suscripción de eventos para recibir eventos. Una consulta de suscripción de eventos es una consulta que define un cambio en el entorno administrado que desea supervisar. Cuando se produce el cambio, la infraestructura de WMI proporciona un evento que describe el cambio en el script de llamada.<br/>                                                                                                                                                                                                        |
| [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md) | Ejecuta de forma asincrónica una consulta para recibir eventos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**ExecQuery**](swbemservices-execquery.md)                                   | Ejecuta una consulta para recuperar una colección de instancias de recursos administrados por WMI (o definiciones de clase). [**ExecQuery**](swbemservices-execquery.md) se puede usar para recuperar una colección filtrada de instancias que coinciden con los criterios definidos en la consulta que se pasa a **ExecQuery**.<br/>                                                                                                                                                                                                           |
| [**ExecQueryAsync**](swbemservices-execqueryasync.md)                         | Ejecuta de forma asincrónica una consulta para recuperar objetos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**Obtener**](swbemservices-get.md)                                               | Recupera una única instancia de un recurso administrado (o una definición de clase) basándose en una ruta de acceso del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| [**GetAsync**](swbemservices-getasync.md)                                     | Recupera de forma asincrónica un objeto, que es una definición de clase o una instancia de, en función de la ruta de acceso del objeto.<br/>                                                                                                                                                                                                                                                                                                                                                                                |
| [**Instancias**](swbemservices-instancesof.md)                               | Recupera todas las instancias de un recurso administrado basado en un nombre de clase. De forma predeterminada, [**las instancias**](swbemservices-instancesof.md) realizan una recuperación en profundidad. Es decir, **las instancias** recuperan las instancias del recurso identificado por el nombre de clase pasado al método y también recupera todas las instancias de todos los recursos que son subclases (definidos debajo) de la clase de destino.<br/>                                                                                       |
| [**InstancesOfAsync**](swbemservices-instancesofasync.md)                     | Devuelve de forma asincrónica las instancias de una clase especificada de acuerdo con los criterios de selección especificados por el usuario.<br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Referencias a**](swbemservices-referencesto.md)                             | Devuelve todas las asociaciones que hacen referencia a un recurso especificado. La mejor manera de comprender [**referenceto**](swbemservices-referencesto.md) es compararlo con el método [**AssociatorsOf**](swbemservices-associatorsof.md) . **AssociatorsOf** devuelve los recursos dinámicos que están en el extremo opuesto de una asociación. **Referenceas** devuelve la propia asociación. El método **referenceto** realiza la misma función que realiza la consulta WQL "References of".<br/> |
| [**ReferencesToAsync**](swbemservices-referencesto.md)                        | Devuelve de forma asincrónica una colección de todas las clases o instancias de asociación que hacen referencia a una clase o instancia específica.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| [**Subclases**](swbemservices-subclassesof.md)                             | Recupera todas las subclases de una clase especificada del repositorio CIM.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SubclassesOfAsync**](swbemservices-subclassesofasync.md)                   | Devuelve de forma asincrónica una colección de subclases para una clase especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                       |



 

### <a name="properties"></a>Propiedades

El objeto **SWbemServices** tiene estas propiedades.



| Propiedad                                                 | Tipo de acceso          | Descripción                                                                          |
|:---------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------|
| [**Seguridad\_**](swbemservices-security-.md)<br/> | Solo lectura<br/> | Se usa para obtener o establecer la configuración de seguridad para un objeto **SWbemServices** .<br/> |



 

## <a name="remarks"></a>Observaciones

Se puede llamar a los métodos en el modo sincrónico, el modo asincrónico o el modo semisincrónico. Para obtener más información, consulte [llamar a un método](calling-a-method.md).

**Información general**

**SWbemServices** atiende dos roles principales. En primer lugar, el objeto **SWbemServices** representa una conexión autenticada a un espacio de nombres WMI en un equipo de destino. En segundo lugar, **SWbemServices** es el objeto de automatización que se usa para recuperar los recursos administrados por WMI. Puede obtener una referencia a un objeto **SWbemServices** de cualquiera de estas dos maneras:

-   Tal y como se muestra en la mayoría de los scripts de WMI presentados hasta ahora, puede usar la función [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx) de VBScript en combinación con el moniker de WMI "winmgmts:". El ejemplo siguiente es la forma más sencilla de una conexión WMI. En el ejemplo se conecta al espacio de nombres predeterminado (normalmente, "root \\ CIMv2") en el equipo local:

    `Set objSWbemServices = GetObject("winmgmts:")`

-   También puede usar el método [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) del objeto [**SWbemLocator**](swbemlocator.md) para obtener una referencia a un objeto **SWbemServices** .

Después de obtener una referencia a un objeto **SWbemServices** , use la referencia de objeto para llamar a 1 de 18 métodos disponibles mediante **SWbemServices**. **SWbemServices** puede devolver uno de los tres objetos diferentes de la biblioteca de scripting de WMI ([**SWbemObjectSet**](swbemobjectset.md), [**SWbemObject**](swbemobject.md)o [**SWbemEventSource**](swbemeventsource.md)), dependiendo del método al que llame. Conocer el tipo de objeto que devuelve cada método le ayudará a determinar el paso siguiente que debe realizar el script. Por ejemplo, si obtiene una **SWbemObjectSet**, debe enumerar la colección para tener acceso a cada **SWbemObject** de la colección. Si obtiene una **SWbemObject**, puede acceder inmediatamente a los métodos y propiedades del objeto sin tener que enumerar primero la colección.

**Modos de funcionamiento**

**SWbemServices** admite tres modos de funcionamiento: sincrónico, asincrónico y semisincrónico.

-   **Sincrónicos**. En el modo sincrónico, el script se bloquea (pausa) hasta que se completa el método **SWbemServices** . No solo espera la secuencia de comandos, sino que en los casos en los que WMI recupera instancias de recursos administrados, WMI crea el [**SWbemObjectSet**](swbemobjectset.md) completo en memoria antes de que el primer byte de datos se devuelva al script de llamada. Esto puede tener un efecto adverso en el rendimiento del script y en el equipo que ejecuta el script. Por ejemplo, la recuperación sincrónica de miles de eventos de los registros de eventos de Windows puede tardar mucho tiempo y usar una gran cantidad de memoria. Por estas razones, no se recomiendan las operaciones sincrónicas, salvo por los tres métodos ([**Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md)y [**Get**](swbemservices-get.md)) que son sincrónicos de forma predeterminada. Estos métodos no devuelven grandes conjuntos de datos, por lo que no se requiere la operación semisincrónica.
-   **Asincrónica**. En el modo asincrónico, el script llama a uno de los nueve métodos asincrónicos y vuelve inmediatamente. Es decir, en cuanto se llama al método asincrónico, el script reanuda la ejecución de la siguiente línea de código. Para usar un método asincrónico, el script debe crear primero un objeto [**SWbemSink**](swbemsink.md) y una subrutina especial llamada controlador de eventos. WMI realiza la operación asincrónica y notifica al script mediante una llamada a la subrutina del controlador de eventos cuando se completa la operación.
-   **Semisincrónico**. El modo semisincrónico es un riesgo entre el sincrónico y el asincrónico. Las operaciones semisincrónicas ofrecen un mejor rendimiento que las operaciones sincrónicas, pero no requieren los pasos adicionales de scripting y de conocimientos necesarios para controlar las operaciones asincrónicas. Este es el tipo de operación predeterminado para la mayoría de las consultas de WMI.

    En el modo semisincrónico, el script llama a uno de los seis métodos de recuperación de datos y vuelve inmediatamente. WMI recupera los recursos administrados en segundo plano a medida que el script continúa ejecutándose. A medida que se recuperan los recursos, se devuelven inmediatamente al script por medio de un SWbemObjectSet. Puede empezar a acceder a los recursos administrados sin esperar a que se Ensamble la colección completa.

    Hay una advertencia respecto a las operaciones semisincrónicas cuando se trabaja con recursos administrados que tienen muchas instancias (muchos significados mayores que 1.000), [**como \_ archivo**](/windows/desktop/CIMWin32Prov/cim-datafile) de [**\_ NTLogEvent**](/previous-versions/windows/desktop/eventlogprov/win32-ntlogevent)de CIM y Win32. La advertencia es el resultado de la forma en que WMI controla las instancias de recursos administrados. Para cada instancia de un recurso administrado, WMI crea y almacena en caché un objeto [**SWbemObject**](swbemobject.md) . Cuando hay un gran número de instancias para un recurso administrado, la recuperación de la instancia puede monopolizar los recursos disponibles, lo que reduce el rendimiento del script y del equipo.

    Para solucionar el problema, puede optimizar las llamadas a métodos semisincrónicos mediante la marca **wbemFlagForwardOnly** . La marca **wbemFlagForwardOnly** , combinada con la marca **wbemFlagReturnImmediately** (la marca semisincrónica predeterminada) indica a WMI que devuelva un [**SWbemObjectSet**](swbemobjectset.md)de solo avance, lo que elimina el problema de rendimiento del conjunto de datos grande. Sin embargo, el uso de la marca **wbemFlagForwardOnly** incluye un costo. Un **SWbemObjectSet** de solo avance solo se puede enumerar una vez. Una vez que se tiene acceso a cada [**SWbemObject**](swbemobject.md) en un **SWbemObjectSet** de solo avance, se libera la memoria asignada a la instancia.

A excepción de los métodos [**Delete**](swbemservices-delete.md), [**ExecMethod**](swbemservices-execmethod.md), [**Get**](swbemservices-get.md)y nueve asincrónicos, semisincrónico es el modo de funcionamiento predeterminado y recomendado.

**Métodos usados con frecuencia**

Los métodos que se usan con más frecuencia en los scripts de administración del sistema son [**instances**](swbemservices-instancesof.md), [**ExecQuery**](swbemservices-execquery.md), [**Get**](swbemservices-get.md)y [**ExecNotificationQuery**](swbemservices-execnotificationquery.md). Aunque a menudo se usa, la **instancia** de no es necesariamente la manera recomendada de recuperar información (aunque es posiblemente la manera más sencilla).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | \_ISWBEMSERVICES IID<br/>                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Scripting de objetos de API](scripting-api-objects.md)
</dt> <dt>

[Llamar a un método](calling-a-method.md)
</dt> </dl>

 

