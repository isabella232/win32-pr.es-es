---
description: MUI permite a las aplicaciones administrar los idiomas de la interfaz de usuario de dos maneras.
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: Administración del idioma de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852fe20d3edb9795c2c2a9d3ec45c1e8ffe053ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424052"
---
# <a name="user-interface-language-management"></a>Administración del idioma de la interfaz de usuario

MUI permite a las aplicaciones administrar los idiomas de la interfaz de usuario de dos maneras. Una aplicación puede usar un enfoque sencillo para la administración de idiomas de forma predeterminada en la configuración de idioma del sistema operativo. Como alternativa, la aplicación puede admitir sus propios idiomas desde los que el usuario puede seleccionar. La API de MUI también permite a la aplicación tener acceso directo a idiomas y listas de idiomas que admite el sistema operativo y que mantiene el cargador de recursos. En el resto de este tema se definen los idiomas admitidos por el sistema y el mecanismo de reserva de idioma.

## <a name="languages-maintained-by-the-operating-system"></a>Idiomas mantenidos por el sistema operativo

### <a name="system-default-ui-languageinstall-language"></a>Idioma de interfaz de usuario predeterminado del sistema/idioma de instalación

El idioma de la interfaz de usuario predeterminada del sistema es el idioma de la versión localizada que se usa para configurar Windows. Todos los menús, cuadros de diálogo, mensajes de error y archivos de ayuda se representan en este idioma, excepto cuando el usuario selecciona un idioma diferente.

En Windows Vista y versiones posteriores, el idioma predeterminado de la interfaz de usuario del sistema se conoce como "idioma de instalación" y juega un rol más limitado. En la mayoría de los casos, se sustituye por los idiomas de interfaz de usuario preferidos del sistema. Sin embargo, en algunos contextos resulta útil tener un solo idioma de instalación que siempre se sabe que es totalmente compatible.

No hay ninguna función de MUI disponible para establecer el idioma de la interfaz de usuario predeterminada del sistema. Para recuperar este idioma, la aplicación puede llamar a [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage).

### <a name="system-ui-language"></a>Idioma de la interfaz de usuario del sistema

El sistema operativo define el idioma de la interfaz de usuario del sistema como un idioma de interfaz de usuario que puede establecer un administrador en la ficha Opciones **avanzadas** de la parte configuración regional y de idioma del panel de control. El sistema operativo usa este idioma si el usuario actual no ha realizado la configuración de idioma específica o si no hay ninguna cuenta activa iniciada. El idioma solo se puede cambiar si hay más de un idioma de interfaz de usuario instalado en el equipo.

> [!Note]  
> El sistema operativo debe reiniciarse para todos los usuarios y servicios para ver el efecto del cambio de idioma.

 

No hay ninguna función de MUI disponible para establecer el idioma de la interfaz de usuario del sistema. Para recuperar este valor, una aplicación destinada a Windows Vista y versiones posteriores puede llamar a [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) y obtener el primer idioma en la lista de idiomas preferidos de la interfaz de usuario del sistema. Las aplicaciones destinadas a sistemas operativos anteriores a Windows Vista no pueden usar [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) y deben basarse en la suposición de que el idioma de la interfaz de usuario del sistema es siempre el mismo que el idioma predeterminado de la interfaz de usuario del sistema.

### <a name="user-ui-language"></a>Idioma de la interfaz de usuario

El idioma de la interfaz de usuario del usuario determina el idioma de la interfaz de usuario que se usa para los menús, cuadros de diálogo, archivos de ayuda, etc. El usuario actual puede establecerla en la ficha **idioma** de la parte configuración regional y de idioma del panel de control. Este idioma solo se puede cambiar si hay más de un idioma de interfaz de usuario instalado en el equipo. Tenga en cuenta que el usuario tendrá que cerrar la sesión y volver a iniciarla para ver el efecto. Por ejemplo, una corporación multinacional desea implementar Windows en todas sus subsidiarias. La compañía crea un trabajo de instalación global, que instala la versión en Inglés de Windows en todos los clientes, independientemente de su ubicación. Al mismo tiempo, instala módulos de idioma específicos en función de la unidad organizativa a la que pertenece un equipo. Cuando el usuario inicia sesión por primera vez en un sistema operativo recién instalado, Windows aparece como una versión localizada.

