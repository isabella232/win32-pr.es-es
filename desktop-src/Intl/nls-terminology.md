---
description: En este tema se definen los términos que son importantes al trabajar con la funcionalidad nls.
ms.assetid: daf929b2-8ff9-4a17-b294-f2c0eaef5848
title: Terminología de NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f83ed44b0ba8be3022721148b688f62379e57f7189ff006a0d9255413e31976
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040805"
---
# <a name="nls-terminology"></a>Terminología de NLS

En este tema se definen los términos que son importantes al trabajar con la funcionalidad nls.

## <a name="locale-and-language-terms"></a>Configuración regional y términos de idioma

En la tabla siguiente se resumen los términos de configuración regional y de idioma. Consulte también [Configuraciones regionales e idiomas.](locales-and-languages.md)



|                          | Grupo de idiomas                                                                                                                                                                                                                                                                   | idioma para programas no Unicode                                                                                                                                                                                                                | Estándares y formatos                                                                                                                                                                                                                   |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propósito**              | Proporciona todos los diseños de teclado, editores de métodos de entrada (IME), fuentes TrueType, vínculos de fuente, archivos de paquete de licencias (LPK), fuentes de mapa de bits y tablas de traducción de páginas de códigos que necesita el sistema operativo para un grupo de idiomas. Por lo tanto, afecta a todas las demás configuraciones de esta lista. | Determina qué fuentes de mapa de bits y las páginas de códigos OEM, ANSI y Macintosh son los valores predeterminados del sistema operativo. Este lenguaje solo afecta a las aplicaciones que no son totalmente Unicode. Antes de Windows XP, este idioma se denominaba "configuración regional del sistema". | Determina qué configuración se usa para dar formato a fechas, horas, moneda y números como valor predeterminado para cada usuario. También determina el criterio de ordenación para ordenar texto. Antes de Windows XP, Estándares y formatos se denominaba "configuración regional del usuario". |
| **Primer conjunto**            | Instalación                                                                                                                                                                                                                                                                     | Instalación                                                                                                                                                                                                                                     | Instalación                                                                                                                                                                                                                            |
| **Cómo pueden cambiar los usuarios** | Opciones regionales (Panel de control elemento)<br/> **Windows XP:** Opciones regionales y de idioma<br/> (solo administradores)<br/>                                                                                                                                       | Opciones regionales (Panel de control elemento)<br/> **Windows XP:** Opciones regionales y de idioma<br/> (solo administradores)<br/>                                                                                                       | Opciones regionales (Panel de control elemento)<br/> **Windows XP:** Opciones regionales y de idioma<br/>                                                                                                                               |
| **Predeterminado**              | Oeste de Europa y Estados Unidos grupo de idioma necesarios para mostrar el idioma de una versión localizada.                                                                                                                                                                         | Idioma de la versión localizada.                                                                                                                                                                                                                   | Idioma del sistema operativo localizado.                                                                                                                                                                                                 |
| **Function**             | [**EnumSystemLanguageGroups**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlanguagegroupsa)                                                                                                                                                                                                                     | [**GetSystemDefaultLangID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlangid)                                                                                                                                                                                         | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid), [ **GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)                                                                                                                          |



 



|                          | Configuración regional del subproceso                                                                                                                                                 | Idioma de entrada                                                                                            | Idioma de interfaz de usuario predeterminado del sistema                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propósito**              | Determina la configuración que se usa para dar formato a fechas, horas, monedas y números grandes para un subproceso. También determina el criterio de ordenación para ordenar texto. | Consta de un idioma y un método de entrada.                                                             | Determina el idioma predeterminado de los menús y diálogos, los mensajes, los archivos de información de configuración (INF) y los archivos de ayuda.<br/> **Windows Vista y versiones posteriores:** Se conoce como idioma de instalación. Desempeña un rol más limitado, reemplazado en gran medida por los lenguajes de interfaz de usuario preferidos por el sistema.<br/> Para obtener más información, [vea Interfaz de usuario Language Management](user-interface-language-management.md)<br/> |
| **Primer conjunto**            | El valor predeterminado es Estándares y formatos                                                                                                                              | Instalación                                                                                              | Instalación                                                                                                                                                                                                                                                                                                                                                                                   |
| **Cómo pueden cambiar los usuarios** | [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)                                                                                                                    | Opciones regionales (Panel de control elemento)<br/> **Windows XP:** Opciones regionales y de idioma<br/> | No                                                                                                                                                                                                                                                                                                                                                                                             |
| **Predeterminado**              | Estándares y formatos                                                                                                                                         | Idioma de la versión localizada con el método de entrada predeterminado.                                                  | Idioma de la versión localizada.                                                                                                                                                                                                                                                                                                                                                                 |
| **Function**             | [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)                                                                                                                    | [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)                                                     | [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)                                                                                                                                                                                                                                                                                                                               |



 



