---
description: LA INTERFAZ de usuario permite que las aplicaciones administren los lenguajes de la interfaz de usuario de dos maneras.
ms.assetid: ae8ab98f-dc3b-414d-85c9-6bf204c2f776
title: Interfaz de usuario Language Management
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852fe20d3edb9795c2c2a9d3ec45c1e8ffe053ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254918"
---
# <a name="user-interface-language-management"></a>Interfaz de usuario Language Management

LA INTERFAZ de usuario permite que las aplicaciones administren los lenguajes de la interfaz de usuario de dos maneras. Una aplicación puede usar un enfoque simple para la administración de idiomas de forma predeterminada en la configuración de idioma del sistema operativo. Como alternativa, la aplicación puede admitir sus propios idiomas desde los que el usuario puede seleccionar. La API DE MOMENTO también permite que la aplicación acceda directamente a idiomas y listas de idiomas compatibles con el sistema operativo y mantenidos por el cargador de recursos. En el resto de este tema se definen los idiomas admitidos por el sistema y el mecanismo de reserva de idioma.

## <a name="languages-maintained-by-the-operating-system"></a>Idiomas mantenidos por el sistema operativo

### <a name="system-default-ui-languageinstall-language"></a>Idioma predeterminado de la interfaz de usuario del sistema/Idioma de instalación

El idioma predeterminado de la interfaz de usuario del sistema es el idioma de la versión localizada que se usa para configurar Windows. Todos los menús, cuadros de diálogo, mensajes de error y archivos de ayuda se representan en este idioma, excepto cuando el usuario selecciona otro idioma.

En Windows Vista y versiones posteriores, el lenguaje de interfaz de usuario predeterminado del sistema se conoce como "idioma de instalación" y desempeña un rol más limitado. Para la mayoría de los propósitos, se sustituye por los idiomas de interfaz de usuario preferidos del sistema. Sin embargo, en determinados contextos es útil tener un único lenguaje de instalación que siempre se sabe que es totalmente compatible.

No hay ninguna función DESA disponible para establecer el idioma predeterminado de la interfaz de usuario del sistema. Para recuperar este lenguaje, la aplicación puede llamar a [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage).

### <a name="system-ui-language"></a>Idioma de la interfaz de usuario del sistema

El sistema operativo define el idioma de la interfaz de usuario  del sistema como un idioma de interfaz de usuario que un administrador puede establecer en la pestaña Opciones avanzadas de la parte de opciones regionales y de idioma de Panel de control. El sistema operativo usa este idioma si el usuario actual no ha realizado una configuración de idioma específica o si no ha iniciado sesión ninguna cuenta activa. El idioma solo se puede cambiar si hay más de un idioma de interfaz de usuario instalado en el equipo.

> [!Note]  
> El sistema operativo debe reiniciarse para que todos los usuarios y servicios vean el efecto del cambio de idioma.

 

No hay ninguna función DE ACUERDO disponible para establecer el idioma de la interfaz de usuario del sistema. Para recuperar este valor, una aplicación destinada a Windows Vista y versiones posteriores puede llamar a [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) y obtener el primer idioma en la lista de idiomas de interfaz de usuario preferidos del sistema. Las aplicaciones destinadas a sistemas operativos anteriores Windows Vista no pueden usar [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages) y deben basarse en la suposición de que el lenguaje de interfaz de usuario del sistema siempre es el mismo que el idioma predeterminado de la interfaz de usuario del sistema.

### <a name="user-ui-language"></a>Lenguaje de interfaz de usuario de usuario

El idioma de la interfaz de usuario de usuario determina el idioma de la interfaz de usuario que se usa para menús, cuadros de diálogo, archivos de ayuda, etc. El usuario actual puede establecerlo en la pestaña **Idioma** de la parte regional y de opciones de idioma de Panel de control. Este idioma solo se puede cambiar si hay más de un idioma de interfaz de usuario instalado en el equipo. Tenga en cuenta que el usuario tendrá que cerrar sesión y volver a iniciarla para ver el efecto. Por ejemplo, una empresa multinacional quiere implementar Windows en todas sus subsidiarias. La empresa crea un trabajo de instalación global, que instala la versión en inglés de Windows en todos los clientes, independientemente de la ubicación. Al mismo tiempo, instala módulos de idioma específicos en función de la unidad organizativa de la que sea miembro un equipo. Cuando el usuario inicia sesión por primera vez en un sistema operativo recién instalado, Windows aparece como una versión localizada.

