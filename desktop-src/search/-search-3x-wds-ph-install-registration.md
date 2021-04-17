---
description: La instalación de un controlador de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio de archivos de programa y, a continuación, registrar el controlador de protocolo a través del registro.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Instalar y registrar controladores de protocolo (búsqueda de Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686624"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a>Instalar y registrar controladores de protocolo (búsqueda de Windows)

La instalación de un controlador de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio de archivos de programa y, a continuación, registrar el controlador de protocolo a través del registro. La aplicación de instalación también puede Agregar una raíz de búsqueda y reglas de ámbito para definir un ámbito de rastreo predeterminado para el origen de datos de Shell.

Este tema se organiza de la siguiente manera:

-   [Acerca de las direcciones URL](#about-urls)
-   [Implementar interfaces de controlador de protocolo](#implementing-protocol-handler-interfaces)
    -   [ISearchProtocol y ISearchProtocol2](#isearchprotocol-and-isearchprotocol2)
    -   [IUrlAccessor, IUrlAccessor2, IUrlAccessor3 y IUrlAccessor4](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [IProtocolHandlerSite](#iprotocolhandlersite)
-   [Implementar controladores de filtro para contenedores](#implementing-filter-handlers-for-containers)
-   [Instalación y registro de un controlador de protocolo](#installing-and-registering-a-protocol-handler)
    -   [Directrices para registrar un controlador de protocolo](#guidelines-for-registering-a-protocol-handler)
    -   [Registrar un controlador de protocolo](#installing-and-registering-a-protocol-handler)
    -   [Registrar el controlador de tipo de archivo del controlador de protocolo](#registering-the-protocol-handlers-file-type-handler)
-   [Asegurarse de que los elementos están indexados](#ensuring-that-your-items-are-indexed)
-   [Temas relacionados](#related-topics)

## <a name="about-urls"></a>Acerca de las direcciones URL

Windows Search usa las direcciones URL para identificar de forma única los elementos de la jerarquía del origen de datos de Shell. La dirección URL que es el primer nodo de la jerarquía se denomina [raíz de búsqueda](-search-3x-wds-extidx-csm-searchroots.md); Windows Search comenzará la indexación en la raíz de búsqueda, solicitando que el controlador de protocolo Enumere los vínculos secundarios para cada dirección URL.

La estructura de direcciones URL típica es:


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



La sintaxis de la dirección URL se describe en la tabla siguiente.



| Sintaxis           | Descripción                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | Identifica el controlador de protocolo que se va a invocar para la dirección URL.                                                                                                                                                           |
| {SID de usuario}       | Identifica el contexto de seguridad del usuario en el que se llama al controlador de protocolo. Si no se identifica ningún identificador de seguridad (SID) de usuario, se llama al controlador de protocolo en el contexto de seguridad del servicio de sistema. |
| <path>     | Define la jerarquía del almacén, donde cada barra diagonal ('/') es un separador entre los nombres de carpeta.                                                                                                            |
| <ItemID>   | Representa una cadena única que identifica el elemento secundario (por ejemplo, el nombre de archivo).                                                                                                                            |



 

El indexador de Windows Search recorta la barra diagonal final de las direcciones URL. Como resultado, no se puede confiar en la existencia de una barra diagonal final para identificar un directorio en lugar de un elemento. El controlador de protocolo debe ser capaz de controlar esta sintaxis de URL. Asegúrese de que el nombre de protocolo que selecciona para identificar el origen de datos de Shell no entra en conflicto con los actuales. Se recomienda esta Convención de nomenclatura: `companyName.scheme` .

Para obtener más información sobre la creación de un origen de datos de Shell, vea [implementar las interfaces de objeto de carpeta básicas](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="implementing-protocol-handler-interfaces"></a>Implementar interfaces de controlador de protocolo

La creación de un controlador de protocolo requiere la implementación de las tres interfaces siguientes:

-   [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) para administrar objetos UrlAccessor.
-   [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) para exponer las propiedades e identificar los filtros adecuados para los elementos del origen de datos de Shell.
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para filtrar los archivos propietarios o para enumerar y filtrar los archivos almacenados jerárquicamente.

Aparte de las tres interfaces obligatorias que se enumeran, las otras interfaces son opcionales y tiene la libertad de implementar las interfaces opcionales más adecuadas para la tarea a mano.

### <a name="isearchprotocol-and-isearchprotocol2"></a>ISearchProtocol y ISearchProtocol2

Las interfaces SearchProtocol inicializan y administran los objetos de UrlAccessor del controlador de protocolo. La interfaz [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) es una extensión opcional de [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)e incluye un método adicional para especificar más información sobre el usuario y el elemento.

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a>IUrlAccessor, IUrlAccessor2, IUrlAccessor3 y IUrlAccessor4

Las interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) se describen en la tabla siguiente.



| Interfaz                                                 | Descripción                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | En el caso de una dirección URL especificada, la interfaz [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) proporciona acceso a las propiedades del elemento que se expone en la dirección URL. También puede enlazar esas propiedades a un filtro específico del controlador de protocolo (es decir, un filtro distinto del asociado al nombre de archivo). |
| [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (opcional) | La interfaz [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) extiende [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) con métodos que obtienen una página de códigos para las propiedades del elemento y su dirección URL de visualización, y que obtienen el tipo de elemento en la dirección URL (documento o directorio).                                    |
| [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (opcional) | La interfaz [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) extiende [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) con un método que obtiene una matriz de SID de usuario, lo que permite al host del Protocolo de búsqueda suplantar a estos usuarios para indizar el elemento.                                                      |
| [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (opcional) | La interfaz [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) extiende la funcionalidad de la interfaz [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) con un método que identifica si se debe indizar el contenido del elemento.                                                                 |



 

Un objeto SearchProtocol crea una instancia del objeto UrlAccessor y lo inicializa. Las interfaces [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) proporcionan acceso a fragmentos importantes de información a través de los métodos que se describen en la tabla siguiente.



| Método                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | Devuelve la hora a la que se modificó la dirección URL por última vez. Si esta hora es más reciente que la última vez que el indexador procesó esta dirección URL, se llama a los controladores de filtro (implementaciones de la interfaz de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ) para extraer los datos modificados (posiblemente) de ese elemento. Se omiten las horas modificadas de los directorios. |
| [**IUrlAccessor::IsDirectory**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | Identifica si la dirección URL representa una carpeta que contiene las direcciones URL secundarias.                                                                                                                                                                                                                                                            |
| [**IUrlAccessor::BindToStream**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | Enlaza a una [interfaz IStream](/windows/win32/api/objidl/nn-objidl-istream) que representa los datos de un archivo en un almacén de datos personalizado.                                                                                                                                                                           |
| [**IUrlAccessor::BindToFilter**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | Enlaza a un [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)específico del controlador de protocolo, que puede exponer propiedades para el elemento.                                                                                                                                                                                                                 |
| [**IUrlAccessor4::ShouldIndexItemContent**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | Identifica si se debe indizar el contenido del elemento.                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a>IProtocolHandlerSite

La interfaz [**IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) se usa para crear instancias de un controlador de filtro, que se hospeda en un proceso aislado. El controlador de filtro adecuado se obtiene para un identificador de clase persistente (CLSID), una clase de almacenamiento de documentos o una extensión de nombre de archivo especificados. La ventaja de solicitar que el proceso de host se enlace a [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) es que el proceso de host puede administrar el proceso de búsqueda de un controlador de filtro adecuado y controlar la seguridad implicada en la llamada al controlador.

## <a name="implementing-filter-handlers-for-containers"></a>Implementar controladores de filtro para contenedores

Si va a implementar un controlador de protocolo jerárquico, debe implementar un controlador de filtro para un contenedor que enumera las direcciones URL secundarias. Un controlador de filtro es una implementación de la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) . El proceso de enumeración es un bucle a través de los métodos [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) y [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) de la interfaz **IFilter** . cada dirección URL secundaria se expone como el valor de la propiedad.

[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devuelve las propiedades del contenedor. Para enumerar las direcciones URL secundarias, **IFilter:: GetChunk** devuelve uno de los siguientes:

-   [PKEY \_ Buscar \_ UrlToIndex](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):

    Dirección URL del elemento sin la hora de la última modificación. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve un PROPVARIANT que contiene la dirección URL secundaria.

-   [PKEY \_ Buscar \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):

    La dirección URL y la hora de la última modificación. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve un PROPVARIANT que contiene un vector de la dirección URL secundaria y la hora de la última modificación.

Devolver [PKEY \_ Search \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) es más eficaz porque el indexador puede determinar inmediatamente si el elemento debe indexarse sin llamar a los métodos [**ISearchProtocol:: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) y [**IUrlAccessor:: GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) .

En el ejemplo de código siguiente se muestra cómo devolver la propiedad [ \_ \_ UrlToIndexWithModificationTime de búsqueda de PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) .

> [!IMPORTANT]
>
> Copyright (c) Microsoft Corporation. Todos los derechos reservados.

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> Un componente de [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de contenedor siempre debe enumerar todas las direcciones URL secundarias aunque no hayan cambiado las direcciones URL secundarias, ya que el indexador detecta eliminaciones a través del proceso de enumeración. Si la fecha de salida en [un \_ \_ UrlToIndexWithModificationTime de búsqueda de PKEY](../properties/props-system-search-urltoindexwithmodificationtime.md) indica que los datos no han cambiado, el indexador no actualiza los datos de esa dirección URL.

 

## <a name="installing-and-registering-a-protocol-handler"></a>Instalación y registro de un controlador de protocolo

La instalación de controladores de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio de archivos de programa y, a continuación, registrar los archivos DLL. Los controladores de protocolo deben implementar el registro automático para la instalación. La aplicación de instalación también puede Agregar una raíz de búsqueda y reglas de ámbito para definir un ámbito de rastreo predeterminado para el origen de datos de Shell, que se describe en [asegurarse de que los elementos se indexan](#ensuring-that-your-items-are-indexed) al final de este tema.

### <a name="guidelines-for-registering-a-protocol-handler"></a>Directrices para registrar un controlador de protocolo

Debe seguir estas instrucciones al registrar un controlador de protocolo:

-   El instalador debe utilizar el instalador EXE o MSI.
-   Se deben proporcionar las notas de la versión.
-   Se debe crear una entrada agregar o quitar programas para cada complemento instalado.
-   El instalador debe asumir toda la configuración del registro para el tipo de archivo o almacén concreto que el complemento actual entienda.
-   Si se está sobrescribiendo un complemento anterior, el instalador debe notificar al usuario.
-   Si un complemento más reciente ha sobrescrito el complemento anterior, debería tener la capacidad de restaurar la funcionalidad del complemento anterior y convertirlo de nuevo en el complemento predeterminado para ese tipo de archivo.
-   El instalador debe definir un ámbito de rastreo predeterminado para el indizador agregando una raíz de búsqueda y reglas de ámbito mediante el administrador de ámbito de rastreo (CSM).

### <a name="registering-a-protocol-handler"></a>Registrar un controlador de protocolo

Debe hacer 14 entradas en el registro para registrar el componente de controlador de protocolo, donde:

-   *Ver \_ Ind \_ ProgID* es el ProgID independiente de la versión de la implementación del controlador de protocolo.
-   *Ver \_ El \_ identificador de programa (ProgID* ) de DEP es el ProgID dependiente de la versión de la implementación del controlador de protocolo.
-   *CLSID \_ 1* es el CLSID de la implementación del controlador de protocolo.

**Para registrar un controlador de protocolo:**

1.  Registre el ProgID independiente de la versión con las claves y los valores siguientes:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  Registre el ProgID dependiente de la versión con los siguientes valores y claves:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  Registre el CLSID del controlador de protocolo con las claves y los valores siguientes:

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  Registre el controlador de protocolo con Windows Search. En el ejemplo siguiente, <Protocol Name> es el nombre del Protocolo, como archivo, MAPI, etc.:

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    Antes de Windows Vista:

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a>Registrar el controlador de tipo de archivo del controlador de protocolo

Debe crear dos entradas en el registro para registrar el controlador de tipo de archivo del controlador de protocolo (que también se conoce como extensión de Shell).

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a>Asegurarse de que los elementos están indexados

Después de haber implementado el controlador de protocolo, debe especificar los elementos de Shell que va a indizar el controlador de protocolo. Puede usar el administrador de catálogo para iniciar la reindización (para obtener más información, vea [usar el administrador de catálogos](-search-3x-wds-mngidx-catalog-manager.md)). También puede usar el administrador de ámbito de rastreo (CSM) para configurar las reglas predeterminadas que indican las direcciones URL que desea que rastree el indexador (para obtener más información, consulte [uso del administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md) y [Administración de reglas de ámbito](-search-3x-wds-extidx-csm-scoperules.md)). También puede Agregar una raíz de búsqueda (para obtener más información, consulte [Administración de raíces de búsqueda](-search-3x-wds-extidx-csm-searchroots.md)). Otra opción disponible es seguir el procedimiento descrito en el ejemplo REINDEX en los [ejemplos del SDK de Windows Search](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

La interfaz [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) proporciona métodos que notifican al motor de búsqueda de los contenedores que se van a rastrear o inspeccionar, y a los elementos de esos contenedores incluir o excluir al rastrear o ver. En Windows 7 y versiones posteriores, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extiende **ISearchCrawlScopeManager** con el método [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) que obtiene la versión, que informa a los clientes de si el estado de la CSM ha cambiado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Vista**
</dt> <dt>

[Descripción de los controladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Desarrollar controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notificar el índice de cambios](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Agregar iconos y menús contextuales](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Código de ejemplo: extensiones de Shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Crear un conector de búsqueda para un controlador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Controladores de protocolo de depuración](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
