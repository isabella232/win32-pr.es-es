---
title: Obtener un puntero a un objeto
description: Obtener un puntero a un objeto
ms.assetid: 4af9d356-402b-4e69-9f6e-8589057d3ac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0476d36390e7077e7fdd75eef8d95e8173683891
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973672"
---
# <a name="getting-a-pointer-to-an-object"></a>Obtener un puntero a un objeto

Dado que COM no tiene un modelo de clase estricto, hay cuatro maneras en que un cliente puede crear una instancia u obtener un puntero a una interfaz en un objeto :

-   Llamar a una función de biblioteca COM que crea un objeto de un tipo predeterminado; es decir, la función devolverá un puntero a solo una interfaz específica para una clase de objeto específica.
-   Llame a una función de biblioteca COM que pueda crear un objeto basado en un identificador de clase (CLSID) y que devuelva cualquier tipo de puntero de interfaz solicitado.
-   Llame a un método de alguna interfaz que cree otro objeto (o se conecte a uno existente) y devuelva un puntero de interfaz en ese objeto independiente.
-   Implemente un objeto con una interfaz a través de la cual otros objetos pasen directamente su puntero de interfaz al cliente.

Para obtener información sobre cómo obtener punteros a otras interfaces en un objeto después de tener el primero, vea [QueryInterface: Navigating in an Object](queryinterface--navigating-in-an-object.md).

## <a name="creating-an-object-of-a-predetermined-type"></a>Crear un objeto de un tipo predeterminado

Hay numerosas funciones COM, como [**CoGetMalloc,**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetmalloc)que devuelven punteros a implementaciones de interfaz específicas. (**CoGetMalloc** recupera un puntero al asignador de memoria COM estándar). La mayoría de ellas son funciones auxiliares y la mayoría de estas funciones se describen en las secciones de referencia de esta documentación, en el área específica a la que están relacionadas, como el almacenamiento o la transferencia de datos.

## <a name="creating-an-object-based-on-a-clsid"></a>Crear un objeto basado en un CLSID

Hay varias funciones que, dado un CLSID, un cliente puede llamar a para crear una instancia de objeto y obtener un puntero a ella. Todas estas funciones se basan en la función [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), que crea un objeto de clase y proporciona un puntero a una interfaz que permite crear instancias de esa clase. Aunque debe haber información que indica en qué sistema reside el servidor, no es necesario que esa información esté contenida en el cliente. El cliente solo debe conocer el CLSID y nunca la ruta de acceso absoluta del código del servidor. Para obtener más información, vea [Crear un objeto a través de un objeto de clase](creating-an-object-through-a-class-object.md).

## <a name="returning-a-pointer-to-a-separate-object"></a>Devolver un puntero a un objeto independiente

Entre los muchos métodos de interfaz que devuelven un puntero a un objeto independiente hay varios que crean y devuelven un puntero a un objeto enumerador *,* lo que permite determinar cuántos elementos de un tipo determinado mantiene un objeto. COM define interfaces para enumerar una amplia variedad de elementos, como cadenas, estructuras importantes, monikers y punteros de interfaz [**IUnknown.**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) La manera típica de crear una instancia de enumerador y obtener un puntero a su interfaz es llamar a un método desde otra interfaz. Por ejemplo, la [**interfaz IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) define dos métodos, [**EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise) y [**EnumFormatEtc,**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc)que devuelven punteros a interfaces en dos objetos de enumeración diferentes. Hay muchos otros ejemplos en COM de métodos que devuelven punteros a objetos, como la interfaz de documento compuesta OLE [**IOleObject::GetClientSite**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclientsite), que, cuando se llama en el objeto incrustado o vinculado, devuelve un puntero a la implementación del objeto contenedor [**de IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite).

## <a name="implementing-an-object-through-which-to-pass-an-interface-pointer-directly-to-the-client"></a>Implementar un objeto a través del cual pasar un puntero de interfaz directamente al cliente

Cuando dos objetos, como un contenedor de documentos compuestos OLE y un servidor, necesitan comunicación bidireccional, cada uno implementa un objeto que contiene un método de interfaz a través del cual puede pasar un puntero de interfaz al otro objeto. El objeto de implementación, que también es el cliente del objeto creado, puede llamar al método y obtener el puntero que se pasó.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clientes y servidores COM](com-clients-and-servers.md)
</dt> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 