En Windows Vista y versiones posteriores, el idioma de la interfaz de usuario de usuario es el primer idioma de la lista de idiomas de interfaz de usuario preferidos por el usuario. Tenga en cuenta que los idiomas de reserva se pueden usar si determinados recursos no están disponibles en este idioma.

En los sistemas operativos Windows vista previos, el idioma de la interfaz de usuario del usuario suele ser el mismo que el idioma predeterminado de la interfaz de usuario del sistema. Sin embargo, para Windows DEA, los dos idiomas pueden ser diferentes.

Para recuperar el lenguaje de interfaz de usuario de usuario, una aplicación puede llamar a [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage) o [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages). La aplicación no puede cambiar el idioma de la interfaz de usuario del usuario, ya que no hay ninguna función para establecerlo.

## <a name="language-lists-maintained-by-the-operating-system"></a>Listas de idiomas mantenidas por el sistema operativo

### <a name="system-preferred-ui-languages-list"></a>Lista de idiomas de interfaz de usuario preferidos del sistema

El cargador de recursos mantiene una lista de idiomas de interfaz de usuario preferidos del sistema. En esta lista se incluyen los idiomas preferidos por el sistema operativo para sus propios recursos, como menús y diálogos, mensajes, archivos INF y archivos de ayuda. La lista se completa con el idioma predeterminado de la interfaz de usuario del sistema y el idioma de la interfaz de usuario del sistema y sus reservas. Una aplicación puede recuperar los lenguajes de interfaz de usuario preferidos del sistema llamando a [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages).

### <a name="user-preferred-ui-languages-list"></a>Lista de idiomas de interfaz de usuario preferidos por el usuario

El cargador de recursos usa una lista de idiomas de interfaz de usuario preferidos por el usuario que incluye los idiomas que prefiere el usuario. El cargador de recursos usa los idiomas que coinciden con los recursos de esta lista, si están disponibles, para un subproceso de aplicación determinado. Estos idiomas tienen prioridad sobre las preferencias del sistema. Para recuperar los lenguajes de interfaz de usuario preferidos por el usuario, la aplicación puede llamar a [**GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages).

### <a name="process-preferred-ui-languages-list"></a>Procesar lista de idiomas de interfaz de usuario preferidos

En Windows Vista y versiones posteriores, el cargador de recursos mantiene una lista de idiomas de interfaz de usuario preferidos del proceso que consta de un máximo de cinco idiomas válidos establecidos por un proceso en ejecución para una aplicación DE INTERFAZ DE USUARIO. La aplicación puede establecer los idiomas con una llamada a [**SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages). La aplicación puede recuperar los idiomas llamando a [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages).

### <a name="thread-preferred-ui-languages-list"></a>Lista de idiomas de interfaz de usuario preferidos para subprocesos

En Windows Vista y versiones posteriores, el cargador de recursos usa una lista de idiomas de interfaz de usuario preferidos para subprocesos que consta de hasta cinco idiomas válidos establecidos por un subproceso en un proceso en ejecución para una aplicación DE INTERFAZ DE USUARIO. Estos idiomas se usan para personalizar los idiomas de la interfaz de usuario de la aplicación y hacer que sean diferentes del idioma del sistema operativo. La lista de idiomas de interfaz de usuario preferidos del subproceso se basa en los idiomas de interfaz de usuario preferidos por el usuario, los idiomas de interfaz de usuario preferidos por el sistema y el idioma predeterminado de la interfaz de usuario del sistema.

Para establecer los lenguajes de interfaz de usuario preferidos del subproceso, la aplicación debe llamar a [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages). Para recuperar estos lenguajes, la aplicación llama a [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages).

## <a name="neutral-language-representation"></a>Representación de idioma neutro

Un idioma neutro se representa como el idioma por sí solo, sin región ni configuración regional. Por ejemplo, la representación neutra del idioma inglés (Canadá), en-CA, se representa como "en". Aunque un idioma neutro no está asociado a los aspectos de una región o configuración regional, puede asociarlo a un conjunto de recursos. Normalmente, un recurso de idioma neutro se basa en el uso en la región más frecuente para el idioma.

