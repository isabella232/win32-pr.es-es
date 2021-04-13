---
title: Problemas de implementación para los proveedores ADSI
description: Problemas de implementación para los proveedores ADSI
ms.assetid: 0be772aa-e7d8-4d34-b55a-162abfb0bfd4
ms.tgt_platform: multiple
keywords:
- Problemas de implementación para los proveedores ADSI ADSI
- proveedores ADSI, implementar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c362b04244580e448e7bb7bd78889e66db12fe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421420"
---
# <a name="implementation-issues-for-adsi-providers"></a>Problemas de implementación para los proveedores ADSI

Para implementar interfaces ADSI, implemente primero la interfaz COM [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). Al proporcionar esta interfaz como una capa de sobrecarga mínima, proporciona a las aplicaciones cliente el control necesario para obtener acceso a los objetos de directorio directamente desde el directorio en lugar de hacerlo a través de la caché ADSI, lo que optimiza el rendimiento de la red. El uso de esta interfaz también proporcionará su propia implementación con la máxima flexibilidad.

En segundo lugar, implemente las interfaces ADSI fundamentales, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)y [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) de caché de propiedades. [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) y [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) también son interfaces en la demanda frecuente del software de administración del sistema.

En tercer lugar, implemente las interfaces de administración de esquemas si el servicio de directorio tiene un esquema subyacente: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax). Si no hay ningún esquema subyacente, utilice estas interfaces para abstraer las clases y propiedades utilizadas por el servicio de directorio. Los esquemas se pueden usar para publicar las características del servicio de directorio en los clientes ADSI.

## <a name="collections"></a>Colecciones

Los componentes del proveedor ADSI pueden seguir a uno de los tres modelos para almacenar en caché las colecciones durante la enumeración. La elección de un modelo de almacenamiento en caché determina el comportamiento de ADSI cuando se elimina un objeto de una colección del servicio de directorio subyacente externo a ADSI.

Los modelos de almacenamiento en caché incluyen:

-   Las colecciones se almacenan en caché de antemano. La colección de instancias de objeto se recupera del servicio de directorio subyacente en su totalidad cuando se llama a [**IADsCollection:: get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) para crear un nuevo objeto de enumerador. Si el objeto de origen de una instancia de objeto de Active Directory en la colección recuperada se elimina del servicio de directorio subyacente, el cliente no reconoce la eliminación hasta que un objeto [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) intente obtener acceso a la colección.
-   Las colecciones se almacenan en caché incrementalmente. La colección se recupera del servicio de directorio subyacente de un objeto cada vez cuando se llama a [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) . [**IEnumVARIANT:: RESET**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) volverá al principio de la colección en la memoria caché y **IEnumVARIANT:: Next** devolverá los objetos almacenados en caché hasta que se alcance el final de la memoria caché, en cuyo punto se agregarán nuevos objetos desde el almacén subyacente. Cuando una instancia de objeto Active Directory está en la memoria caché, el cliente no conocerá su eliminación desde el servicio de directorio subyacente hasta que un objeto [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) intente tener acceso al objeto.
-   Colecciones no almacenadas en caché. La colección se recupera del servicio de directorio subyacente de un objeto cada vez cuando se llama a [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) . [**IEnumVARIANT:: RESET**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) volverá al principio de la colección en el almacén subyacente. Las operaciones **IEnumVARIANT:: Next** y **IEnumVARIANT:: RESET** no pueden recuperar objetos eliminados, ya que los objetos se recuperan a petición desde el servicio de directorio subyacente. Solo se almacena en caché el objeto actual; Si se elimina el objeto actual, el cliente no conocerá su eliminación desde el servicio de directorio subyacente hasta que un objeto [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) intente tener acceso al objeto.

Independientemente del modelo de almacenamiento en caché, tenga en cuenta que la enumeración ADSI devuelve Active Directory interfaces de servicio al llamador. Para evitar la sobrecarga de obtener un nuevo puntero de interfaz, las aplicaciones ADSI deben almacenar en caché los punteros de interfaz devueltos para los objetos que se van a manipular. Por ejemplo, una aplicación Visual Basic que enumera un contenedor y rellena un cuadro de lista con nombres puede almacenar en caché los punteros de interfaz asociados a los nombres para su uso posterior. Este enfoque proporcionará un mayor rendimiento que el rellenado del cuadro de lista durante la enumeración y la obtención de un nuevo puntero de interfaz cuando el usuario realiza una selección.

## <a name="about-dispatch-ids"></a>Acerca de los ID. de envío

