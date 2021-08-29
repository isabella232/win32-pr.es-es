---
description: La instalación de un controlador de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio Archivos de programa y, a continuación, registrar el controlador de protocolo a través del Registro.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Instalación y registro de controladores de protocolo (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a71a47c7ea3fbc82607749239838a7f03fb784d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880122"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a>Instalación y registro de controladores de protocolo (Windows Search)

La instalación de un controlador de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio Archivos de programa y, a continuación, registrar el controlador de protocolo a través del Registro. La aplicación de instalación también puede agregar una raíz de búsqueda y reglas de ámbito para definir un ámbito de rastreo predeterminado para el origen de datos de Shell.

Este tema se organiza de la siguiente manera:

-   [Acerca de las direcciones URL](#about-urls)
-   [Implementar interfaces de controlador de protocolos](#implementing-protocol-handler-interfaces)
    -   [ISearchProtocol e ISearchProtocol2](#isearchprotocol-and-isearchprotocol2)
    -   [IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [IProtocolHandlerSite](#iprotocolhandlersite)
-   [Implementar controladores de filtro para contenedores](#implementing-filter-handlers-for-containers)
-   [Instalar y registrar un controlador de protocolo](#installing-and-registering-a-protocol-handler)
    -   [Directrices para registrar un controlador de protocolos](#guidelines-for-registering-a-protocol-handler)
    -   [Registro de un controlador de protocolo](#installing-and-registering-a-protocol-handler)
    -   [Registrar el controlador de tipos de archivo del controlador de protocolos](#registering-the-protocol-handlers-file-type-handler)
-   [Asegurarse de que los elementos están indexados](#ensuring-that-your-items-are-indexed)
-   [Temas relacionados](#related-topics)

## <a name="about-urls"></a>Acerca de las direcciones URL

Windows La búsqueda usa direcciones URL para identificar de forma única los elementos de la jerarquía del origen de datos de Shell. La dirección URL que es el primer nodo de la jerarquía se denomina raíz [de búsqueda](-search-3x-wds-extidx-csm-searchroots.md); Windows La búsqueda comenzará la indexación en la raíz de búsqueda, solicitando que el controlador de protocolo enumere los vínculos secundarios para cada dirección URL.

La estructura de dirección URL típica es:


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



La sintaxis de la dirección URL se describe en la tabla siguiente.



| Sintaxis           | Descripción                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| &lt;protocolo&gt; | Identifica el controlador de protocolo que se va a invocar para la dirección URL.                                                                                                                                                           |
| {SID de usuario}       | Identifica el contexto de seguridad del usuario bajo el que se llama al controlador de protocolo. Si no se identifica ningún identificador de seguridad de usuario (SID), se llama al controlador de protocolo en el contexto de seguridad del servicio del sistema. |
| &lt;path&gt;     | Define la jerarquía del almacén, donde cada barra diagonal ('/') es un separador entre los nombres de carpeta.                                                                                                            |
| &lt;Itemid&gt;   | Representa una cadena única que identifica el elemento secundario (por ejemplo, el nombre de archivo).                                                                                                                            |



 

El Windows search indexer recorta la barra diagonal final de las direcciones URL. Como resultado, no puede confiar en la existencia de una barra diagonal final para identificar un directorio frente a un elemento. El controlador de protocolo debe ser capaz de controlar esta sintaxis de dirección URL. Asegúrese de que el nombre de protocolo que seleccione para identificar el origen de datos de Shell no entre en conflicto con los actuales. Se recomienda esta convención de nomenclatura: `companyName.scheme` .

Para obtener más información sobre cómo crear un origen de datos de Shell, vea [Implementing the Basic Folder Object Interfaces](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="implementing-protocol-handler-interfaces"></a>Implementar interfaces de controlador de protocolos

La creación de un controlador de protocolo requiere la implementación de las tres interfaces siguientes:

-   [**ISearchProtocol para**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) administrar objetos UrlAccessor.
-   [**IUrlAccessor para**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) exponer propiedades e identificar los filtros adecuados para los elementos del origen de datos de Shell.
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) para filtrar archivos propietarios o para enumerar y filtrar archivos almacenados jerárquicamente.

Aparte de las tres interfaces obligatorias enumeradas, las otras interfaces son opcionales y puede implementar las interfaces opcionales que sean más adecuadas para la tarea en la mano.

### <a name="isearchprotocol-and-isearchprotocol2"></a>ISearchProtocol e ISearchProtocol2

Las interfaces SearchProtocol inicializan y administran los objetos UrlAccessor del controlador de protocolos. La [**interfaz ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) es una extensión opcional de [**ISearchProtocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)e incluye un método adicional para especificar más información sobre el usuario y el elemento.

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a>IUrlAccessor, IUrlAccessor2, IUrlAccessor3 e IUrlAccessor4

Las [**interfaces IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) se describen en la tabla siguiente.



| Interfaz                                                 | Descripción                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | Para una dirección URL especificada, la [**interfaz IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) proporciona acceso a las propiedades del elemento que se expone en la dirección URL. También puede enlazar esas propiedades a un filtro específico del controlador de protocolo (es decir, un filtro distinto del asociado al nombre de archivo). |
| [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (opcional) | La [**interfaz IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) amplía [**IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) con métodos que obtienen una página de códigos para las propiedades del elemento y su dirección URL de presentación, y que obtienen el tipo de elemento en la dirección URL (documento o directorio).                                    |
| [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (opcional) | La [**interfaz IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) extiende [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) con un método que obtiene una matriz de SID de usuario, lo que permite al host del protocolo de búsqueda suplantar a estos usuarios para indexar el elemento.                                                      |
| [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (opcional) | La [**interfaz IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) amplía la funcionalidad de la interfaz [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) con un método que identifica si se debe indexar el contenido del elemento.                                                                 |



 

Un objeto SearchProtocol crea una instancia del objeto UrlAccessor y lo inicializa. Las [**interfaces IUrlAccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) proporcionan acceso a información importante a través de los métodos descritos en la tabla siguiente.



| Método                                                                                        | Descripción                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUrlAccessor::GetLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | Devuelve la hora a la que se modificó la dirección URL por última vez. Si esta hora es más reciente que la última vez que el indexador procesó esta dirección URL, se llama a los controladores de filtro (implementaciones de la interfaz [**IFilter)**](/windows/win32/api/filter/nn-filter-ifilter) para extraer los (posiblemente) datos modificados para ese elemento. Se omiten las horas de modificación de los directorios. |
| [**IUrlAccessor::IsDirectory**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | Identifica si la dirección URL representa una carpeta que contiene direcciones URL secundarias.                                                                                                                                                                                                                                                            |
| [**IUrlAccessor::BindToStream**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | Enlaza a una [interfaz IStream que](/windows/win32/api/objidl/nn-objidl-istream) representa los datos de un archivo en un almacén de datos personalizado.                                                                                                                                                                           |
| [**IUrlAccessor::BindToFilter**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | Enlaza a un IFilter específico del controlador de [**protocolo,**](/windows/win32/api/filter/nn-filter-ifilter)que puede exponer las propiedades del elemento.                                                                                                                                                                                                                 |
| [**IUrlAccessor4::ShouldIndexItemContent**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | Identifica si se debe indexar el contenido del elemento.                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a>IProtocolHandlerSite

La [**interfaz IProtocolHandlerSite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) se usa para crear instancias de un controlador de filtro, que se hospeda en un proceso aislado. Se obtiene el controlador de filtro adecuado para un identificador de clase persistente (CLSID) especificado, una clase de almacenamiento de documentos o una extensión de nombre de archivo. La ventaja de solicitar al proceso de host que se enlace a [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) es que el proceso de host puede administrar el proceso de buscar un controlador de filtro adecuado y controlar la seguridad implicada en la llamada al controlador.

## <a name="implementing-filter-handlers-for-containers"></a>Implementar controladores de filtro para contenedores

Si va a implementar un controlador de protocolo jerárquico, debe implementar un controlador de filtro para un contenedor que enumera las direcciones URL secundarias. Un controlador de filtro es una implementación de la [**interfaz IFilter.**](/windows/win32/api/filter/nn-filter-ifilter) El proceso de enumeración es un bucle a través de los métodos [**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) [**e IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) de la **interfaz IFilter;** cada dirección URL secundaria se expone como el valor de la propiedad .

[**IFilter::GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) devuelve las propiedades del contenedor. Para enumerar las direcciones URL secundarias, **IFilter::GetChunk** devuelve una de las siguientes opciones:

-   [PKEY \_ \_UrlToIndex de búsqueda:](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85))

    Dirección URL del elemento sin la hora de la última modificación. [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve un VALOR PROPVARIANT que contiene la dirección URL secundaria.

-   [PKEY \_ Search \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md):

    La dirección URL y la hora de la última modificación. [**IFilter::GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) devuelve un VALOR PROPVARIANT que contiene un vector de la dirección URL secundaria y la hora de la última modificación.

Devolver [PKEY \_ Search \_ UrlToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) es más eficaz porque el indexador puede determinar inmediatamente si el elemento debe indexarse sin llamar a los métodos [**ISearchProtocol::CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) [**e IUrlAccessor::GetLastModified.**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)

En el código de ejemplo siguiente se muestra cómo devolver la [propiedad \_ \_ UrlToIndexWithModificationTime de PKEY Search.](../properties/props-system-search-urltoindexwithmodificationtime.md)

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
> Un componente [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) de contenedor siempre debe enumerar todas las direcciones URL secundarias, incluso si las direcciones URL secundarias no han cambiado, porque el indexador detecta eliminaciones a través del proceso de enumeración. Si la salida de fecha en una url de búsqueda [ \_ \_ PKEYToIndexWithModificationTime](../properties/props-system-search-urltoindexwithmodificationtime.md) indica que los datos no han cambiado, el indexador no actualiza los datos de esa dirección URL.

 

## <a name="installing-and-registering-a-protocol-handler"></a>Instalación y registro de un controlador de protocolos

La instalación de controladores de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio Archivos de programa y, a continuación, registrar los archivos DLL. Los controladores de protocolo deben implementar el registro propio para la instalación. La aplicación de instalación también puede agregar una raíz de búsqueda y reglas de ámbito para definir un ámbito de rastreo predeterminado para el origen de datos de Shell, que se describe en [Asegurarse](#ensuring-that-your-items-are-indexed) de que los elementos se indexa al final de este tema.

### <a name="guidelines-for-registering-a-protocol-handler"></a>Directrices para registrar un controlador de protocolos

Debe seguir estas directrices al registrar un controlador de protocolo:

-   El instalador debe usar el instalador EXE o MSI.
-   Se deben proporcionar notas de la versión.
-   Se debe crear una entrada Agregar o quitar programas para cada complemento instalado.
-   El instalador debe asumir toda la configuración del Registro para el tipo de archivo o almacén determinado que el complemento actual entiende.
-   Si se sobrescribe un complemento anterior, el instalador debe notificar al usuario.
-   Si un complemento más reciente ha sobrescrito el complemento anterior, debe haber la capacidad de restaurar la funcionalidad del complemento anterior y convertirla de nuevo en el complemento predeterminado para ese tipo de archivo.
-   El instalador debe definir un ámbito de rastreo predeterminado para el indexador mediante la adición de una raíz de búsqueda y reglas de ámbito mediante Administrador del ámbito de rastreo (CSM).

### <a name="registering-a-protocol-handler"></a>Registrar un controlador de protocolo

Debe realizar 14 entradas en el Registro para registrar el componente de controlador de protocolo, donde:

-   *Ver \_ Ind \_ ProgID es* el ProgID independiente de la versión de la implementación del controlador de protocolo.
-   *Ver \_ Dep \_ ProgID es* el ProgID dependiente de la versión de la implementación del controlador de protocolo.
-   *CLSID \_ 1 es* el CLSID de la implementación del controlador de protocolo.

**Para registrar un controlador de protocolo:**

1.  Registre el ProgID independiente de la versión con las siguientes claves y valores:

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

2.  Registre el ProgID dependiente de la versión con las siguientes claves y valores:

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

3.  Registre el CLSID del controlador de protocolo con las siguientes claves y valores:

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

4.  Registre el controlador de protocolo con Windows Search. En el ejemplo siguiente, es el nombre del propio protocolo, como <Protocol Name> file, mapi, etc.:

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

### <a name="registering-the-protocol-handlers-file-type-handler"></a>Registrar el controlador de tipos de archivo del controlador de protocolos

Debe crear dos entradas en el Registro para registrar el controlador de tipos de archivo del controlador de protocolos (que también se conoce como extensión de Shell).

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

Después de implementar el controlador de protocolo, debe especificar qué elementos de Shell va a indexar el controlador de protocolos. Puede usar el Administrador de catálogos para iniciar la indexación de nuevo (para obtener más información, vea [Uso del Administrador de catálogos).](-search-3x-wds-mngidx-catalog-manager.md) O bien, también puede usar Administrador del ámbito de rastreo (CSM) para configurar reglas predeterminadas que indiquen las direcciones URL [](-search-3x-wds-extidx-csm.md) que desea que rastree el indexador (para obtener más información, vea Uso de la Administrador del ámbito de rastreo y Administración de reglas de [ámbito).](-search-3x-wds-extidx-csm-scoperules.md) También puede agregar una raíz de búsqueda (para obtener más información, vea [Administración de raíces de búsqueda).](-search-3x-wds-extidx-csm-searchroots.md) Otra opción disponible es seguir el procedimiento del ejemplo ReIndex de Windows [Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

La [**interfaz ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) proporciona métodos que notifican al motor de búsqueda los contenedores que se deben rastrear o observar, y los elementos de esos contenedores que se incluirán o excluirán al rastrear o observar. En Windows 7 y versiones posteriores, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) amplía **ISearchCrawlScopeManager** con el método [**ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) que obtiene la versión, que informa a los clientes de si el estado del CSM ha cambiado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Conceptual**
</dt> <dt>

[Descripción de los controladores de protocolo](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Desarrollo de controladores de protocolo](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notificación al índice de cambios](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Agregar iconos y menús contextuales](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Ejemplo de código: Extensiones de shell para controladores de protocolo](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Crear un conector de búsqueda para un controlador de protocolo](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Depuración de controladores de protocolo](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