|                          | Idioma de la interfaz de usuario del sistema, idiomas de interfaz de usuario preferidos del sistema                                                                                                                                                                  | Idioma de la interfaz de usuario del usuario, idiomas de interfaz de usuario preferidos por el usuario                                                                                                                                               | Idiomas de interfaz de usuario preferidos para subprocesos                                                                                                                                                                 |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propósito**              | Determine el idioma de los menús y diálogos, los mensajes, los archivos INF y los archivos de ayuda para el sistema operativo. Para obtener más información, [vea Interfaz de usuario Language Management](user-interface-language-management.md). | Determine el idioma de los menús y diálogos, los mensajes y los archivos de ayuda para el usuario. Para obtener más información, [vea Interfaz de usuario Language Management](user-interface-language-management.md). | **Windows Vista y versiones posteriores:** Especifique los idiomas preferidos para los subprocesos de aplicación. Para obtener más información, [vea Interfaz de usuario Language Management](user-interface-language-management.md). |
| **Primer conjunto**            | El valor predeterminado es NULL                                                                                                                                                                                                    | El valor predeterminado es NULL                                                                                                                                                                             | El valor predeterminado es NULL                                                                                                                                                                               |
| **Cómo pueden cambiar los usuarios** | Configuración regional y de idioma<br/> (solo administradores)<br/>                                                                                                                                          | Opciones regionales (Panel de control elemento)<br/> **Windows XP:** Opciones regionales y de idioma<br/>                                                                                   | [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)                                                                                                                        |
| **Predeterminado**              | **Windows Vista y versiones posteriores:** Idioma de la versión localizada, seguido de cualquier reserva.                                                                                                                             | **Antes de Windows Vista:** Idioma de la versión localizada.<br/> **Windows Vista y versiones posteriores:** Idioma de la versión localizada, seguido de cualquier reserva.<br/>                     | Lista de valores NULL                                                                                                                                                                                     |
| **Function**             | [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)                                                                                                                                             | [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage), [ **GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)                                                            | [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)                                                                                                                        |



 



|                          | Procesar idiomas de interfaz de usuario preferidos                                                                                                                                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propósito**              | **Windows 7 y versiones posteriores:** Determine los idiomas preferidos para un proceso de aplicación. Para obtener más información, [vea Interfaz de usuario Language Management](user-interface-language-management.md). |
| **Primer conjunto**            | El valor predeterminado es NULL                                                                                                                                                                                |
| **Cómo pueden cambiar los usuarios** | Opciones regionales y de idioma (solo administradores)                                                                                                                                            |
| **Predeterminado**              | **Windows 7 y versiones posteriores:** Idioma de la versión localizada, seguido de cualquier reserva.                                                                                                             |
| **Function**             | [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages), [ **SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)                                             |



 

## <a name="code-page"></a>Página de códigos

La incapacidad de las páginas de códigos de 256 puntos de código para admitir la combinación de scripts en un solo texto fue una de las razones principales para el aumento de Unicode. Las páginas de códigos siguen siendo importantes para escribir código de consola, para mantener aplicaciones heredadas o ejecutarse en versiones anteriores de Windows y para la interacción con algún software que no sea de Microsoft que no esté habilitado para Unicode.

## <a name="input-language"></a>Idioma de entrada

El idioma de entrada se representa mediante una variable de datos por proceso que describe un idioma (por ejemplo, griego) y un método de entrada (por ejemplo, el teclado). Se pueden instalar varios idiomas de entrada y el usuario puede cambiar entre ellos.

Para establecer y recuperar el valor de idioma de entrada, la aplicación llama a [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) y [**GetKeyboardLayout,**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)respectivamente. Los usuarios pueden agregar y quitar idiomas de entrada a través de la pestaña **Idiomas** de la parte regional y de opciones de idioma de la Panel de control.

El idioma de entrada predeterminado es el idioma localizado del sistema operativo y es la configuración que está activa cuando se inicia una nueva aplicación (o cuando se abre una nueva ventana para algunas aplicaciones). El cambio a un idioma de entrada diferente se realiza por aplicación. En otras palabras, se pueden usar dos idiomas de entrada diferentes en dos aplicaciones diferentes. Por ejemplo, un usuario puede escribir alemán con el diseño internacional de teclado Estados Unidos, inglés con entrada de voz (con software que no es de Microsoft) y español mediante un IME en tres aplicaciones diferentes.

## <a name="language-for-non-unicode-programs"></a>Lenguaje para programas no Unicode

