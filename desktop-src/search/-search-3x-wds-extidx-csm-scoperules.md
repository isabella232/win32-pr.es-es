---
description: El administrador de ámbito de rastreo (CSM) permite definir reglas de ámbito que incluyen o excluyen direcciones URL del ámbito de rastreo de Windows Search.
ms.assetid: 132a55f9-680d-438e-b983-f5ce4cf66a41
title: Administrar reglas de ámbito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20d45199726cfe36dc1c4936e9ac7699a288c3ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153994"
---
# <a name="managing-scope-rules"></a>Administrar reglas de ámbito

El administrador de ámbito de rastreo (CSM) permite definir reglas de ámbito que incluyen o excluyen direcciones URL del ámbito de rastreo de Windows Search.

CSM le permite hacer lo siguiente:

-   Agregar nuevas reglas de ámbito al conjunto de reglas de trabajo
-   Quitar las reglas de ámbito existentes
-   Enumerar reglas de ámbito predeterminadas
-   Detectar si una dirección URL determinada está incluida o excluida del ámbito de rastreo o tiene una regla de ámbito primario o secundario

 

En esta sección se incluyen los siguientes temas:

-   [Acerca de las reglas de ámbito](#about-scope-rules)
-   [Antes de comenzar](#before-you-begin)
-   [Agregar reglas de ámbito](#adding-scope-rules)
    -   [Notas sobre las reglas de usuario](#notes-on-user-rules)
-   [Quitar reglas de ámbito](#removing-scope-rules)
-   [Revertir a las reglas predeterminadas](#reverting-to-default-rules)
-   [Enumerar reglas de ámbito](#enumerating-scope-rules)
-   [Seguimiento de reglas de ámbito](#tracing-scope-rules)
-   [Temas relacionados](#related-topics)

## <a name="about-scope-rules"></a>Acerca de las reglas de ámbito

Una regla de ámbito es una regla que incluye o excluye las direcciones URL de una raíz de búsqueda que se rastrean e indexan. Las reglas de inclusión hacen que el indexador incluya esa dirección URL en el ámbito Scrawl y las reglas de exclusión hacen que el indexador excluya esa dirección URL (y sus elementos secundarios) del ámbito de rastreo.

Por ejemplo, supongamos que ha instalado una nueva aplicación cuyos archivos de datos se encuentran en la carpeta WorkteamA \\ ProjectFiles en un equipo local. Supongamos que desea indizar todo el contenido de la carpeta ProjectFiles, excepto los elementos de los prototipos de la subcarpeta. En esta situación, necesitaría una regla de inclusión para myPH:///C: \\ WorkteamA \\ ProjectFiles \\ y una regla de exclusión para los \\ prototipos myPH:///C: WorkteamA \\ ProjectFiles \\ \\ .

Hay tres tipos de reglas, con el siguiente orden de prioridad:

1.  Los administradores establecen las reglas de directiva de grupo y pueden invalidar todas las demás reglas.
2.  Las reglas de usuario las establecen los usuarios que modifican el ámbito en la interfaz de usuario de opciones de búsqueda de Windows. Los usuarios u otras aplicaciones pueden quitar todas las reglas de usuario y volver a las reglas predeterminadas.
3.  Normalmente, las reglas predeterminadas se establecen en una aplicación para definir un ámbito predeterminado. Por ejemplo, las reglas predeterminadas se pueden establecer cuando se agrega al sistema un nuevo contenedor o controlador de protocolo.

Juntos, estos tipos de reglas constituyen el *conjunto de reglas de trabajo* desde el que el administrador de ámbito de rastreo (CSM) genera la lista completa de direcciones URL que se van a rastrear. Aunque las reglas predeterminadas pueden reemplazarse por las reglas de directiva de grupo y por las reglas de usuario, se mantienen en su propio conjunto de reglas predeterminado, al que se puede revertir en cualquier momento. El indexador rastrea las direcciones URL del conjunto de reglas de trabajo y agrega elementos, propiedades y contenido al catálogo.

> [!Note]  
> Los usuarios con acceso al panel de control pueden modificar las reglas a través de esa interfaz. Por lo tanto, las aplicaciones que ofrecen la administración de ámbitos siempre deben obtener las reglas directamente de CSM mediante los métodos de enumeración en lugar de depender de una copia guardada de reglas de usuario.

 

Las reglas de exclusión pueden definir direcciones URL de patrón con el carácter comodín ' \* '; por ejemplo: file:///C: \\ Projecta \\ \* \\ . Una regla de exclusión que usa este patrón evita que el indexador rastree las carpetas del directorio Projecta. Para un ejemplo más complicado, supongamos que hay una regla de inclusión para file:///C: \\ Projecta \\ y una regla de patrón de exclusión para file:///C: \\ Projecta \\ \* \\ Data \\ \* . En este caso, el indizador rastrearía los elementos de:

-   C: \\ proyectoa\\
-   C: prueba de prueba de \\ Projecta \\ **version1** \\\\
-   C: \\ \\ **datos \\ temporales de version1** \\\\

Pero el indizador no rastrearía los elementos de:

-   C: \\ datos de Projecta \\ **version1** \\\\

 

## <a name="before-you-begin"></a>Antes de empezar

Antes de usar cualquiera de las interfaces del administrador de ámbito de rastreo, debe realizar los siguientes pasos de requisitos previos:

1.  Cree el objeto **CSearchManager** y obtenga su interfaz **ISearchManager** .
2.  Llame a **ISearchManager:: GetCatalog** para "SystemIndex" para obtener una instancia de la interfaz **ISearchCatalogManager** .
3.  Llame a **ISearchCatalogManager:: GetCrawlScopeManager** para obtener una instancia de la interfaz **ISearchCrawlScopeManager** .

Después de realizar cambios en el administrador de ámbito de rastreo, debe llamar al método [**ISearchCrawlScopeManager:: SAVEALL**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-saveall) . Este método no toma ningún parámetro y devuelve si es \_ correcto.

 

## <a name="adding-scope-rules"></a>Agregar reglas de ámbito

Las reglas de trabajo establecidas para CSM incluyen reglas predeterminadas y de usuario, así como cualquier regla forzada por la Directiva de grupo. Los usuarios configuran las reglas de usuario en una interfaz de usuario y las reglas predeterminadas se pueden establecer de una de las siguientes opciones:

-   Directivas de grupo implementadas por un administrador del sistema (no usan la interfaz [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) ).
-   Instalación o actualización de una aplicación como Windows Search o un controlador de protocolo
-   Una aplicación de instalación para agregar un nuevo almacén de datos o contenedor

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) proporciona dos métodos para agregar nuevas reglas de ámbito, como se describe en la tabla siguiente. Las rutas de acceso de las reglas de inclusión del sistema de archivos deben terminar con una barra diagonal inversa ' \\ ' (por ejemplo, File:///C: \\ files \\ ) y las rutas de acceso de las reglas de exclusión deben terminar con un asterisco (por ejemplo, File:///c: \\ files \\ \* ). Solo las reglas de exclusión pueden contener direcciones URL de patrón. Además, se recomienda incluir los identificadores de seguridad (SID) de los usuarios en las rutas de acceso para mejorar la seguridad. Las rutas de acceso por usuario son más seguras, ya que las consultas se ejecutarán en un proceso por usuario, asegurándose de que un usuario no pueda ver los elementos indizados desde la bandeja de entrada de otro usuario, por ejemplo.

En la tabla siguiente se describen los métodos de la interfaz ISearchCrawlScopeManager que se usan para agregar nuevas reglas de ámbito.



| Método                                                                              | Descripción                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddUserScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adduserscoperule)       | Agrega una regla para una dirección URL, según lo especificado por el usuario. Estas reglas invalidan las reglas predeterminadas. Use este método si ha implementado una interfaz de usuario que permite a los usuarios administrar sus propias reglas de ámbito y direcciones URL.                         |
| [**AddDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-adddefaultscoperule) | Agrega una regla para una dirección URL, tal como la especifica otra aplicación como un controlador de protocolo. Use este método cuando haya implementado un nuevo controlador de protocolo o agregado un nuevo almacén de datos. Estas reglas pueden reemplazarse por las reglas de usuario. |



 

Cada método toma una dirección URL a una ubicación Indizable y marcas que determinan si la dirección URL se debe incluir o excluir. El parámetro *fFollowFlags* se reserva para uso futuro. Cuando se agrega una nueva regla de ámbito y el administrador de ámbito de rastreo determina que la regla ya existe (en función de la dirección URL o el patrón proporcionado), el conjunto de reglas de trabajo se actualiza de modo que (1) la regla antigua se reemplaza por la nueva regla y (2) se quitan las reglas de usuario que contradicen.

**Sugerencia:** Aunque la raíz file://se incluye de forma predeterminada en el ámbito de rastreo, los archivos de programa no se indizan de forma predeterminada. Por lo tanto, las aplicaciones con datos guardados en el directorio de archivos de programa deben agregar su ubicación como regla predeterminada.

### <a name="notes-on-user-rules"></a>Notas sobre las reglas de usuario

Si una nueva regla de usuario es la misma que una regla predeterminada existente, la nueva regla de usuario invalida la regla predeterminada en el conjunto de reglas de trabajo. Si la nueva regla de usuario es la misma que una regla de usuario existente, se reemplaza la regla de usuario anterior.

Establecer la marca *fOverrideChildren* tiene los siguientes resultados en el conjunto de reglas de trabajo:

-   **True** da como resultado la eliminación de todas las reglas secundarias del conjunto de reglas de trabajo (reglas de usuario y reglas predeterminadas).
-   FALSE: al volver a agregar las reglas de trabajo, se establecen todas las reglas predeterminadas que son secundarias de la nueva regla de usuario. Si una regla predeterminada secundaria es una inclusión y la nueva regla de usuario es una exclusión, la regla predeterminada se cambia a una regla de usuario de inclusión.

 

## <a name="removing-scope-rules"></a>Quitar reglas de ámbito

Puede usar la interfaz [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) para quitar una regla de ámbito del conjunto de reglas de trabajo. Esta interfaz proporciona los dos métodos siguientes para quitar las reglas de ámbito.



| Método                                                                                    | Descripción                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RemoveScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removescoperule)               | Quita una regla de usuario para una dirección URL especificada del conjunto de reglas de trabajo. Si la regla de usuario es un duplicado de o invalida una regla predeterminada, la regla predeterminada permanece en el conjunto de reglas de trabajo.                  |
| [**RemoveDefaultScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removedefaultscoperule) | Quita una regla predeterminada para una dirección URL especificada del conjunto de reglas de trabajo y del conjunto de reglas predeterminado. Después de llamar a este método, no se puede revertir a esta regla predeterminada mediante RevertToDefaultScopes. |



 

Cada método toma una dirección URL y una marca que indica si la regla que se va a quitar es una regla de inclusión o exclusión. Estos métodos devuelven un error si no se encuentra una regla con esa marca de dirección URL y de inclusión/exclusión.

**Sugerencia:** Si desea quitar completamente un ámbito del ámbito de rastreo, use el método [**RemoveRoot**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-removeroot) , que quita la raíz de búsqueda y todas las reglas de ámbito asociadas. Para ello, se recomienda, por ejemplo, la desinstalación.

También es posible quitar todas las invalidaciones definidas por el usuario de una raíz de búsqueda y volver a la raíz de búsqueda original y a las reglas de ámbito predeterminadas. Para obtener más información, consulte la sección siguiente.

> [!Note]  
> En Windows Vista, si los usuarios se quitan a través de perfiles de usuario en el panel de control, CSM quita todas las reglas y raíces que incluyen su SID y quita los elementos indexados del catálogo. En Windows XP, debe quitar manualmente las raíces y reglas de los usuarios.

 

 

## <a name="reverting-to-default-rules"></a>Revertir a las reglas predeterminadas

Al revertir a las reglas predeterminadas se quitan todas las reglas de usuario de una dirección URL o raíz y se restauran todas las reglas predeterminadas en el conjunto de reglas de trabajo. No obstante, no quita las reglas establecidas por la Directiva de grupo. El método [**RevertToDefaultScopes**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-reverttodefaultscopes) no toma ningún parámetro y devuelve un código de error si no se puede revertir a las reglas predeterminadas.

 

## <a name="enumerating-scope-rules"></a>Enumerar reglas de ámbito

CSM enumera las reglas de ámbito mediante una interfaz de enumerador de estilo COM estándar, [**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules) . Puede usar esta interfaz para enumerar las reglas de ámbito para varios propósitos. Por ejemplo, puede que desee mostrar todo el conjunto de reglas de trabajo en una interfaz de usuario o detectar si una regla o el elemento secundario de una regla ya está en el ámbito de rastreo.

 

## <a name="tracing-scope-rules"></a>Seguimiento de reglas de ámbito

CSM también le permite determinar si una dirección URL especificada está incluida en el ámbito de rastreo y si tiene una regla de ámbito primario o secundario. También puede averiguar por qué se incluye una dirección URL o se excluye del ámbito de rastreo. Estos métodos no están diseñados para usarse con direcciones URL de patrón.

En la tabla siguiente se describen los métodos de [**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) que se usan para agregar nuevas reglas de ámbito.



| Método                                                                                      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetParentScopeVersionId**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-getparentscopeversionid) | Obtiene el identificador de la versión de la dirección URL de inclusión primaria. Puede usar este método para ver si el ámbito primario ha cambiado desde la última vez que lo protegió.<br/> Ejemplo: Si una aplicación de correo utiliza notificaciones administradas por el proveedor, podría obtener la versión del ámbito principal antes de que se cierre y volver a comprobar la versión cuando se abra. A continuación, la aplicación puede determinar si es necesario insertar un nuevo conjunto de notificaciones en el indexador.<br/> |
| [**HasChildScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-haschildscoperule)             | Devuelve **true** si la dirección URL especificada tiene una regla secundaria (una regla que se aplica a un elemento secundario en cualquier nivel dentro de su jerarquía de direcciones URL). <br/> Ejemplo: Si la dirección URL es file:///C: \\ Folder \\ , este método devuelve **true** si CSM tiene una regla de ámbito específica para la subcarpeta File:///C: \\ Folder \\ \\ .<br/>                                                                                                                                              |
| [**HasParentScopeRule**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-hasparentscoperule)           | Devuelve **true** si la dirección URL especificada tiene una regla primaria (una regla que se aplica a un elemento primario en cualquier nivel de la jerarquía de direcciones URL).<br/> Ejemplo: Si la dirección URL es file:///C: \\ carpeta subcarpeta \\ , este método devuelve **true** si CSM tiene una regla de ámbito específica para file:///C: \\ Folder \\ .<br/>                                                                                                                                                   |
| [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope)       | Devuelve **true** si la dirección URL especificada está incluida en el ámbito de rastreo.                                                                                                                                                                                                                                                                                                                                                                                  |
| [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex)   | Devuelve un valor de la enumeración [**CLUSION \_ Reason**](/windows/win32/api/searchapi/ne-searchapi-clusion_reason) que explica por qué la dirección URL se incluye en el ámbito de rastreo o se excluye del mismo, y recupera el valor **true** si la dirección URL está incluida en el ámbito de rastreo. Este método puede ayudarle a identificar conflictos en el conjunto de reglas de trabajo.                                                                                                                                       |



 

 

> [!Note]  
> Los métodos [**IncludedInCrawlScope**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscope) y [**IncludedInCrawlScopeEx**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager-includedincrawlscopeex) determinan si la dirección URL se rastreará basándose únicamente en las reglas de la CSM. Puede haber otras razones por las que no se rastrea una dirección URL, como el bit FANCI que se establece (es decir, un usuario ha deshabilitado la indexación rápida en el cuadro de diálogo de propiedades de la carpeta).

 

Si cree que se debe excluir una ruta de acceso de archivo, pero se muestra como se incluye, asegúrese de que las reglas de exclusión terminan en " <path> \\ \* ". Si cree que se debe incluir una ruta de acceso de archivo o archivo pero no, asegúrese de comprobar la configuración de bits FANCI para el archivo o la ruta de acceso. Para ello, haga clic con el botón secundario en la ruta de acceso de archivo o archivo y seleccione **propiedades** y, a continuación, asegúrese de que la casilla **de verificación para la búsqueda rápida, permitir el servicio de indización para indizar esta carpeta** está activada. Si el archivo o la ruta de acceso de archivo no se marcan aquí para la indexación, no se indexará aunque esté en una regla de inclusión.

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

**Vista**
</dt> <dt>

[Administración de raíces de búsqueda](-search-3x-wds-extidx-csm-searchroots.md)
</dt> </dl>

 

 




