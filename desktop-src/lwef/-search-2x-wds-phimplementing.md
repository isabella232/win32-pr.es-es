---
title: Implementar un controlador de protocolo para WDS
description: La creación de un controlador de protocolo implica implementar ISearchProtocol para administrar objetos UrlAccessor, IUrlAccessor para generar metadatos sobre e identificar los filtros adecuados para los elementos del almacén de datos, IProtocolHandlerSite para crear instancias de un objeto SearchProtocol e identificar los filtros adecuados, e IFilterto filtrar archivos propietarios o para enumerar y filtrar archivos almacenados jerárquicamente.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127475885"
---
# <a name="implementing-a-protocol-handler-for-wds"></a>Implementar un controlador de protocolo para WDS

> [!NOTE]
> Windows Desktop Search 2.x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use [Windows Search en](../search/-search-3x-wds-overview.md) su lugar.

La creación de un controlador de protocolo implica implementar [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) para administrar objetos UrlAccessor, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) para generar metadatos sobre e identificar los filtros adecuados para los elementos del almacén de datos, IProtocolHandlerSite para crear instancias de un objeto SearchProtocol e identificar los filtros adecuados, e [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para filtrar archivos propietarios o para enumerar y filtrar archivos almacenados jerárquicamente. El controlador de protocolo debe ser multiproceso.

En esta sección se incluyen los temas siguientes:

-   [Nota sobre las direcciones URL](#note-on-urls)
-   [Interfaces de controlador de protocolos](#protocol-handler-interfaces)
-   [IFilters for Containers](#ifilters-for-containers)
-   [Agregar funcionalidad de opciones de controlador de protocolos](#adding-protocol-handler-options-functionality)
    -   [ISearchProtocolOptions](#isearchprotocoloptions)
-   [Temas relacionados](#related-topics)

## <a name="note-on-urls"></a>Nota sobre las direcciones URL

Microsoft Windows Desktop Search (WDS) usa direcciones URL para identificar de forma única los elementos de un sistema de archivos, dentro de un almacén de tipo base de datos o en la Web. Una dirección URL que define un nodo de entrada se denomina página de inicio; WDS comienza en esa página de inicio y rastrea de forma recursiva el almacén de datos. La estructura de direcciones URL típica es:

`protocol://host/path/name.extension`

> [!Note]
>
> Si desea agregar un nuevo almacén de datos, deberá seleccionar un nombre para identificarlo que no entre en conflicto con los actuales. Se recomienda esta convención de nomenclatura: companyName.scheme.

 

## <a name="protocol-handler-interfaces"></a>Interfaces de controlador de protocolos

**ISearchProtocol**

La [**interfaz ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) invoca, inicializa y administra objetos UrlAccessor. Para obtener más información sobre cómo implementar la interfaz ISearchProtocol, vea **ISearchProtocol Interface reference (Referencia de la interfaz ISearchProtocol).**

**IUrlAccessor**

Para una dirección URL especificada, la interfaz [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) genera metadatos sobre la estructura de ubicación, así como los elementos contenidos, y enlaza esos elementos a un filtro. Un objeto SearchProtocol crea instancias del objeto **IUrlAccessor** e inicializa el objeto . Sin embargo, también puede implementar un método de inicialización interno para que el objeto **IUrlAccessor** pueda realizar tareas de inicialización específicas del controlador de protocolo, como validar la dirección URL de un elemento al que se tiene acceso o comprobar la hora de la última modificación para determinar si un archivo debe procesarse en el rastreo actual.

> [!Note]
>
> Se omiten las horas de modificación de los directorios. El [**objeto IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) debe enumerar los objetos secundarios para determinar si se han realizado modificaciones o eliminaciones.

 

Gran parte del diseño del objeto **UrlAccessor** depende de si la estructura es jerárquica o basada en vínculos. En el caso de los almacenes de datos jerárquicos, el objeto **UrlAccessor** debe encontrar un filtro que pueda enumerar su contenido. Otra distinción entre los controladores de protocolo jerárquicos y basados en vínculos es el uso del método IsDirectory. En los controladores de protocolos basados en vínculos, este método debe devolver S \_ FALSE. Los controladores de protocolo jerárquicos deben devolver S \_ OK para los contenedores.

Para obtener más instrucciones sobre cómo implementar una [**interfaz IUrlAccessor,**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) consulte la referencia de [**la interfaz IUrlAccessor.**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor)

**IProtocolHandlerSite**

Esta interfaz se usa para crear instancias de un objeto **SearchProtocol** y también proporciona al objeto **UrlAccessor** un filtro adecuado para un identificador de clase especificado (CLSID).

## <a name="ifilters-for-containers"></a>IFilters for Containers

Si va a implementar un controlador de protocolo jerárquico, debe implementar un componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)de contenedor que enumera las direcciones URL que representan contenedores o carpetas. El proceso de enumeración es un bucle a través de los métodos **GetChunk** y **GetValue** de la interfaz IFilter que devuelven una lista de direcciones URL que representan cada elemento del contenedor.

En primer **lugar, GetChunk** devuelve un FULLPROSPEC con la propiedad set GATHER \_ PROPSET y:

-   PID \_ GTHR \_ DIRLINK, la dirección URL del elemento sin la hora de la última modificación, o
-   PID \_ GTHR \_ DIRLINK \_ WITH \_ TIME, la dirección URL junto con la hora de la última modificación

El GUID del conjunto de propiedades para GATHER PROPSET es \_ 0B63E343-9CCC-11D0-BCDB-00805FCCCE04. La propiedad PROPSPEC es PID \_ GTHR \_ DIRLINK=2 o PID \_ GTHR \_ DIRLINK \_ WITH TIME = \_ 12 decimal.

Devolver DIRLINK WITH TIME de PID GTHR es más eficaz porque el indexador puede determinar inmediatamente si el elemento debe indexarse sin llamar a los métodos \_ \_ \_ \_ ISearchProtocol->CreateUrlAccessor() e IUrlAccessor->GetLastModified().

A **continuación, GetValue** devuelve propVARIANT para la dirección URL (y la hora de la última modificación, si se usa), como:

-   VT \_ LPWSTR, la dirección URL del elemento secundario o
-   Vector de la dirección URL seguido de filetime

En el código de ejemplo siguiente se muestra cómo compilar el DIRLINK WITH TIME de PID \_ GTHR \_ \_ \_ adecuado.

> [!Note]
>
> **ESTE CÓDIGO E INFORMACIÓN SE PROPORCIONAN "TAL Y COMO ESTÁN" SIN GARANTÍA DE NINGÚN TIPO, YA SEA EXPRESA O IMPLÍCITA, INCLUIDAS, ENTRE OTRAS, LAS GARANTÍAS IMPLÍCITAS DE COMERCIABILIDAD O IDONEIDAD PARA UN PROPÓSITO DETERMINADO.**
>
> Copyright (C) Microsoft. Todos los derechos reservados.

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
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
>
> Un componente [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)de contenedor siempre debe enumerar todas las direcciones URL secundarias incluso si las direcciones URL secundarias no han cambiado, ya que el indexador detecta eliminaciones a través del proceso de enumeración. Si la salida de fecha en un DIR LINKS WITH TIME indica que los datos no han cambiado, el indexador no actualiza los datos \_ \_ de esa dirección \_ URL.

 

La dirección URL física es la dirección URL que procesa **el objeto UrlAccessor.** Si el filtro no emite una propiedad DisplayUrl fácil de usar, WDS muestra la dirección URL física al usuario como parte de los resultados de la búsqueda. El esquema WDS contiene dos propiedades para controlar lo que se muestra al usuario final, como se muestra en la tabla siguiente.



| GUID                                 | PROPSPEC      | Descripción                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DisplayFolder | Ruta de acceso de carpeta mostrada al usuario en los resultados de la búsqueda |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | FolderName    | Nombre para mostrar de la carpeta primaria                   |



 

Si el código no emite displayFolder o FolderName, estos valores se calculan a partir de DisplayUrl. Las barras diagonales de la dirección URL denotan contenedores dentro del almacén o sistema de archivos.

## <a name="adding-protocol-handler-options-functionality"></a>Agregar funcionalidad de opciones de controlador de protocolos

Para que el controlador de protocolo tenga una página de inicio predeterminada (y una dirección URL del nodo de entrada), debe implementar la **interfaz ISearchProtocolOptions.** En versiones futuras de WDS, esta interfaz proporcionará enlaces al cuadro de diálogo Opciones para mejorar la experiencia del usuario. Esta interfaz proporciona la siguiente funcionalidad:

-   Determina si se cumplen los requisitos del controlador de protocolo. Por ejemplo, el almacén del controlador de protocolo puede requerir acceso a una aplicación determinada para indexar correctamente los datos de la aplicación, pero esa aplicación no está disponible.
-   Identifica los requisitos mínimos que necesita el controlador de protocolo para procesar un elemento. Los requisitos se pueden expresar en una descripción localizada y fácil de usar, como "Microsoft Outlook 2000 o superior".
-   Define las direcciones URL que el controlador de protocolo debe procesar de forma predeterminada.

### <a name="isearchprotocoloptions"></a>ISearchProtocolOptions

En la tabla siguiente se describen los métodos que debe implementar para la **interfaz ISearchProtocolOptions.**



| Método               | Descripción                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| CheckRequirements    | Determina si se cumplen los requisitos mínimos de un controlador de protocolo personalizado.                             |
| GetDefaultCrawlScope | Devuelve una lista de direcciones URL predeterminadas dentro de un almacén especificado para un controlador de protocolo personalizado.                   |
| GetRequirements      | Identifica una descripción fácil de usar y localizada de los requisitos mínimos para un controlador de protocolo personalizado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Notificación al índice de cambios](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Agregar iconos, vistas previas y menús contextuales con extensiones de shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Instalación y registro de controladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 