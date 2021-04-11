---
description: El administrador de ámbito de rastreo (CSM) permite agregar y quitar raíces de búsqueda de los almacenes de datos en el ámbito de rastreo de Windows Search.
ms.assetid: 0f1ff41f-7c4c-4516-bb55-bf09a8f2f3bc
title: Administración de raíces de búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbdd63e5e71cd18d3028c6d08019890f90c0228a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275273"
---
# <a name="managing-search-roots"></a>Administración de raíces de búsqueda

El administrador de ámbito de rastreo (CSM) permite agregar y quitar raíces de búsqueda de los almacenes de datos en el ámbito de rastreo de Windows Search.

En esta sección se incluyen los siguientes temas:

-   [Acerca de las raíces de búsqueda](#about-search-roots)
-   [Antes de comenzar](#before-you-begin)
-   [Windows 7: nueva API del administrador de ámbito de rastreo](#windows-7-new-crawl-scope-manager-api)
-   [Agregar raíces al ámbito de rastreo](#adding-roots-to-the-crawl-scope)
-   [Quitar raíces del ámbito de rastreo](#removing-roots-from-the-crawl-scope)
-   [Enumerar raíces en el ámbito de rastreo](#enumerating-roots-in-the-crawl-scope)
-   [Temas relacionados](#related-topics)

 

## <a name="about-search-roots"></a>Acerca de las raíces de búsqueda

Una raíz de búsqueda define la base de un espacio de nombres de Shell donde se pueden incluir o excluir ámbitos específicos, y suele ser el contenedor de nivel superior de un protocolo que se puede enumerar. No especifica qué partes de este almacén deben o no deben indexarse; simplemente indica que existe un almacén de contenido y está asociado a un controlador de protocolo registrado. La sintaxis para identificar una dirección URL raíz de búsqueda incluye el protocolo, el identificador de seguridad del usuario o el almacén, la ruta de acceso y, opcionalmente, un elemento específico (como un archivo). En los siguientes ejemplos se muestran dos formas de la sintaxis de una raíz de búsqueda.


```
<protocol>://<store or SID>\<path>\[item]
or
<protocol>://<store or SID>/<path>/[item]
```



El <protocol> segmento debe ir seguido de dos (2) barras diagonales ('/') a menos que sea el archivo: Protocolo, que requiere tres barras diagonales (File:///). El <site or SID> segmento representa un almacén de contenido o un identificador de seguridad de usuario si la raíz de búsqueda está pensada para ser específica del usuario. El <path> segmento es un conjunto de contenedores, como directorios o carpetas, y puede incluir el carácter comodín " \* ". A la clase <item> Segment es opcional y también puede incluir el carácter comodín ' \* '. Si no incluye un elemento, asegúrese de terminar el segmento de ruta de acceso con una barra diagonal o el indexador supondrá que el último subcontenedor es un elemento.

Por ejemplo, supongamos que ha implementado un controlador de protocolo (myPH) para controlar los archivos de tipo \* . myext para una aplicación personalizada. Todos estos archivos se ubicarán en la carpeta WorkteamA \\ ProjectFiles en un equipo local. La raíz de búsqueda de puede tener el siguiente aspecto:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles\\

Supongamos que está planeando incluir todos los archivos. myext, pero nada más de ese contenedor en el índice. La raíz de búsqueda de puede tener el siguiente aspecto:

-   myPH:///C: \\ WorkteamA \\ ProjectFiles \\ \* . myext.

Los patrones de caracteres comodín definen las direcciones URL mediante el carácter comodín ' \* ' y se consideran un patrón en lugar de una dirección URL, pero la terminología se suele usar indistintamente. Por ejemplo, File:///C: \\ Projecta \\ \* \\ Data \\ coincidiría con las siguientes direcciones URL:

-   C: \\ datos de Projecta \\ **version1** \\\\
-   C: \\ datos de la \\ **version2** de proyecto \\\\

Pero ese patrón no coincidiría con esta dirección URL:

-   C: \\ \\ **datos \\ temporales de version1** \\\\

Debe crear nuevas raíces de búsqueda para los contenedores que no estén ya en el ámbito de rastreo del indexador. Si la ruta de acceso C: \\ ParentScope ya está incluida en el ámbito de rastreo, no es necesario agregar una nueva raíz de búsqueda para C: \\ ParentScope \\ ChildScope a menos que sepa que el ámbito secundario se excluyó previamente.

La interfaz de usuario para establecer las opciones de Windows Search muestra las raíces de búsqueda a los usuarios para que puedan refinar las reglas de ámbito para sus búsquedas. Como parte del proceso de instalación del controlador de protocolo personalizado, el contenedor o la aplicación, puede definir un ámbito de rastreo predeterminado, con reglas de inclusión y exclusión. Estas reglas se presentan a los usuarios finales como ubicaciones. Los usuarios pueden navegar dentro de los subdirectorios de la raíz de búsqueda predefinida y seleccionar las que deseen incluir en las búsquedas o borrar las que deseen excluir.

 

## <a name="before-you-begin"></a>Antes de empezar

Para poder usar cualquiera de las interfaces del administrador de ámbito de rastreo (CSM), debe realizar los siguientes pasos de requisitos previos:

1.  Cree el objeto **CrawlSearchManager** y obtenga su interfaz [**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) .
2.  Llame a [**ISearchManager:: GetCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog) para "SystemIndex" para obtener una instancia de una interfaz [**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) .
3.  Llame a [**ISearchCatalogManager:: GetCrawlScopeManager**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getcrawlscopemanager) para obtener una instancia de la interfaz [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) .

Después de realizar cambios en el administrador de ámbito de rastreo (CSM), debe llamar a [**ISearchCrawlScopeManager:: SAVEALL**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall). Este método no toma ningún parámetro y devuelve si es \_ correcto.

 

## <a name="windows-7-new-crawl-scope-manager-api"></a>Windows 7: nueva API del administrador de ámbito de rastreo

En **Windows 7 y versiones posteriores**, [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) extiende la funcionalidad de la interfaz [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) . El método [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) obtiene la versión del administrador de ámbito de rastreo (CSM), que informa a los clientes si el estado de CSM ha cambiado. **ISearchCrawlScopeManager2:: GetVersion** no produce una llamada entre procesos. Si la función se ejecuta correctamente, el puntero que se devuelve sigue siendo válido hasta que el cliente llama a **UnmapViewOfFile** en el puntero y **CloseHandle** en el identificador devuelto.

 

## <a name="adding-roots-to-the-crawl-scope"></a>Agregar raíces al ámbito de rastreo

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) indica al motor de búsqueda acerca de los contenedores que se van a rastrear o ver, y los elementos de esos contenedores que se van a incluir o excluir. Para agregar una nueva raíz de búsqueda, cree una instancia de un objeto [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot) , establezca los atributos raíz y, después, llame a [**ISearchCrawlScopeManager:: AddRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-addroot) y pásele un puntero al objeto **ISearchRoot** . La dirección URL raíz de búsqueda tiene el mismo formato que la raíz de búsqueda que se ha descrito anteriormente.

En la tabla siguiente se describen los métodos Put correspondientes para [**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot); los otros métodos put de la interfaz no se usan actualmente en Windows Search. Se recomienda incluir los identificadores de seguridad (SID) de los usuarios en todas las raíces para mejorar la seguridad. Las raíces por usuario son más seguras a medida que las consultas se ejecutan en un proceso por usuario, lo que garantiza que un usuario no pueda ver los elementos indizados desde la bandeja de entrada de otro usuario, por ejemplo.



| Método                     | Descripción                                                                                                                                                                                         |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Put \_ ProvidesNotifications | Establézcalo en **true** si un controlador de protocolo u otra aplicación notificará al motor de búsqueda los cambios en las direcciones URL en la raíz de búsqueda. La notificación indica que las direcciones URL deben reindizarse. |
| Put \_ RootURL               | Establece la dirección URL raíz de la búsqueda actual. La dirección URL toma el formulario raíz de búsqueda descrito anteriormente.                                                                                                      |



 

 

De forma predeterminada, el indexador no rastrea un ámbito cuando se agrega una raíz de búsqueda. También debe agregar una regla de inclusión para la raíz. Si desea agregar una raíz específica del usuario para una aplicación, esa aplicación debe agregar las raíces adecuadas para los nuevos usuarios cuando se inicie la aplicación.

Para agregar las raíces adecuadas para los nuevos usuarios:

1.  Obtiene el SID del usuario.
2.  Enumerar todas las raíces para comprobar si existe una para este SID.
3.  Agregue una nueva raíz, utilizando el SID, si es necesario.

 

## <a name="removing-roots-from-the-crawl-scope"></a>Quitar raíces del ámbito de rastreo

Puede usar [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para quitar una raíz del ámbito de rastreo cuando ya no desee que esta dirección URL se indexe. Al quitar una raíz también se eliminan todas las reglas de ámbito de esa dirección URL. Por ejemplo, supongamos que desea desinstalar un almacén de contenido o su controlador de protocolo de un sistema. Puede desinstalar la aplicación, quitar todos los datos y, a continuación, quitar la raíz de búsqueda del ámbito de rastreo, y el administrador del ámbito de rastreo quitará la raíz y todas las reglas de ámbito asociadas a la raíz.

Para quitar una raíz de búsqueda existente, llame a [**ISearchCrawlScopeManager:: RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) con la raíz de búsqueda que desea quitar. La dirección URL raíz de búsqueda tiene el mismo formato que la raíz de búsqueda que se ha descrito anteriormente. Este método devuelve S \_ false si no se encuentra la raíz y un código de error si se produjo un error al quitar una raíz encontrada.

Al quitar una raíz de búsqueda, también se quita la dirección URL de la interfaz de usuario para las opciones de búsqueda de Windows, por lo que es posible que los usuarios no puedan volver a agregar el contenedor o la ubicación mediante la interfaz de usuario. También es posible quitar todas las invalidaciones definidas por el usuario de una raíz de búsqueda y volver a las reglas de ámbito y raíz de búsqueda originales. Para obtener más información, consulte [Administración de reglas de ámbito](-search-3x-wds-extidx-csm-scoperules.md).

> [!Note]  
> En Windows Vista, si los usuarios se quitan a través de perfiles de usuario en el panel de control, CSM quita todas las reglas y raíces con su SID y quita los elementos indexados del catálogo. En Windows XP, debe quitar manualmente las raíces y reglas de los usuarios.

 

 

## <a name="enumerating-roots-in-the-crawl-scope"></a>Enumerar raíces en el ámbito de rastreo

CSM enumera las raíces de búsqueda mediante una interfaz de enumerador de estilo COM estándar, [**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots). Puede usar esta interfaz para enumerar las raíces de búsqueda de una serie de propósitos. Por ejemplo, puede que desee mostrar el ámbito de rastreo completo en una interfaz de usuario o detectar si una raíz determinada o el elemento secundario de una raíz ya está en el ámbito de rastreo.

 

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

**Vista**
</dt> <dt>

[Usar el administrador de ámbito de rastreo](-search-3x-wds-extidx-csm.md)
</dt> <dt>

[Administrar reglas de ámbito](-search-3x-wds-extidx-csm-scoperules.md)
</dt> </dl>

 

 



