---
title: Problemas de implementación para proveedores adsi
description: Problemas de implementación para proveedores adsi
ms.assetid: 0be772aa-e7d8-4d34-b55a-162abfb0bfd4
ms.tgt_platform: multiple
keywords:
- Problemas de implementación de ADSI Providers ADSI
- proveedores ADSI, implementando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 848744673fff9dc98622f17ff89b1a8a552076d57451a771cfc0af66151213ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821355"
---
# <a name="implementation-issues-for-adsi-providers"></a>Problemas de implementación para proveedores adsi

Para implementar interfaces ADSI, implemente primero la interfaz COM [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). Al proporcionar esta interfaz como una capa de sobrecarga mínima, se proporciona a las aplicaciones cliente el control necesario para acceder a los objetos de directorio directamente desde el directorio en lugar de a través de la caché ADSI, lo que optimiza el rendimiento de la red. El uso de esta interfaz también proporciona su propia implementación con la máxima flexibilidad.

En segundo lugar, implemente las interfaces ADSI fundamentales, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)y las interfaces de caché de propiedades [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry), [**IADsPropertyList.**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup) e [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) también son interfaces a petición frecuente del software de administración del sistema.

En tercer lugar, implemente las interfaces de administración de esquemas si el servicio de directorio tiene un esquema subyacente: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax). Si no hay ningún esquema subyacente, use estas interfaces para abstraer las clases y propiedades que usa el servicio de directorio. Los esquemas se pueden usar para publicar las características del servicio de directorio en clientes ADSI.

## <a name="collections"></a>Colecciones

Los componentes del proveedor ADSI pueden seguir uno de los tres modelos para almacenar en caché las colecciones durante la enumeración. La elección de un modelo de almacenamiento en caché determina el comportamiento de ADSI cuando se elimina un objeto de una colección del servicio de directorio subyacente externo a ADSI.

Los modelos de almacenamiento en caché incluyen:

-   Colecciones almacenadas en caché de antemano. La colección de instancias de objeto se recupera del servicio de directorio subyacente en su totalidad cuando se llama a [**IADsCollection::get \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) para crear un nuevo objeto enumerador. Si el objeto de origen de una instancia de objeto Active Directory de la colección recuperada se elimina del servicio de directorio subyacente, el cliente no reconoce la eliminación hasta que un [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) intenta acceder a la colección.
-   Colecciones almacenadas en caché incrementalmente. La colección se recupera del servicio de directorio subyacente de un objeto a la vez cuando se llama a [**IEnumVARIANT::Next.**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) volverá al principio de la colección en la memoria caché e **IEnumVARIANT::Next** devolverá objetos almacenados en caché hasta que se alcance el final de la memoria caché, momento en el que se agregarán nuevos objetos desde el almacén subyacente. Cuando una instancia de objeto Active Directory está en la memoria caché, el cliente no será consciente de su eliminación del servicio de directorio subyacente hasta que un [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) intente acceder al objeto.
-   Colecciones no almacenadas en caché. La colección se recupera del servicio de directorio subyacente de un objeto a la vez cuando se llama a [**IEnumVARIANT::Next.**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) [**IEnumVARIANT::Reset**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-reset) volverá al principio de la colección en el almacén subyacente. **Las operaciones IEnumVARIANT::Next** **e IEnumVARIANT::Reset** no pueden recuperar objetos eliminados, porque los objetos se recuperan a petición desde el servicio de directorio subyacente. Solo se almacena en caché el objeto actual; Si se elimina el objeto actual, el cliente no será consciente de su eliminación del servicio de directorio subyacente hasta que un [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) intente acceder al objeto.

Independientemente del modelo de almacenamiento en caché, tenga en cuenta que la enumeración ADSI devuelve Active Directory interfaces de servicio al autor de la llamada. Para evitar la sobrecarga de obtener un nuevo puntero de interfaz, las aplicaciones ADSI deben almacenar en caché los punteros de interfaz devueltos para los objetos que pretenden manipular. Por ejemplo, una Visual Basic que enumera un contenedor y rellena un cuadro de lista con nombres puede almacenar en caché los punteros de interfaz asociados a los nombres para su uso posterior. Este enfoque proporcionará un mayor rendimiento que rellenar el cuadro de lista durante la enumeración y obtener un nuevo puntero de interfaz cuando el usuario realiza una selección.

## <a name="about-dispatch-ids"></a>Acerca de los IDs de distribución