En Windows Vista y versiones posteriores, el idioma de la interfaz de usuario del usuario es el primer idioma de la lista de idiomas preferidos de la interfaz de usuario. Tenga en cuenta que se pueden usar idiomas de reserva si los recursos determinados no están disponibles en este idioma.

En los sistemas operativos anteriores a Windows Vista, el idioma de la interfaz de usuario del usuario suele ser el mismo que el idioma predeterminado de la interfaz de usuario. Sin embargo, para Windows MUI, los dos idiomas pueden ser diferentes.

Para recuperar el idioma de la interfaz de usuario del usuario, una aplicación puede llamar a [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) o [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages). La aplicación no puede cambiar el idioma de la interfaz de usuario del usuario, ya que no hay ninguna función para establecerla.

## <a name="language-lists-maintained-by-the-operating-system"></a>Listas de idiomas mantenidas por el sistema operativo

### <a name="system-preferred-ui-languages-list"></a>Lista de idiomas de interfaz de usuario preferidos del sistema

El cargador de recursos mantiene una lista de idiomas de interfaz de usuario preferidos del sistema. En esta lista se incluyen los idiomas preferidos por el sistema operativo para sus propios recursos, como menús y cuadros de diálogo, mensajes, archivos INF y archivos de ayuda. La lista está formada por el idioma predeterminado de la interfaz de usuario del sistema y el idioma de la interfaz de usuario del sistema y sus reservas. Una aplicación puede recuperar los idiomas de interfaz de usuario preferidos del sistema llamando a [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages).

### <a name="user-preferred-ui-languages-list"></a>Lista de idiomas de interfaz de usuario preferidos

El cargador de recursos usa una lista de idiomas preferidos de la interfaz de usuario que incluye los idiomas que el usuario prefiere. El cargador de recursos utiliza los lenguajes que coinciden con los de esta lista, si están disponibles, para un subproceso de aplicación determinado. Estos idiomas tienen prioridad sobre las preferencias del sistema. Para recuperar los idiomas preferidos de la interfaz de usuario, la aplicación puede llamar a [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages).

### <a name="process-preferred-ui-languages-list"></a>Procesar lista de idiomas preferidos de la interfaz de usuario

En Windows Vista y versiones posteriores, el cargador de recursos mantiene una lista de idiomas preferidos de la interfaz de usuario de proceso que consta de hasta cinco idiomas válidos establecidos por un proceso en ejecución para una aplicación MUI. La aplicación puede establecer los idiomas con una llamada a [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages). La aplicación puede recuperar los idiomas mediante una llamada a [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages).

### <a name="thread-preferred-ui-languages-list"></a>Lista de idiomas de interfaz de usuario preferida de subproceso

En Windows Vista y versiones posteriores, el cargador de recursos usa una lista de idiomas de interfaz de usuario preferida de subprocesos que consta de hasta cinco idiomas válidos establecidos por un subproceso en un proceso en ejecución para una aplicación MUI. Estos idiomas se usan para personalizar los idiomas de la interfaz de usuario de la aplicación y hacerlos distintos del idioma del sistema operativo. La lista de idiomas preferidos de la interfaz de usuario de subprocesos se basa en los idiomas preferidos de la interfaz de usuario, en los idiomas de interfaz de usuario preferidos del sistema y en el idioma predeterminado.

