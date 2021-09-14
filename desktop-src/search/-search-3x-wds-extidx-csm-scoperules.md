---
description: El Administrador del ámbito de rastreo (CSM) permite definir reglas de ámbito que incluyen o excluyen direcciones URL del ámbito de rastreo Windows Search.
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: Administración de reglas de ámbito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134e4241e9dcd66e468935ae56a4029a51a96c37
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363310"
---
# <a name="managing-scope-rules"></a>Administración de reglas de ámbito

El Administrador del ámbito de rastreo (CSM) permite definir reglas de ámbito que incluyen o excluyen direcciones URL del ámbito de rastreo Windows Search.

El CSM le permite hacer lo siguiente:

-   Agregar nuevas reglas de ámbito al conjunto de reglas de trabajo
-   Eliminación de reglas de ámbito existentes
-   Enumerar reglas de ámbito predeterminadas
-   Descubra si una dirección URL determinada está incluida o excluida del ámbito de rastreo o tiene una regla de ámbito principal o secundario.

 

En esta sección se incluyen los siguientes temas:

-   [Acerca de las reglas de ámbito](#about-scope-rules)
-   [Antes de comenzar](#before-you-begin)
-   [Agregar reglas de ámbito](#adding-scope-rules)
    -   [Notas sobre las reglas de usuario](#notes-on-user-rules)
-   [Quitar reglas de ámbito](#removing-scope-rules)
-   [Revertir a las reglas predeterminadas](#reverting-to-default-rules)
-   [Enumerar reglas de ámbito](#enumerating-scope-rules)
-   [Reglas de ámbito de seguimiento](#tracing-scope-rules)
-   [Temas relacionados](#related-topics)

## <a name="about-scope-rules"></a>Acerca de las reglas de ámbito

Una regla de ámbito es una regla que incluye o excluye las direcciones URL dentro de una raíz de búsqueda para que no se rastreen e indexe. Las reglas de inclusión hacen que el indexador incluya esa dirección URL en el ámbito de scrawl y las reglas de exclusión hacen que el indexador excluya esa dirección URL (y sus secundarios) del ámbito de rastreo.

Por ejemplo, supongamos que ha instalado una nueva aplicación cuyos archivos de datos se encuentran en la carpeta WorkteamA \\ ProjectFiles en un equipo local. Supongamos que quiere que todo el contenido de la carpeta ProjectFiles esté indexado, excepto los elementos de la subcarpeta Prototipos. En esta situación, necesitará una regla de inclusión para myPH:///C: WorkteamA ProjectFiles y una regla de exclusión \\ \\ para \\ myPH:///C: \\ WorkteamA \\ \\ ProjectFiles Prototypes \\ .

Hay tres tipos de reglas, con el orden de prioridad siguiente:

1.  directiva de grupo reglas las establecen los administradores y pueden invalidar todas las demás reglas.
2.  Las reglas de usuario las establecen los usuarios que modifican el ámbito en la interfaz de usuario Windows opciones de búsqueda. Los usuarios u otras aplicaciones pueden quitar todas las reglas de usuario y revertir a las reglas predeterminadas.
3.  Normalmente, una aplicación establece reglas predeterminadas para definir un ámbito predeterminado. Por ejemplo, se pueden establecer reglas predeterminadas cuando se agrega un nuevo controlador de protocolo o contenedor al sistema.

Juntos, estos tipos  de reglas componen el conjunto de reglas de trabajo a partir del cual el Administrador del ámbito de rastreo (CSM) genera la lista completa de direcciones URL para rastrear. Aunque las reglas predeterminadas se pueden invalidar por reglas de directiva de grupo y por reglas de usuario, se mantienen en su propio conjunto de reglas predeterminado, al que puede revertir en cualquier momento. El indexador rastrea las direcciones URL del conjunto de reglas de trabajo y agrega elementos, propiedades y contenido al catálogo.

> [!Note]  
> Los usuarios con acceso a Panel de control pueden modificar las reglas a través de esa interfaz. Por lo tanto, las aplicaciones que ofrecen administración de ámbitos siempre deben obtener las reglas directamente del CSM mediante los métodos de enumeración en lugar de confiar en una copia guardada de reglas de usuario.

 

Las reglas de exclusión pueden definir direcciones URL de patrón con el carácter comodín ' '; por \* ejemplo: file:///C: \\ ProjectA \\ \* \\ . Una regla de exclusión que usa este patrón impide que el indexador rastree las carpetas del directorio ProjectA. Para obtener un ejemplo más complicado, supongamos que hay una regla de inclusión para file:///C: ProjectA y una regla de patrón de exclusión \\ \\ para file:///C: Datos de \\ \\ \* \\ ProjectA \\ \* . En este caso, el indexador rastrearía elementos en:

-   C: \\ ProjectA\\
-   C: \\ Archivos de prueba \\ **projectA versión1** \\\\
-   C: \\ Datos temporales de ProjectA versión \\ **\\ 1** \\\\

Pero el indexador no rastrearía elementos en:

-   C: \\ Datos de ProjectA versión \\ **1** \\\\

 

## <a name="before-you-begin"></a>Antes de empezar

Antes de usar cualquiera de las Administrador del ámbito de rastreo, debe realizar los siguientes pasos previos:

1.  Cree el **objeto CSearchManager** y obtenga su **interfaz ISearchManager.**
2.  Llame **a ISearchManager::GetCatalog** para "SystemIndex" para obtener una instancia de la **interfaz ISearchCatalogManager.**
3.  Llame **a ISearchCatalogManager::GetCrawlScopeManager para** obtener una instancia de la interfaz **ISearchCrawlScopeManager.**

Después de realizar cambios en el Administrador del ámbito de rastreo, debe llamar al método [**ISearchCrawlScopeManager::SaveAll.**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) Este método no toma ningún parámetro y devuelve S \_ OK si se realiza correctamente.

 

## <a name="adding-scope-rules"></a>Agregar reglas de ámbito

Las reglas de trabajo establecidas para el CSM incluyen reglas predeterminadas y de usuario, así como las reglas forzadas por la directiva de grupo. Los usuarios establecen reglas de usuario en una interfaz de usuario y las reglas predeterminadas se pueden establecer mediante cualquiera de las siguientes opciones:

-   Directivas de grupo implementadas por un administrador del sistema (no usan la [**interfaz ISearchCrawlScopeManager).**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
-   La instalación o actualización de una aplicación como Windows Search o un controlador de protocolo
-   Una aplicación de configuración para la adición de un nuevo almacén de datos o contenedor

[**ISearchCrawlScopeManager proporciona**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) dos métodos para agregar nuevas reglas de ámbito, como se describe en la tabla siguiente. Las rutas de acceso para las reglas de inclusión del sistema de archivos deben terminar con una barra diagonal inversa ' ' (por ejemplo, file:///C: archivos ) y las rutas de acceso para las reglas de exclusión deben terminar con un \\ \\ asterisco \\ (por ejemplo, file:///c: \\ archivos \\ \* ). Solo las reglas de exclusión pueden contener direcciones URL de patrón. Además, se recomienda incluir los identificadores de seguridad (SID) de los usuarios en las rutas de acceso, para mejorar la seguridad. Las rutas de acceso por usuario son más seguras, ya que las consultas se ejecutarían en un proceso por usuario, lo que garantiza que un usuario no pueda ver elementos indexados desde la bandeja de entrada de otro usuario, por ejemplo.

En la tabla siguiente se describen los métodos de la interfaz ISearchCrawlScopeManager que se usa para agregar nuevas reglas de ámbito.



| Método                                                                              | Descripción                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddUserScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | Agrega una regla para una dirección URL, según lo especificado por el usuario. Estas reglas invalidan las reglas predeterminadas. Use este método si ha implementado una interfaz de usuario que permite a los usuarios administrar sus propias reglas de ámbito y direcciones URL.                         |
| [**AddDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | Agrega una regla para una dirección URL, como especifica otra aplicación, como un controlador de protocolo. Use este método cuando haya implementado un nuevo controlador de protocolo o haya agregado un nuevo almacén de datos. Estas reglas se pueden invalidar mediante reglas de usuario. |



 

Cada método toma una dirección URL a una ubicación indexable y marcas que determinan si la dirección URL debe incluirse o excluirse. El *parámetro fFollowFlags* está reservado para su uso futuro. Cuando agrega una nueva regla de ámbito y el Administrador del ámbito de rastreo determina que la regla ya existe (en función de la dirección URL o el patrón proporcionado), el conjunto de reglas de trabajo se actualiza para que (1) la regla anterior se reemplaza por la nueva regla y (2) se quitan las reglas de usuario que la contradicen.

**Sugerencia:** Aunque la file:// se incluye de forma predeterminada en el ámbito de rastreo, archivos de programa no se indexa de forma predeterminada. Por lo tanto, las aplicaciones con datos guardados en su directorio archivos de programa deben agregar su ubicación como regla predeterminada.

### <a name="notes-on-user-rules"></a>Notas sobre las reglas de usuario

Si una nueva regla de usuario es la misma que una regla predeterminada existente, la nueva regla de usuario invalida la regla predeterminada en el conjunto de reglas de trabajo. Si la nueva regla de usuario es la misma que una regla de usuario existente, se reemplaza la regla de usuario anterior.

Establecer la marca *fOverrideChildren tiene* los siguientes resultados en el conjunto de reglas de trabajo:

-   **TRUE** da como resultado la eliminación de todas las reglas secundarias del conjunto de reglas de trabajo (reglas de usuario y reglas predeterminadas).
-   False da como resultado volver a agregar a las reglas de trabajo para establecer todas las reglas predeterminadas que son elementos secundarios de la nueva regla de usuario. Si una regla predeterminada secundaria es una inclusión y la nueva regla de usuario es una exclusión, la regla predeterminada cambia a una regla de usuario de inclusión.

 

## <a name="removing-scope-rules"></a>Quitar reglas de ámbito

Puede usar la interfaz [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para quitar una regla de ámbito del conjunto de reglas de trabajo. Esta interfaz proporciona los dos métodos siguientes para quitar reglas de ámbito.



| Método                                                                                    | Descripción                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | Quita una regla de usuario para una dirección URL especificada del conjunto de reglas de trabajo. Si la regla de usuario es un duplicado de o invalida una regla predeterminada, la regla predeterminada permanece en el conjunto de reglas de trabajo.                  |
| [**RemoveDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | Quita una regla predeterminada para una dirección URL especificada del conjunto de reglas de trabajo y del conjunto de reglas predeterminado. Después de llamar a este método, no puede revertir a esta regla predeterminada mediante RevertToDefaultScopes. |



 

Cada método toma una dirección URL y una marca que indica si la regla que se va a quitar es una regla de inclusión o exclusión. Estos métodos devuelven un error si no se encuentra una regla con esa dirección URL y la marca de inclusión o exclusión.

**Sugerencia:** Si desea quitar completamente un ámbito del ámbito de rastreo, use el método [**RemoveRoot,**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) que quita la raíz de búsqueda y todas las reglas de ámbito asociadas. Esto durante la desinstalación, por ejemplo, se considera un procedimiento recomendado.

También es posible quitar todas las invalidaciones de conjunto de usuarios de una raíz de búsqueda y revertir a la raíz de búsqueda original y a las reglas de ámbito predeterminadas. Para obtener más información, consulte la sección siguiente.

> [!Note]  
> En Windows Vista, si los usuarios se quitan a través de perfiles de usuario en Panel de control, CSM quita todas las reglas y raíces que incluyen su SID y quita sus elementos indexados del catálogo. En Windows XP, debe quitar manualmente las raíces y las reglas de los usuarios.

 

 

## <a name="reverting-to-default-rules"></a>Revertir a las reglas predeterminadas

Al revertir a las reglas predeterminadas, se quitan todas las reglas de usuario de una dirección URL o raíz y se restauran todas las reglas predeterminadas al conjunto de reglas de trabajo. Sin embargo, no quita las reglas establecidas por la directiva de grupo. El [**método RevertToDefaultScopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes) no toma ningún parámetro y devuelve un código de error si no puede revertir a las reglas predeterminadas.

 

## <a name="enumerating-scope-rules"></a>Enumerar reglas de ámbito

El CSM enumera las reglas de ámbito mediante una interfaz de enumerador de estilo COM estándar, [**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) . Puede usar esta interfaz para enumerar las reglas de ámbito para varios propósitos. Por ejemplo, es posible que desee mostrar todo el conjunto de reglas de trabajo en una interfaz de usuario o detectar si una regla o el elemento secundario de una regla ya está en el ámbito de rastreo.

 

## <a name="tracing-scope-rules"></a>Reglas de ámbito de seguimiento

El CSM también le permite determinar si se incluye una dirección URL especificada en el ámbito de rastreo y si tiene una regla de ámbito principal o secundaria. También puede averiguar por qué se incluye o excluye una dirección URL del ámbito de rastreo. Estos métodos no están diseñados para usarse con direcciones URL de patrón.

En la tabla siguiente se describen los métodos de [**ISearchCrawlScopeManager usados**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para agregar nuevas reglas de ámbito.



| Método                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentScopeVersionId**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | Obtiene el identificador de versión de la dirección URL de inclusión primaria. Puede usar este método para ver si el ámbito primario ha cambiado desde la última vez que lo comprobó.<br/> Ejemplo: si una aplicación de correo usa notificaciones administradas por el proveedor, podría obtener la versión del ámbito primario antes de cerrarse y comprobar la versión de nuevo cuando se abra. A continuación, la aplicación puede determinar si necesita insertar un nuevo conjunto de notificaciones en el indexador.<br/> |
| [**HasChildScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | Devuelve **TRUE** si la dirección URL especificada tiene una regla secundaria (una regla que se aplica a un elemento secundario en cualquier nivel dentro de su jerarquía de direcciones URL). <br/> Ejemplo: si la dirección URL es file:///C: Carpeta , este método devuelve TRUE si el CSM tiene una regla de ámbito específicamente \\ \\ para file:///C: Subcarpeta de carpeta  \\ \\ \\ .<br/>                                                                                                                                              |
| [**HasParentScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | Devuelve **TRUE** si la dirección URL especificada tiene una regla primaria (una regla que se aplica a un elemento primario en cualquier nivel de la jerarquía de direcciones URL).<br/> Ejemplo: si la dirección URL es file:///C: Subcarpeta de carpeta, este método devuelve TRUE si el CSM tiene una regla de ámbito específicamente \\ \\ para file:///C: Carpeta  \\ \\ .<br/>                                                                                                                                                   |
| [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | Devuelve **TRUE** si la dirección URL especificada se incluye en el ámbito de rastreo.                                                                                                                                                                                                                                                                                                                                                                                  |
| [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | Devuelve un valor de la enumeración [**CLUSION \_ REASON**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) que explica por qué la dirección URL se incluye o se excluye del ámbito de rastreo y recupera el valor **TRUE** si la dirección URL se incluye en el ámbito de rastreo. Este método puede ayudarle a identificar conflictos en el conjunto de reglas de trabajo.                                                                                                                                       |



 

 

> [!Note]  
> Los [**métodos IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope) e [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex) determinan si la dirección URL se rastreará basándose únicamente en las reglas del CSM. Puede haber otras razones por las que no se rastree una dirección URL, como el bit FANCI que se establece (es decir, un usuario no ha permitido la indexación rápida en el cuadro de diálogo Propiedad de la carpeta).

 

Si cree que se debe excluir una ruta de acceso de archivo, pero aparece como incluida, asegúrese de que las reglas de exclusión terminen con " &lt; ruta &gt; \\ \* de acceso ". Si cree que se debe incluir un archivo o una ruta de acceso de archivo, pero no lo está, asegúrese de comprobar la configuración de bits FANCI para el archivo o la ruta de acceso. Para ello, haga clic con el botón derecho en la ruta de acceso del archivo o archivo y seleccione Propiedades y, a continuación, asegúrese de que la casilla Para búsqueda rápida, permitir que **Indexing Service** indexe esta carpeta está activada. Si la ruta de acceso del archivo o archivo no está marcada para la indexación aquí, no se indexará aunque esté en una regla de inclusión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

**Referencia**
</dt> <dt>

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)
</dt> <dt>

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)
</dt> <dt>

[**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)
</dt> <dt>

[**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Administración de raíces de búsqueda](-search-3x-wds-extidx-csm-searchroots.md)
</dt> </dl>

 

 




