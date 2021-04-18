---
description: Es importante que comprenda la estructura de DLL necesaria de un controlador de filtro (una implementación de la interfaz de IFilter).
ms.assetid: a2b5a813-573a-44d3-8780-99603e3246c1
title: Implementar controladores de filtro en Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5f326440b31b62ff5697274962f4d4a2cfe7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720336"
---
# <a name="implementing-filter-handlers-in-windows-search"></a>Implementar controladores de filtro en Windows Search

Es importante que comprenda la estructura de DLL necesaria de un controlador de filtro (una implementación de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ).

Este tema se organiza de la siguiente manera:

- [Implementación y exportación de los puntos de entrada de DLL](#implementing-and-exporting-the-dll-entry-points)
- [Implementar la clase IFilter y el generador de clases](#implementing-the-ifilter-class-and-class-factory)
- [Heredar las interfaces COM](#inheriting-the-com-interfaces)
- [Implementar los métodos de la interfaz COM](#implementing-the-com-interface-methods)
  - [Métodos COM no implementados](#com-methods-that-are-not-implemented)
- [Recursos adicionales](#additional-resources)
- [Temas relacionados](#related-topics)

## <a name="implementing-and-exporting-the-dll-entry-points"></a>Implementación y exportación de los puntos de entrada de DLL

Cada archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) (indicado por Ifilter.dll en esta sección) debe implementar y exportar los siguientes puntos de entrada. Estos puntos de entrada se exportan normalmente mediante un archivo de definición de módulo (. def) para la interfaz **IFilter** o mediante la palabra clave **\_ \_ declspec (dllexport)** . El archivo DLL se puede registrar para que esté en cualquier carpeta, pero normalmente reside en la carpeta% SystemRoot% \\ system32.

Los puntos de entrada de DLL se enumeran y describen en la tabla siguiente.

| Nombre de DLL                                                                                     | Descripción de DLL                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver)            | El punto de entrada de [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) registra el archivo dll como un filtro en el registro. Para registrar el archivo DLL, ejecute el programa regsvr32.exe con el nombre de archivo DLL de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) como argumento: `regsvr32.exe %SystemRoot%\system32\Ifilter.dll`                                              |
| [DllUnregisterServer (función)](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) | El punto de entrada de la [función DllUnregisterServer](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) quita el archivo dll como un controlador persistente en el registro. Para anular el registro del archivo DLL, ejecute el programa regsvr32.exe con la `/u` marca: `regsvr32.exe /u %SystemRoot%\system32\Ifilter.dll`                                                                                    |
| [DllGetClassObject (función)](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)   | El cliente de indización de contenido llama al punto de entrada de la [función DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) , a través del modelo de objetos componentes (com), para crear un objeto de generador de clases para la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) y obtener un puntero a la interfaz del generador de clases de ese objeto.                                               |
| [DllCanUnloadNow, función](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)     | El cliente de indización de contenido llama al punto de entrada de la [función DllCanUnloadNow](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow) , a través de com, para determinar si es posible descargar el archivo dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  . La interfaz **IFilter** se descarga después de que no se utilice durante un intervalo de tiempo, según se especifica en el valor del registro FilterIdleTimeOut. |

## <a name="implementing-the-ifilter-class-and-class-factory"></a>Implementar la clase IFilter y el generador de clases

Por lo general, cada dll de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) implementa al menos dos clases, como CFilter y CFilterCF. La clase CFilter genera el objeto de interfaz de **IFilter** que implementa la funcionalidad de filtrado de contenido. Sus funciones miembro implementan los métodos de interfaz de la interfaz **IFilter** . Cada clase **IFilter** requiere un identificador de clase único (CLSID), que genera el implementador de la interfaz de **IFilter** .

La clase CFilterCF genera el objeto de generador de clases para la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . Se llama al generador de clases, a través de su interfaz de [interfaz IClassFactory](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) , mediante el punto de entrada de la [función DllGetClassObject](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject) del archivo dll. La clase CFilterCF crea el objeto CFilter y devuelve un puntero a [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown). En casos más complejos, un **IFilter** puede implementar una jerarquía de clases en lugar de la clase CFilter única.

## <a name="inheriting-the-com-interfaces"></a>Heredar las interfaces COM

Windows Search 3,0 y versiones posteriores requieren que se use [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) por las siguientes razones:

- Para garantizar el rendimiento y la compatibilidad futura.
- Para ayudar a aumentar la seguridad. Los IFilters implementados con [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) son más seguros porque el contexto en el que se ejecuta la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) no necesita los derechos para abrir archivos en el disco o a través de la red.
- Aunque Windows Search solo usa [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), la clase de interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) también puede heredar las implementaciones de interfaz de la interfaz [IPersistFile](/windows/win32/api/objidl/nn-objidl-ipersistfile) y/o [IPersistStorage](/windows/win32/api/objidl/nn-objidl-ipersiststorage) para la compatibilidad con versiones anteriores.