El idioma de los programas que no son Unicode (anteriormente denominado "configuración regional del sistema") determina la página de códigos que se usa en el sistema operativo de forma predeterminada. El idioma de la configuración de programas que no son Unicode solo afecta a las aplicaciones que no son Unicode, es decir, a las aplicaciones ANSI. Al establecer el idioma se Windows a emular un sistema operativo no basado en Unicode, localizado a este idioma. Al cambiar el idioma de los programas que no son Unicode se instalan los archivos de fuente de mapa de bits necesarios para admitir aplicaciones no Unicode en el idioma especificado. Para permitir que el usuario seleccione un idioma para programas que no sean Unicode, debe instalarse el grupo de idioma adecuado. La aplicación necesita la compatibilidad con scripts para seleccionar un idioma para programas que no son Unicode. El lenguaje de los programas no Unicode es una configuración por sistema y requiere que se implemente un reinicio.

A veces no hay ninguna diferencia apreciable entre dos idiomas para los programas que no son Unicode. Por ejemplo, este es el caso de las configuraciones regionales alemán (neutro) y alemán (Francia). En general, la configuración de un grupo de idioma es muy similar y solo difiere en la página de códigos OEM o MAC.

Una aplicación ANSI debe comprobar el idioma de la configuración de programas no Unicode durante la instalación. Usa [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) o [**GetOEMCP para**](/windows/desktop/api/Winnls/nf-winnls-getoemcp) recuperar el valor. No se admite ninguna función para establecer el idioma de los programas que no son Unicode. Sin embargo, los usuarios pueden cambiarlo mediante la **pestaña** Opciones avanzadas de la parte de opciones regionales y de idioma de la Panel de control. A continuación se muestran algunos ejemplos de idioma para la configuración de programas no Unicode:

1.  Un usuario alemán que quiera ejecutar una aplicación japonesa diseñada para japonés Windows 95 debe seleccionar japonés como idioma de los programas que no son Unicode. Después de esta selección, las aplicaciones alemanas que no son Unicode tienen problemas. Por ejemplo, las umlauts alemanas (ntes) no se muestran correctamente.
2.  Un usuario alemán que quiera escribir texto japonés en una aplicación en alemán que no sea Unicode debe seleccionar japonés como idioma de los programas que no son Unicode. Como en el primer ejemplo, esto provoca problemas al escribir texto en alemán en aplicaciones que no son Unicode.
3.  Un usuario árabe que quiera escribir árabe, francés e inglés en una aplicación de árabe no Unicode debe seleccionar el árabe como idioma para los programas que no son Unicode, ya que la página de códigos ANSI árabe contiene la mayoría de los caracteres en francés y todos los caracteres en inglés.

## <a name="language-group"></a>Grupo de idioma

El grupo de idioma controla el idioma de los programas no Unicode, estándares y formatos, idiomas de entrada e idiomas de interfaz de usuario que se pueden seleccionar. Para cada versión localizada, el grupo de idioma especificado es el predeterminado y no se puede quitar. Por ejemplo, Windows el grupo de idiomas De Europa Occidental Estados Unidos de forma predeterminada. Por lo tanto, si la versión en inglés de Windows está instalada en un país o región de habla no inglesa, el usuario normalmente instalará otro grupo de idioma.

Al agregar un grupo de idioma, Windows copia (pero no activa) los archivos de teclado necesarios, los editores de métodos de entrada (IME), los archivos de fuente TrueType, los archivos de fuente de mapa de bits y los archivos de compatibilidad con el lenguaje nacional (.nls). La adición de un grupo de idioma también agrega valores del Registro para la vinculación de fuentes e instala motores de scripting para lenguajes de script complejos (árabe, hebreo, indic y tailandés).

Además del grupo de idiomas oeste de Europa Estados Unidos, hay otros 16 grupos de idiomas:



<table>
<tbody>
<tr class="odd">
<td><dl> Árabe<br />
Armenio<br />
Báltico<br />
Europa central<br />
Cirílico<br />
Georgiano<br />
Griego<br />
Hebreo<br />
</dl></td>
<td><dl> Índicas<br />
Japonés<br />
Coreano<br />
Chino simplificado<br />
Chino tradicional<br />
Tailandés<br />
Turcas<br />
Vietnamita<br />
</dl></td>
</tr>
</tbody>
</table>



 

Cualquier número y combinación de grupos de idioma se puede instalar en cualquier sistema operativo. Por ejemplo, un usuario español puede instalar el grupo de idioma cirílico para trabajar con textos en ruso. En este caso, una aplicación de procesamiento de palabras también debe admitir el grupo de lenguaje cirílico.

> [!Note]  
> Agregar el grupo de idioma adecuado no permite automáticamente que una aplicación acepte texto. Se recomienda realizar pruebas. Por ejemplo, las aplicaciones que no son Unicode pueden requerir que se cambie el idioma de los programas que no son Unicode.

 