[**IDispatch es**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) una interfaz de Automation definida por COM para controladores que no usan interfaces COM directamente. El acceso a un objeto a través de **IDispatch** se denomina acceso enlazado a nombre o enlazado en tiempo de ejecución, porque se produce en tiempo de ejecución ("en tiempo de ejecución") y usa nombres de cadena de propiedades y métodos para resolver referencias ("nombre"). En tiempo de ejecución, los clientes pasan el nombre de cadena de la propiedad o método al que desean llamar en el método [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames)(). Si la propiedad o el método existe en el objeto , se recupera el identificador de distribución (dispID) de la función correspondiente. A continuación, el dispID se usa para ejecutar la función a través [**de IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke)(). Con **IDispatch**, las propiedades y los métodos de las interfaces expuestas por un solo objeto aparecen como una lista plana. Dado que el acceso enlazado a nombres requiere dos llamadas de función, es menos eficaz que usar directamente una interfaz COM. Se recomienda a los clientes usar las interfaces COM adsi en los objetos cuando el rendimiento es una consideración. Los controladores de Automatización avanzada, como Visual Basic 4.0, pueden llamar a otras interfaces COM, así como **a IDispatch,** si las interfaces cumplen las restricciones de Automation para los tipos de datos y el paso de parámetros.

Los proveedores adsi generan dispID dinámicamente para cada Active Directory objeto. Los dispID recuperados a través de [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) para un objeto determinado son los valores generados, pero no los valores que están en el IDL del objeto. [**Los usuarios de IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) deben llamar **a GetIDsOfNames** para obtener dispID válidos en tiempo de ejecución.

## <a name="type-information-and-type-libraries"></a>Información de tipos y bibliotecas de tipos

El SDK de ADSI proporciona una biblioteca de tipos, Activeds.tlb, que documenta todas las interfaces estándar compatibles con ADSI. Un proveedor debe proporcionar una biblioteca de tipos similar para todas las interfaces que se encuentran en Activeds.tlb, además de cualquier dato de tipo adicional para las interfaces implementadas dentro del componente de proveedor.

A continuación se muestra un ejemplo de código IDL.

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

El modelo de objetos componentes (COM) describe los tres modelos de subprocesos siguientes. Las aplicaciones COM indican qué modelo está en uso al inicializar la biblioteca COM mediante las funciones [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) y [**CoInitializeEx:**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex)

-   Subproceso único. El modelo de subproceso único supone un único subproceso de ejecución en un proceso, suponiendo además que las estructuras de datos COM de un proceso no necesitan serialización de acceso.
-   Subprocesamiento de apartamento. Un objeto COM está asociado al subproceso que lo creó. El subproceso que creó ese objeto debe ejecutar las llamadas a un objeto en otro subproceso. Para ello, el subproceso de origen invoca un proxy de cliente que organiza la llamada al método y la entrega a una función de código auxiliar del servidor en el subproceso de destino a través de la cola de mensajes win32 asociada al subproceso de destino.
-   Subprocesamiento libre. Se supone que los objetos COM son seguros para subprocesos. Se permite el acceso a varios subprocesos a cualquier objeto del proceso sin ninguna serialización impuesta.

ADSI no asume ningún modelo de subprocesamiento determinado. Los escritores de componentes de proveedor deben asumir el modelo de subprocesamiento libre y garantizar la coherencia de sus estructuras de datos internas protegiéndolos de las actualizaciones no seguras para subprocesos, es decir, sin coordinación, mediante el uso de objetos de sincronización como secciones críticas o semáforos.

## <a name="object-locking"></a>Bloqueo de objetos

ADSI no impone ni define un esquema de bloqueo de objetos. Los proveedores de espacios de nombres que admiten la serialización de acceso mediante el bloqueo pueden exponer el esquema de bloqueo subyacente a través de extensiones específicas del proveedor a ADSI.

## <a name="property-names-within-a-schema"></a>Nombres de propiedad dentro de un esquema

ADSI representa las propiedades como objetos de propiedad dentro del contenedor de esquemas ADSI. Esto requiere que los nombres de propiedad sean únicos dentro de cada contenedor de esquema. El proveedor debe asegurarse de que no haya ninguna colisión de nombres.

## <a name="primary-interface"></a>Interfaz principal

Cuando un proveedor no puede identificar qué interfaz se debe devolver como interfaz principal, se deben devolver id. de **IID. \_** Esto proporciona acceso enlazado a nombres a todas las propiedades de un objeto a través de [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) y los [**métodos IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**IADs::GetEx,**](/windows/desktop/api/Iads/nf-iads-iads-getex) [**IADs::P ut**](/windows/desktop/api/Iads/nf-iads-iads-put)e [**IADs::P utEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex)

 

 