Estas interfaces se declaran en archivos incluidos en el directorio de inclusión de mssdk \\ y tienen identificadores de interfaz predefinidos (IID). El cliente de indización de contenido consulta la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) a través de [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para determinar cuál de estas interfaces usar al filtrar el contenido.

## <a name="implementing-the-com-interface-methods"></a>Implementar los métodos de la interfaz COM

La interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) implementa los métodos [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) para la clase de interfaz de **IFilter** y el generador de clases de interfaz de **IFilter** . En la tabla siguiente se enumeran, en orden vtable, las interfaces y los métodos específicos de la interfaz de **IFilter** que debe implementar la interfaz de **IFilter** . La interfaz **IFilter** debe implementar al menos [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), pero puede implementar interfaces derivadas de IPersist adicionales.

| Interfaz COM                                                                             | Método                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IClassFactory (interfaz)](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)   | CreateInstance, Lockserver (                                                                                                                                                                                                                                                     |
| [Interfaz IClassFactory2](/windows/win32/api/ocidl/nn-ocidl-iclassfactory2)  | GetLicInfo, RequestLicKey, CreateInstanceLic                                                                                                                                                                                                                                   |
| [**Imaging**](/windows/win32/api/filter/nn-filter-ifilter)                                                        | [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init), [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext), [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue), [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) |
| [IPersist (interfaz)](/windows/desktop/api/objidl/nn-objidl-ipersist)               | GetClassID                                                                                                                                                                                                                                                                     |
| [IPersistFile (interfaz)](/windows/win32/api/objidl/nn-objidl-ipersistfile)    | IsDirty, cargar, guardar, SaveCompleted, GetCurFile                                                                                                                                                                                                                                 |
| [IPersistStorage (interfaz)](/windows/win32/api/objidl/nn-objidl-ipersiststorage) | IsDirty, cargar, guardar, GetSizeMax                                                                                                                                                                                                                                                |
| [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)            | IsDirty, cargar, guardar, GetSizeMax                                                                                                                                                                                                                                                |

En la página de referencia de cada método se especifican los parámetros y el comportamiento funcional de ese método. Cada página de referencia también proporciona los códigos de resultado que se van a implementar para ese método. Las páginas de referencia de los métodos de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) proporcionan a los códigos específicos de la interfaz de los códigos de resultado de la [ \_ ITF de servicio](../com/codes-in-facility-itf.md) que se van a implementar, y el cliente de indización de contenido también puede controlar cualquiera de los códigos de resultado genéricos, como Facility \_ y Facility \_ Win32. Para obtener más información, vea [estructura de los códigos de error com](../com/structure-of-com-error-codes.md).

### <a name="com-methods-that-are-not-implemented"></a>Métodos COM no implementados

La interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) debe implementar al menos [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream), pero no es necesario implementar otras interfaces derivadas de IPersist.

Windows Search no necesita implementar los métodos COM que se enumeran en la tabla siguiente.

| Método que no es necesario                               | Descripción                       |
|-----------------------------------------------------------|-----------------------------------|
| IPersistStream:: IsDirty                                   | Los filtros deben devolver E \_ NOTIMPL. |
| IPersistStream:: Save                                      | Los filtros deben devolver E \_ NOTIMPL. |
| IPersistStream:: GetSizeMax                                | Los filtros deben devolver E \_ NOTIMPL. |
| [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Los filtros deben devolver E \_ NOTIMPL. |

## <a name="additional-resources"></a>Recursos adicionales

- En el ejemplo de código [IFilterSample](-search-sample-ifiltersample.md) , disponible en [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample), se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .
- Para obtener información general sobre el proceso de indización, vea [el proceso de indización](-search-indexing-process-overview.md).
- Para obtener información general sobre los tipos de archivo, consulte [tipos de archivo](../shell/fa-file-types.md).
- Para consultar los atributos de Asociación de archivo para un tipo de archivo, consulte [PerceivedTypes, SystemFileAssociations y registro de aplicaciones](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Temas relacionados

[Desarrollar controladores de filtro](-search-ifilter-conceptual.md)

[Descripción de los controladores de filtro en Windows Search](-search-ifilter-about.md)

[Prácticas recomendadas para crear controladores de filtro en Windows Search](-search-3x-wds-extidx-filters.md)

[Devolver propiedades de un controlador de filtro](-search-ifilter-property-filtering.md)

[Controladores de filtro que se distribuyen con Windows](-search-ifilter-implementations.md)

[Registrar controladores de filtro](-search-ifilter-registering-filters.md)

[Probar controladores de filtro](-search-ifilter-testing-filters.md)