## <a name="location"></a>Ubicación

**Windows XP:** Una ubicación es un identificador geográfico. Se representa mediante una variable de datos por usuario que define el país o región donde reside el usuario.

Para establecer el valor, la aplicación llama a [**SetUserGeoID.**](/windows/desktop/api/Winnls/nf-winnls-setusergeoid) Para recuperar el valor, la aplicación llama [**a GetUserGeoID.**](/windows/desktop/api/Winnls/nf-winnls-getusergeoid)

## <a name="standards-and-formats"></a>Estándares y formatos

Estándares y formatos (anteriormente "configuración regional del usuario") es una variable por usuario que determina el criterio de ordenación predeterminado y la configuración predeterminada para dar formato a fechas, horas, moneda y números. La variable se presenta como un idioma (a veces en combinación con un país o región), pero no es un idioma en sí. Por ejemplo, establecer la variable Estándares y formatos en hebreo indica que el usuario quiere usar las convenciones de formato de hebreo, no necesariamente el idioma hebreo. Además, la variable Estándares y formatos determina la cadena que se usa para los nombres de días y meses. Por ejemplo, si un usuario muestra "25 de noviembre de 1998", la cadena "Noviembre" puede cambiar en función de la variable Estándares y formatos. Al cambiar la variable, se agrega automáticamente una configuración regional de entrada con la configuración predeterminada del idioma.

Para obtener la configuración de variable Estándares y formatos, la aplicación llama a [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) o [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename). No hay ninguna función NLS disponible para establecer la variable. Sin embargo, los usuarios pueden cambiarlo a través de la **pestaña Opciones de** región en la parte de opciones regionales y de idioma de la Panel de control.

Normalmente, una aplicación debe usar la configuración de variables Estándares y Formatos para mostrar los datos. Sin embargo, una aplicación que usa una configuración regional fija para mostrar datos debe pasar un identificador de configuración regional específico en lugar de usar LOCALE \_ USER \_ DEFAULT.

## <a name="thread-locale"></a>Configuración regional del subproceso

La configuración regional del subproceso se representa mediante una variable de datos de configuración regional por subproceso que determina el formato de fechas, horas, moneda y números grandes para el subproceso. El valor predeterminado es el valor de la configuración regional seleccionada actualmente para Estándares y formatos. Para establecer la configuración regional del subproceso, la aplicación llama a [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale). Para recuperar la configuración regional del subproceso, la aplicación llama [**a GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).

En la mayoría de los casos, no se debe sobrescribir la configuración regional del subproceso. Normalmente solo se debe usar para sincronizar la configuración regional del subproceso de una aplicación de servidor con la variable Estándares y formatos de un equipo cliente. Por ejemplo, una aplicación bursátil financiera para la bolsa de Nueva York Exchange, que se usa en bancos de todo el mundo, tiene que mostrar la hora, la fecha y los precios de las acciones en Estados Unidos formatos. Esta aplicación usa [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) para establecer la configuración regional del subproceso en inglés (Estados Unidos) y, a continuación, usa las funciones NLS para dar formato a fechas, horas y precios de las acciones.

El cambio de la configuración regional del subproceso no afecta a todas las funciones de API. Por lo tanto, no siempre es una manera confiable de invalidar la variable Standards and Formats. En su lugar, las aplicaciones que controlan estándares y formatos deben usar una configuración regional fija para mostrar datos, pasando un identificador de configuración regional específico en lugar de usar LOCALE \_ USER \_ DEFAULT.

## <a name="nls-example"></a>Ejemplo de NLS

En el ejemplo siguiente se muestra la interacción entre estándares y formatos, el idioma de los programas que no son Unicode, la ubicación y el idioma de la interfaz de usuario del usuario.

Un usuario nativo de México pero que está en la Estados Unidos tiene un equipo que ejecuta Windows XP inglés. El usuario establece la ubicación en Estados Unidos usar un proveedor de servicios de Internet (ISP) para obtener el tiempo del Estados Unidos. Sin embargo, la variable Estándares y formatos se establece en Español (México) para que la información se formatee según los estándares de La República. Además, el usuario usa un procesador de palabras coreano, que es una aplicación ANSI, para que el idioma de los programas no Unicode esté establecido en coreano (Corea). Para usar la aplicación, el usuario tiene un teclado en inglés y también instala un IME coreano para admitir un segundo idioma de entrada. El compañero de trabajo del usuario, que comparte el equipo pero no está cómodo con el inglés, puede establecer el idioma de la interfaz de usuario del usuario en español (España) cuando se usa el equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con idiomas nacionales](about-national-language-support.md)
</dt> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Interfaz de usuario multilingüe](multilingual-user-interface.md)
</dt> </dl>

 

 