Para establecer los lenguajes de interfaz de usuario preferidos del subproceso, la aplicación debe llamar a [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Para recuperar estos lenguajes, la aplicación llama a [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages).

## <a name="neutral-language-representation"></a>Representación de lenguaje neutro

Un idioma neutro se representa como el idioma por sí solo, sin región o configuración regional. Por ejemplo, la representación neutra del idioma inglés (Canadá), en-CA, se representa como "en". Aunque un idioma neutro no esté asociado a los aspectos de una región o configuración regional, puede asociarlo a un conjunto de recursos. Normalmente, un recurso de idioma neutro se basa en el uso en la región más frecuente del idioma.

Como ejemplo, supongamos que la aplicación MUI localiza los recursos de idioma alemán para alemán (Suiza) representados como de-CH y alemán (Austria) representados como de-AT, mientras se crea un conjunto completo de recursos para alemán (Alemania) representado como de-DE. Debe tomar decisiones para esta aplicación que considere archivos de recursos completos. Si la aplicación duplica los recursos de-DE como recursos de idioma neutro, debe proporcionar un idioma de reserva para el cargador de recursos. Si el cargador no encuentra un archivo de recursos específico del lenguaje concreto para el de-CH o para el de-AT, recurre a los recursos de "de" independientes del lenguaje. Es más probable que estos recursos sean más adecuados que los recursos para un idioma totalmente diferente, por ejemplo, Inglés (Estados Unidos), que son los únicos otros posibles reservas.

Como otro ejemplo, una aplicación podría no localizarse en absoluto para Belice. Sin embargo, la compatibilidad con una preferencia de idioma de inglés (Belice), representada como en-BZ, permite a la aplicación revertir a los recursos "en".

## <a name="language-fallback-in-the-resource-loader"></a>Reserva de lenguaje en el cargador de recursos

Windows Vista y versiones posteriores organizan la configuración del idioma de la interfaz de usuario en una lista de idiomas de reserva prepedidos que usa el cargador de recursos. Para formar la lista, el sistema operativo combina varios idiomas en el orden mostrado:

-   Idiomas preferidos de la interfaz de usuario de subprocesos, que constan del lenguaje de la interfaz de usuario de subprocesos y su Algunos ejemplos son fr-FR para francés (Francia) y su forma neutra "fr" y es-ES para español (España) y su forma neutra "es".
-   Procese los idiomas preferidos de la interfaz de usuario, que consisten en el idioma de la interfaz de usuario del proceso y su forma neutra. Un ejemplo es de-DE para alemán (Alemania) y su forma neutra "de".
-   Idioma de la interfaz de usuario del usuario y su forma neutra. Un ejemplo es ja-JP para japonés (Japón) y su forma neutra "ja".
-   Idioma de la interfaz de usuario del sistema y su forma neutra. Un ejemplo es it-IT para italiano (Italia) y su forma neutra "it".
    > [!Note]  
    > Este idioma solo se incluye en la lista de reserva cuando no se establece el idioma de la interfaz de usuario del usuario.

     

-   Idioma de la interfaz de usuario predeterminada del sistema y su forma neutra. Un ejemplo es es-ES para español (España) y su forma neutra "es".

A continuación se muestra la lista de reserva combinada. Tenga en cuenta que la duplicación de lenguajes, por ejemplo, es-ES y es, se elimina. Puesto que en el ejemplo se establece el idioma de la interfaz de usuario de usuario en ja-JP, el idioma de la interfaz de usuario del sistema no aparece en la lista de reserva combinada.

fr-FR, fr, es-ES, es, de-DE, de, ja-JP, ja

Al cargar recursos para una aplicación de MUI, el cargador de recursos intenta seleccionar uno de los archivos que coinciden con la lista de idiomas preferidos de la interfaz de usuario del subproceso para el subproceso de la aplicación que se está ejecutando. Si el cargador de recursos no encuentra una coincidencia directa entre un idioma seleccionado y el primer recurso específico del idioma de la lista de reserva combinada, comprueba los idiomas siguientes de la lista hasta que encuentre una reserva aceptable.

Si el cargador de recursos no encuentra ningún archivo que necesite, debe usar un lenguaje de reserva de "buena garantía". Para la tecnología de recursos de MUI, el cargador de recursos determina el idioma de reserva de los datos de configuración de recursos proporcionados. Para obtener más información, consulte [Administración de recursos de MUI](mui-resource-management.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la interfaz de usuario multilingüe](about-multilingual-user-interface.md)
</dt> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Terminología de NLS](nls-terminology.md)
</dt> </dl>

 

 