[**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) es una interfaz de automatización definida por com para los controladores que no utilizan directamente las interfaces com. El acceso a un objeto a través de **IDispatch** se denomina acceso enlazado a un nombre o enlace en tiempo de ejecución, ya que se produce en tiempo de ejecución ("late") y usa nombres de cadena de propiedades y métodos para resolver referencias ("Name"). En tiempo de ejecución, los clientes pasan el nombre de cadena de la propiedad o el método que desean llamar en el método [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames)(). Si la propiedad o el método existen en el objeto, se recupera el identificador de envío (DISPID) de la función correspondiente. A continuación, se usa el DISPID para ejecutar la función mediante [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)(). Con **IDispatch**, las propiedades y los métodos de las interfaces expuestas por un solo objeto aparecen como una lista plana. Dado que el acceso enlazado a nombres requiere dos llamadas a funciones, es menos eficaz que usar directamente una interfaz COM. Se anima a los clientes a usar las interfaces COM ADSI en los objetos cuando el rendimiento es una consideración. Los controladores de automatización avanzados, como Visual Basic 4,0, pueden llamar a otras interfaces COM, así como a **IDispatch**, si las interfaces cumplen con las restricciones de automatización de los tipos de datos y el paso de parámetros.

Los proveedores ADSI generan los dispids dinámicamente para cada Active Directory objeto. Los DISPID recuperados a través de [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) para un objeto determinado son los valores generados, pero no los valores que se encuentran en el IDL para el objeto. Los usuarios de [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) deben llamar a **GetIDsOfNames** para obtener los DISPID válidos en tiempo de ejecución.

## <a name="type-information-and-type-libraries"></a>Información de tipos y bibliotecas de tipos

El SDK de ADSI proporciona una biblioteca de tipos, activeds. tlb, que documenta todas las interfaces estándar compatibles con ADSI. Un proveedor debe proporcionar una biblioteca de tipos similar para todas las interfaces que se encuentran en activeds. tlb, además de los datos de tipo adicionales para las interfaces implementadas dentro del componente de proveedor.

El siguiente es un ejemplo de código IDL.

``` syntax
[ object, uuid(IID_IADsXYZ), oleautomation, dual ]
interface IADsXYZ: IDispatch
{
// Read-only properties.
[propget]
HRESULT AReadOnlyProp ([out, retval]BSTR *pbstrAReadOnlyProp);
 
// Read/write properties.
[propget]
HRESULT AReadWriteProp ([out, retval]long *plAReadWriteProp);
[propput]
HRESULT AReadWriteProp ([in]long lAReadWriteProp);
 
// Methods.
HRESULT AMethod ([in]DATE dateInParameter,
[out, retval]BSTR *pbstrReturnValue);
};
```

## <a name="thread-safety"></a>Seguridad para subprocesos

El modelo de objetos componentes (COM) describe los tres modelos de subprocesos siguientes. Las aplicaciones COM indican qué modelo se usa al inicializar la biblioteca COM mediante las funciones [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) y [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) :

-   Subprocesamiento único. El modelo de un solo subproceso presupone un único subproceso de ejecución en un proceso, con lo que se supone que las estructuras de datos COM de un proceso no necesitan ninguna serialización de acceso.
-   Subprocesamiento de apartamento. Un objeto COM está asociado al subproceso que lo creó. El subproceso que creó ese objeto debe ejecutar las llamadas a un objeto en otro subproceso. Para ello, el subproceso de origen invoca un proxy de cliente que organiza la llamada al método y la entrega a una función de código auxiliar de servidor en el subproceso de destino a través de la cola de mensajes de Win32 asociada al subproceso de destino.
-   Subprocesamiento libre. Se supone que los objetos COM son seguros para subprocesos. A varios subprocesos se les permite el acceso a cualquier objeto del proceso sin ninguna serialización impuesta.

ADSI no supone ningún modelo de subprocesos determinado. Los escritores de componentes de proveedor deben suponer el modelo de subprocesos gratuito y garantizar la coherencia de sus estructuras de datos internas mediante su protección contra los subprocesos no seguros, es decir, sin coordinación, actualizaciones mediante el uso de objetos de sincronización como secciones críticas o semáforos.

## <a name="object-locking"></a>Bloqueo de objetos

ADSI no impone ni define un esquema de bloqueo de objetos. Los proveedores de espacios de nombres que admiten la serialización de acceso mediante el bloqueo pueden exponer el esquema de bloqueo subyacente a través de extensiones específicas del proveedor a ADSI.

## <a name="property-names-within-a-schema"></a>Nombres de propiedad dentro de un esquema

ADSI representa propiedades como objetos de propiedad dentro del contenedor de esquema ADSI. Esto requiere que los nombres de propiedad sean únicos en cada contenedor de esquemas. El proveedor debe asegurarse de que no haya conflictos de nombres.

## <a name="primary-interface"></a>Interfaz principal

Cuando un proveedor no puede identificar qué interfaz se debe devolver como la interfaz principal, se debe devolver el **IID de IID \_** . Esto proporciona acceso con enlace de nombre a todas las propiedades de un objeto a través de [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) y los métodos [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex), [**iads::P UT**](/windows/desktop/api/Iads/nf-iads-iads-put)y [**IADs::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .

 

 