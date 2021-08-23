---
description: El Administrador del ámbito de rastreo (CSM) le permite agregar y quitar raíces de búsqueda de los almacenes de datos hacia y desde el ámbito de rastreo de Windows Search.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Administración de raíces de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758d3c10a4c69f336202274cd1fb40528848b0ddb431fd58646cf700d2b2d736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119095292"
---
# <a name="managing-search-roots"></a>Administración de raíces de búsqueda

El Administrador del ámbito de rastreo (CSM) le permite agregar y quitar raíces de búsqueda de los almacenes de datos hacia y desde el ámbito de rastreo de Windows Search.

En esta sección se incluyen los siguientes temas:

-   [Acerca de las raíces de búsqueda](#about-search-roots)
-   [Antes de comenzar](#before-you-begin)
-   [Windows 7: Nueva API de Administrador del ámbito de rastreo](#windows-7-new-crawl-scope-manager-api)
-   [Agregar raíces al ámbito de rastreo](#adding-roots-to-the-crawl-scope)
-   [Quitar raíces del ámbito de rastreo](#removing-roots-from-the-crawl-scope)
-   [Enumerar raíces en el ámbito de rastreo](#enumerating-roots-in-the-crawl-scope)
-   [Temas relacionados](#related-topics)

 

## <a name="about-search-roots"></a>Acerca de las raíces de búsqueda

Una raíz de búsqueda define la base de un espacio de nombres de Shell donde se podrían incluir o excluir ámbitos específicos, y suele ser el contenedor de nivel superior de un protocolo que se puede enumerar. No especifica qué partes de este almacén se deben indexar o no; simplemente indica que existe un almacén de contenido y está asociado a un controlador de protocolo registrado. La sintaxis para identificar una dirección URL raíz de búsqueda incluye el protocolo, el identificador de seguridad del almacén o del usuario, la ruta de acceso y, opcionalmente, un elemento específico (como un archivo). En los ejemplos siguientes se muestran dos formas de sintaxis para una raíz de búsqueda.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



El segmento debe ir seguido de dos (2) barras diagonales ('/') a menos que sea el archivo: protocolo, que requiere tres barras <protocol> diagonales (file:///). El segmento representa un almacén de contenido o un identificador de seguridad de usuario si la raíz de búsqueda está pensada para <site or SID> ser específica del usuario. El <path> segmento es un conjunto de contenedores, como directorios o carpetas, y puede incluir el carácter comodín ' \* '. A la clase <item> segment es opcional y también puede incluir el carácter comodín ' \* '. Si no incluye un elemento, asegúrese de finalizar el segmento de ruta de acceso con una barra diagonal o el indexador asumirá que el último subcontenedor es un elemento.

Por ejemplo, supongamos que ha implementado un controlador de protocolo (myPH) para controlar archivos de tipo \* .myext para una aplicación personalizada. Todos estos archivos se ubicarán en la carpeta WorkteamA \\ ProjectFiles en un equipo local. La raíz de búsqueda de que podría tener este aspecto:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles\\

Supongamos que planea incluir todos los archivos .myext, pero nada más de ese contenedor en el índice. La raíz de búsqueda de que podría tener este aspecto:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles \\ \* .myext.

Los patrones de caracteres comodín definen direcciones URL mediante el carácter comodín ' ' y se consideran un patrón en lugar de una dirección URL, pero la terminología se suele usar \* indistintamente. Por ejemplo, file:///C: \\ Los datos de ProjectA \\ \* \\ \\ coincidirían con las direcciones URL siguientes:

-   C: Datos \\ de ProjectA \\ **versión 1** \\\\
-   C: Datos \\ de ProjectA \\ **versión 2** \\\\

Pero ese patrón no coincidiría con esta dirección URL:

-   C: Datos \\ temporales de ProjectA \\ **versión 1 \\** \\\\

Debe crear nuevas raíces de búsqueda para contenedores que aún no están en el ámbito de rastreo del indexador. Si la ruta de acceso C: ParentScope ya está incluida en el ámbito de rastreo, no es necesario agregar una nueva raíz de búsqueda para \\ C: ParentScope ChildScope a menos que sepa que el ámbito secundario se excluyó \\ \\ anteriormente.

La interfaz de usuario para configurar Windows search muestra raíces de búsqueda a los usuarios para que puedan refinar las reglas de ámbito de sus búsquedas. Como parte del proceso de instalación para el controlador de protocolo personalizado, el contenedor o la aplicación, puede definir un ámbito de rastreo predeterminado, con reglas de inclusión y exclusión. Estas reglas se presentan a los usuarios finales como ubicaciones. Los usuarios pueden navegar por los subdirectorios de la raíz de búsqueda predefinida y seleccionar los que quieren incluir en las búsquedas o borrar los que quieren excluir.

 

## <a name="before-you-begin"></a>Antes de empezar

Para poder usar cualquiera de las interfaces Administrador del ámbito de rastreo (CSM), debe realizar los siguientes pasos de requisitos previos:

1.  Cree el **objeto CrawlSearchManager** y obtenga su [**interfaz ISearchManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)
2.  Llame [**a ISearchManager::GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) para "SystemIndex" para obtener una instancia de una [**interfaz ISearchCatalogManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)
3.  Llame [**a ISearchCatalogManager::GetCrawlScopeManager para**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) obtener una instancia de la interfaz [**ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

Después de realizar cambios en el Administrador del ámbito de rastreo (CSM), debe llamar a [**ISearchCrawlScopeManager::SaveAll**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall). Este método no toma ningún parámetro y devuelve S \_ OK en caso de éxito.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7: Nueva API de Administrador del ámbito de rastreo

En **Windows 7 y** versiones posteriores, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) amplía la funcionalidad de la interfaz [**ISearchCrawlScopeManager.**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) El [**método ISearchCrawlScopeManager2::GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) obtiene la versión Administrador del ámbito de rastreo (CSM), que informa a los clientes si el estado del CSM ha cambiado. **ISearchCrawlScopeManager2::GetVersion** no da como resultado una llamada entre procesos. Si la función se realiza correctamente, el puntero que se devuelve sigue siendo válido hasta que el cliente llama a **UnmapViewOfFile** en el puntero y **CloseHandle** en el identificador devuelto.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Agregar raíces al ámbito de rastreo

[**ISearchCrawlScopeManager indica**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) al motor de búsqueda que los contenedores se rastreen o observen, así como los elementos de esos contenedores que se deben incluir o excluir. Para agregar una nueva raíz de búsqueda, cree una instancia de un objeto [**ISearchRoot,**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) establezca los atributos raíz y, a continuación, llame a [**ISearchCrawlScopeManager::AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) y pásallo un puntero al objeto **ISearchRoot.** La dirección URL raíz de búsqueda tiene la misma forma que la raíz de búsqueda descrita anteriormente.

En la tabla siguiente se describen los métodos put pertinentes para [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); Los otros métodos put de la interfaz no se usan actualmente en Windows Search. Se recomienda incluir los identificadores de seguridad (SID) de los usuarios en todas las raíces para mejorar la seguridad. Las raíces por usuario son más seguras a medida que las consultas se ejecutan en un proceso por usuario, lo que garantiza que un usuario no pueda ver los elementos indexados desde la bandeja de entrada de otro usuario, por ejemplo.



| Método                     | Descripción                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| put \_ ProvidesNotifications | Establezca en **TRUE si** un controlador de protocolo u otra aplicación notificará al motor de búsqueda los cambios en las direcciones URL de la raíz de búsqueda. La notificación indica que las direcciones URL deben volver a indexarse. |
| put \_ RootURL               | Establece la dirección URL raíz de la búsqueda actual. La dirección URL toma el formulario raíz de búsqueda descrito anteriormente.                                                                                                      |



 

 

De forma predeterminada, el indexador no rastrea un ámbito al agregar una raíz de búsqueda. También debe agregar una regla de include para la raíz. Si desea agregar una raíz específica del usuario para una aplicación, esa aplicación debe agregar las raíces adecuadas para los nuevos usuarios cuando se inicie la aplicación.

Para agregar las raíces adecuadas para los nuevos usuarios:

1.  Obtenga el SID del usuario.
2.  Enumera todas las raíces para comprobar si existe una para este SID.
3.  Agregue una nueva raíz mediante el SID, si es necesario.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Quitar raíces del ámbito de rastreo

Puede usar [**ISearchCrawlScopeManager para**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) quitar una raíz del ámbito de rastreo cuando ya no quiera indexar esa dirección URL. Al quitar una raíz también se eliminan todas las reglas de ámbito de esa dirección URL. Por ejemplo, supongamos que quiere desinstalar un almacén de contenido o su controlador de protocolo de un sistema. Puede desinstalar la aplicación, quitar todos los datos y, a continuación, quitar la raíz de búsqueda del ámbito de rastreo, y el Administrador del ámbito de rastreo quitará la raíz y todas las reglas de ámbito asociadas a la raíz.

Para quitar una raíz de búsqueda existente, llame a [**ISearchCrawlScopeManager::RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) con la raíz de búsqueda que desea quitar. La dirección URL raíz de búsqueda tiene la misma forma que la raíz de búsqueda descrita anteriormente. Este método devuelve S FALSE si no se encuentra la raíz y un código de error si se produjo un error al quitar una raíz \_ que se encontró.

Al quitar una raíz de búsqueda también se quita la dirección URL de la interfaz de usuario para las opciones de búsqueda de Windows, por lo que es posible que los usuarios no puedan volver a agregar ese contenedor o ubicación mediante la interfaz de usuario. También es posible quitar todas las invalidaciones de conjunto de usuarios de una raíz de búsqueda y revertir a las reglas de ámbito y raíz de búsqueda originales. Para obtener más información, vea [Administración de reglas de ámbito.](-search-3x-wds-extidx-csm-scoperules.md)

> [!Note]  
> En Windows Vista, si los usuarios se quitan a través de perfiles de usuario en Panel de control, CSM quita todas las reglas y raíces con su SID y quita sus elementos indexados del catálogo. En Windows XP, debe quitar manualmente las raíces y las reglas de los usuarios.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Enumerar raíces en el ámbito de rastreo

El CSM enumera las raíces de búsqueda mediante una interfaz de enumerador de estilo COM estándar, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots). Puede usar esta interfaz para enumerar las raíces de búsqueda para una serie de propósitos. Por ejemplo, puede que desee mostrar todo el ámbito de rastreo en una interfaz de usuario o detectar si una raíz determinada o el elemento secundario de una raíz ya está en el ámbito de rastreo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)
</dt> <dt>

[**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Uso del Administrador del ámbito de rastreo](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Administración de reglas de ámbito](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