Como ilustración, supongamos que la aplicación DEA localiza recursos en alemán para alemán (Suiza) representados como de-CH y alemán (Alemania) representados como de-AT, al tiempo que se construye un conjunto completo de recursos para alemán (Alemania) representado como de-DE. Debe tomar decisiones para esta aplicación teniendo en cuenta los archivos de recursos completos. Si la aplicación duplica los recursos de de-DE como recursos de lenguaje neutro, debe proporcionar un idioma de reserva para el cargador de recursos. Si el cargador no encuentra un archivo de recursos específico del idioma concreto para de-CH o para de-AT, vuelve a los recursos "de" neutrales del idioma. Estos recursos son probablemente más adecuados que los recursos para un idioma completamente diferente, por ejemplo, inglés (Estados Unidos), que son las únicas posibles reservaciones.

Como otro ejemplo, es posible que una aplicación no se localice en absoluto para La 1.0. Sin embargo, la compatibilidad con una preferencia de idioma de inglés (en-BZ), representada como en-BZ, permite que la aplicación vuelva a los recursos "en".

## <a name="language-fallback-in-the-resource-loader"></a>Reserva de idioma en el cargador de recursos

Windows Vista y versiones posteriores organizan la configuración del idioma de la interfaz de usuario en una lista de idiomas de reserva ordenados previamente que usa el cargador de recursos. Para formar la lista, el sistema operativo combina varios idiomas, en el orden mostrado:

-   Idiomas de interfaz de usuario preferidos para subprocesos, que constan del lenguaje de interfaz de usuario del subproceso y su forma neutra. Algunos ejemplos son fr-FR para francés (Francia) y su forma neutra "fr" y es-ES para español (España) y su forma neutra "es".
-   Procese los idiomas de interfaz de usuario preferidos, que constan de lenguaje de interfaz de usuario de proceso y su forma neutra. Un ejemplo es de-DE para alemán (Alemania) y su forma neutra "de".
-   Idioma de la interfaz de usuario de usuario y su forma neutra. Un ejemplo es ja-JP para japonés (Japón) y su forma neutra "ja".
-   Idioma de la interfaz de usuario del sistema y su forma neutra. Un ejemplo es it-IT para italiano (Italia) y su forma neutra "it".
    > [!Note]  
    > Este idioma solo se incluye en la lista de reserva cuando no se establece el idioma de la interfaz de usuario del usuario.

     

-   Idioma de interfaz de usuario predeterminado del sistema y su forma neutra. Un ejemplo es-ES para español (España) y su forma neutra "es".

A continuación se muestra la lista de reserva combinada. Tenga en cuenta que se elimina la duplicación de idiomas, por ejemplo, es-ES y es. Puesto que el ejemplo establece el idioma de la interfaz de usuario del usuario en ja-JP, el idioma de la interfaz de usuario del sistema no aparece en la lista de reserva combinada.

fr-FR, fr, es-ES, es, de-DE, de, ja-JP, ja

Al cargar recursos para una aplicación DE JAVA, el cargador de recursos intenta seleccionar uno de los archivos que coinciden con la lista de idiomas de interfaz de usuario preferidos del subproceso para el subproceso de aplicación que se está ejecutando actualmente. Si el cargador de recursos no encuentra una coincidencia directa entre un idioma seleccionado y el primer recurso específico del lenguaje en la lista de reserva combinada, comprueba los idiomas posteriores de la lista hasta que encuentra una reserva aceptable.

Si el cargador de recursos no encuentra ningún archivo que necesite, debe usar un lenguaje de reserva "bueno garantizado". En el caso de la tecnología de recursos DE JAVA, el cargador de recursos determina el lenguaje de reserva a partir de los datos de configuración de recursos proporcionados. Para obtener más información, vea [ADMINISTRACIÓN DE RECURSOS DE LA INTERFAZ DE USUARIO](mui-resource-management.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Interfaz de usuario multilingüe](about-multilingual-user-interface.md)
</dt> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Terminología de NLS](nls-terminology.md)
</dt> </dl>

 

 



