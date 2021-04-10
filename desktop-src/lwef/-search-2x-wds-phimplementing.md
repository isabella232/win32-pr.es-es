---
title: Implementar un controlador de protocolo para WDS
description: La creación de un controlador de protocolo implica la implementación de ISearchProtocol para administrar objetos UrlAccessor, IUrlAccessor para generar metadatos acerca de e identificar los filtros adecuados para los elementos del almacén de datos, IProtocolHandlerSite para crear instancias de un objeto SearchProtocol e identificar los filtros adecuados, y IFilterto filtrar archivos propietarios o para enumerar y filtrar archivos almacenados jerárquicamente.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149222"
---
# <a name="implementing-a-protocol-handler-for-wds"></a>Implementar un controlador de protocolo para WDS

> [!NOTE]
> Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003. En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.

La creación de un controlador de protocolo implica la implementación de [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) para administrar objetos UrlAccessor, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) para generar metadatos acerca de e identificar los filtros adecuados para los elementos del almacén de datos, IProtocolHandlerSite para crear instancias de un objeto SearchProtocol e identificar los filtros adecuados, y [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)para filtrar los archivos propietarios o para enumerar y filtrar los archivos almacenados jerárquicamente. El controlador de protocolo debe ser multiproceso.

Esta sección contiene los temas siguientes:

-   [Nota sobre las direcciones URL](#note-on-urls)
-   [Interfaces del controlador de protocolo](#protocol-handler-interfaces)
-   [IFilters para contenedores](#ifilters-for-containers)
-   [Agregar funcionalidad de opciones de controlador de protocolo](#adding-protocol-handler-options-functionality)
    -   [ISearchProtocolOptions](#isearchprotocoloptions)
-   [Temas relacionados](#related-topics)

## <a name="note-on-urls"></a>Nota sobre las direcciones URL

Microsoft Windows Desktop Search (WDS) usa las direcciones URL para identificar de forma única los elementos de un sistema de archivos, dentro de un almacén similar a la base de datos o en la Web. Una dirección URL que define un nodo de entrada se denomina página de inicio. WDS comienza en la página de inicio y rastrea de forma recursiva el almacén de datos. La estructura de direcciones URL típica es:

`protocol://host/path/name.extension`

> [!Note]
>
> Si desea agregar un nuevo almacén de datos, debe seleccionar un nombre para identificarlo que no entra en conflicto con los actuales. Se recomienda esta Convención de nomenclatura: companyName. Scheme.

 

## <a name="protocol-handler-interfaces"></a>Interfaces del controlador de protocolo

**ISearchProtocol**

La interfaz [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) invoca, inicializa y administra objetos UrlAccessor. Para obtener más información sobre la implementación de la interfaz ISearchProtocol, consulte referencia de la **interfaz ISearchProtocol**.

**IUrlAccessor**

En el caso de una dirección URL especificada, la interfaz [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) genera metadatos sobre la estructura de ubicación, así como los elementos contenidos, y enlaza esos elementos a un filtro. Un objeto SearchProtocol crea una instancia del objeto **IUrlAccessor** y lo inicializa. sin embargo, también puede implementar un método de inicialización interno para que el objeto **IUrlAccessor** pueda realizar tareas de inicialización específicas del controlador de protocolo, como la validación de la dirección URL de un elemento al que se está accediendo o la comprobación de la hora de la última modificación para determinar si un archivo se debe procesar en el rastreo actual.

> [!Note]
>
> Se omiten las horas modificadas de los directorios. El objeto [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) debe enumerar los objetos secundarios para determinar si se ha producido alguna modificación o eliminación.

 

Gran parte del diseño del objeto **UrlAccessor** depende de si la estructura es jerárquica o basada en vínculos. En el caso de los almacenes de datos jerárquicos, el objeto **UrlAccessor** debe encontrar un filtro que pueda enumerar su contenido. Otra diferencia entre los controladores de protocolos jerárquicos y basados en vínculos es el uso del método IsDirectory. En los controladores de protocolo basados en vínculos, este método debe devolver S \_ false. Los controladores de protocolo jerárquicos deben devolver los valores \_ correctos para los contenedores.

Para obtener más instrucciones sobre la implementación de una interfaz [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) , vea la referencia de la [**interfaz IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) .

**IProtocolHandlerSite**

Esta interfaz se usa para crear instancias de un objeto **SearchProtocol** y también proporciona el objeto **UrlAccessor** con un filtro adecuado para un identificador de clase especificado (CLSID).

## <a name="ifilters-for-containers"></a>IFilters para contenedores

Si va a implementar un controlador de protocolo jerárquico, debe implementar un componente de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)de contenedor que enumere las direcciones URL que representan contenedores o carpetas. El proceso de enumeración es un bucle a través de los métodos **GetChunk** y **GetValue** de la interfaz IFilter que devuelve una lista de direcciones URL que representan cada elemento del contenedor.

En primer lugar, **GetChunk** devuelve FULLPROSPEC con el conjunto de propiedades Gather \_ PROPSET y:

-   PID \_ GTHR \_ DIRLINK, la dirección URL del elemento sin la hora de la última modificación, o bien
-   PID \_ GTHR \_ DIRLINK \_ con \_ hora, la dirección URL junto con la hora de la última modificación

El GUID del conjunto de propiedades para GATHER \_ PROPSET es 0B63E343-9CCC-11D0-BCDB-00805FCCCE04. La propiedad PROPSPEC es PID \_ GTHR \_ DIRLINK = 2 o PID \_ GTHR \_ DIRLINK \_ con \_ Time = 12 decimal.

Devolver el PID \_ GTHR \_ DIRLINK con el \_ \_ tiempo es más eficaz porque el indexador puede determinar inmediatamente si el elemento debe indizarse sin llamar a los métodos ISearchProtocol->CreateUrlAccessor () y IUrlAccessor->GetLastModified ().

A continuación, **GetValue** devuelve un PROPVARIANT para la dirección URL (y la hora de la última modificación si se usa), como:

-   VT \_ LPWStr, la dirección URL del elemento secundario o
-   Vector de la dirección URL seguido de un FILETIME

En el código de ejemplo siguiente se muestra cómo compilar el PID adecuado \_ GTHR \_ DIRLINK \_ con \_ Time.

> [!Note]
>
> **ESTE CÓDIGO E INFORMACIÓN SE PROPORCIONA "TAL CUAL" SIN GARANTÍA DE NINGÚN TIPO, YA SEA EXPRESA O IMPLÍCITA, INCLUIDAS, ENTRE OTRAS, LAS GARANTÍAS IMPLÍCITAS DE COMERCIABILIDAD O IDONEIDAD PARA UN PROPÓSITO DETERMINADO.**
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
> Un componente de [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)de contenedor siempre debe enumerar todas las direcciones URL secundarias aunque no hayan cambiado las direcciones URL secundarias, ya que el indexador detecta eliminaciones a través del proceso de enumeración. Si la fecha de salida en un \_ vínculo de directorio \_ con \_ la hora indica que los datos no han cambiado, el indizador no actualiza los datos de esa dirección URL.

 

La dirección URL física es la dirección URL que procesa el objeto **UrlAccessor** . Si el filtro no emite un DisplayUrl descriptivo, WDS muestra la dirección URL física del usuario como parte de los resultados de la búsqueda. El esquema de WDS contiene dos propiedades para controlar lo que se muestra al usuario final, tal como se muestra en la tabla siguiente.



| GUID                                 | PROPSPEC      | Descripción                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DisplayFolder | Ruta de acceso de la carpeta que se muestra al usuario en los resultados de la búsqueda |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | FolderName    | Nombre para mostrar de la carpeta principal                   |



 

Si el código no emite DisplayFolder o nombreDeCarpeta, estos valores se calculan a partir de DisplayUrl. Las barras diagonales de la dirección URL indican contenedores dentro del almacén o del sistema de archivos.

## <a name="adding-protocol-handler-options-functionality"></a>Agregar funcionalidad de opciones de controlador de protocolo

Para que el controlador de protocolo tenga una página de inicio predeterminada (y una dirección URL de nodo de entrada), debe implementar la interfaz **ISearchProtocolOptions** . En versiones futuras de WDS, esta interfaz proporcionará enlaces al cuadro de diálogo Opciones para mejorar la experiencia del usuario. Esta interfaz proporciona la funcionalidad siguiente:

-   Determina si se cumplen los requisitos para el controlador de protocolo. Por ejemplo, el almacén del controlador del Protocolo puede requerir el acceso a una aplicación determinada para indizar correctamente los datos de la aplicación, pero esa aplicación no está disponible.
-   Identifica los requisitos mínimos que el controlador de protocolo necesita para procesar un elemento. Los requisitos se pueden expresar en una descripción localizada y fácil de usar, como "Microsoft Outlook 2000 o superior".
-   Define las direcciones URL que el controlador de protocolo debe procesar de forma predeterminada.

### <a name="isearchprotocoloptions"></a>ISearchProtocolOptions

En la tabla siguiente se describen los métodos que debe implementar para la interfaz **ISearchProtocolOptions** .



| Método               | Descripción                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| CheckRequirements    | Determina si se cumplen los requisitos mínimos de un controlador de protocolo personalizado.                             |
| GetDefaultCrawlScope | Devuelve una lista de direcciones URL predeterminadas dentro de un almacén especificado para un controlador de protocolo personalizado.                   |
| GetRequirements      | Identifica una descripción localizada y descriptiva de los requisitos mínimos para un controlador de protocolo personalizado. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[Notificar el índice de cambios](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Agregar iconos, vistas previas y menús contextuales con extensiones de Shell](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Instalar y registrar controladores de protocolo](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 