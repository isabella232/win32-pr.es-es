---
description: En este tema se definen los términos que son importantes al trabajar con la funcionalidad NLS.
ms.assetid: daf929b2-8ff9-4a17-b294-f2c0eaef5848
title: Terminología de NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a86808d31cb034e7ad29e4580b8f201ad3c9a6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818595"
---
# <a name="nls-terminology"></a>Terminología de NLS

En este tema se definen los términos que son importantes al trabajar con la funcionalidad NLS.

## <a name="locale-and-language-terms"></a>Términos de idioma y configuración regional

En la tabla siguiente se resumen los términos de idioma y la configuración regional. Vea también [configuraciones regionales e idiomas](locales-and-languages.md).



|                          | Grupo de idiomas                                                                                                                                                                                                                                                                   | idioma para programas no Unicode                                                                                                                                                                                                                | Estándares y formatos                                                                                                                                                                                                                   |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propósito**              | Proporciona todas las distribuciones de teclado, editores de métodos de entrada (IME), fuentes TrueType, vínculos de fuente, archivos de paquete de licencia (LPKs), fuentes de mapa de bits y tablas de traducción de páginas de códigos necesarias para el sistema operativo de un grupo de idiomas. Por lo tanto, afecta a todas las demás opciones de esta lista. | Determina qué fuentes de mapa de bits, y las páginas de códigos OEM, ANSI y Macintosh son valores predeterminados para el sistema operativo. Este lenguaje solo afecta a las aplicaciones que no son totalmente Unicode. Antes de Windows XP, este idioma se denominaba "configuración regional del sistema". | Determina qué valores se usan para dar formato a fechas, horas, monedas y números como valor predeterminado para cada usuario. También determina el criterio de ordenación para ordenar el texto. Antes de Windows XP, los estándares y formatos se denominaban "configuración regional del usuario". |
| **Primer conjunto**            | Instalación                                                                                                                                                                                                                                                                     | Instalación                                                                                                                                                                                                                                     | Instalación                                                                                                                                                                                                                            |
| **Cómo los usuarios pueden cambiar** | Opciones regionales (elemento del panel de control)<br/> **Windows XP:** Opciones de configuración regional y de idioma<br/> (solo administradores)<br/>                                                                                                                                       | Opciones regionales (elemento del panel de control)<br/> **Windows XP:** Opciones de configuración regional y de idioma<br/> (solo administradores)<br/>                                                                                                       | Opciones regionales (elemento del panel de control)<br/> **Windows XP:** Opciones de configuración regional y de idioma<br/>                                                                                                                               |
| **Valor predeterminado**              | Europa occidental y Estados Unidos y el grupo de idiomas necesarios para mostrar el idioma de una versión localizada.                                                                                                                                                                         | Idioma de la versión localizada.                                                                                                                                                                                                                   | Idioma del sistema operativo localizado.                                                                                                                                                                                                 |
| **Function**             | [**EnumSystemLanguageGroups**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlanguagegroupsa)                                                                                                                                                                                                                     | [**GetSystemDefaultLangID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlangid)                                                                                                                                                                                         | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid), [ **GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)                                                                                                                          |



 



|                          | Configuración regional de subprocesos                                                                                                                                                 | Idioma de entrada                                                                                            | Idioma de interfaz de usuario predeterminado del sistema                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propósito**              | Determina la configuración que se usa para dar formato a fechas, horas, monedas y números grandes de un subproceso. También determina el criterio de ordenación para ordenar el texto. | Consta de un lenguaje y un método de entrada.                                                             | Determina el idioma predeterminado de los menús y los cuadros de diálogo, los mensajes, los archivos de información de instalación (INF) y los archivos de ayuda.<br/> **Windows Vista y versiones posteriores:** Conocido como idioma de instalación. Juega un rol más limitado, reemplazado en gran medida por los idiomas de interfaz de usuario preferidos del sistema.<br/> Para obtener más información, consulte Administración del idioma de la [interfaz de usuario](user-interface-language-management.md)<br/> |
| **Primer conjunto**            | De forma predeterminada, estándares y formatos                                                                                                                              | Instalación                                                                                              | Instalación                                                                                                                                                                                                                                                                                                                                                                                   |
| **Cómo los usuarios pueden cambiar** | [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)                                                                                                                    | Opciones regionales (elemento del panel de control)<br/> **Windows XP:** Opciones de configuración regional y de idioma<br/> | No                                                                                                                                                                                                                                                                                                                                                                                             |
| **Valor predeterminado**              | Estándares y formatos                                                                                                                                         | Idioma de la versión localizada con el método de entrada predeterminado.                                                  | Idioma de la versión localizada.                                                                                                                                                                                                                                                                                                                                                                 |
| **Function**             | [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)                                                                                                                    | [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)                                                     | [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)                                                                                                                                                                                                                                                                                                                               |



 



|                          | Idioma de la interfaz de usuario del sistema, idiomas de interfaz de usuario preferidos                                                                                                                                                                  | Idioma de la IU de usuario, idiomas preferidos de la interfaz de usuario                                                                                                                                               | Idiomas de interfaz de usuario preferidos del subproceso                                                                                                                                                                 |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propósito**              | Determine el idioma de los menús y cuadros de diálogo, mensajes, archivos INF y archivos de ayuda del sistema operativo. Para obtener más información, consulte Administración del idioma de la [interfaz de usuario](user-interface-language-management.md). | Determine el idioma de los menús y los cuadros de diálogo, los mensajes y los archivos de ayuda del usuario. Para obtener más información, consulte Administración del idioma de la [interfaz de usuario](user-interface-language-management.md). | **Windows Vista y versiones posteriores:** Especifique los idiomas preferidos para los subprocesos de aplicación. Para obtener más información, consulte Administración del idioma de la [interfaz de usuario](user-interface-language-management.md). |
| **Primer conjunto**            | El valor predeterminado es NULL                                                                                                                                                                                                    | El valor predeterminado es NULL                                                                                                                                                                             | El valor predeterminado es NULL                                                                                                                                                                               |
| **Cómo los usuarios pueden cambiar** | Configuración regional y de idioma<br/> (solo administradores)<br/>                                                                                                                                          | Opciones regionales (elemento del panel de control)<br/> **Windows XP:** Opciones de configuración regional y de idioma<br/>                                                                                   | [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)                                                                                                                        |
| **Valor predeterminado**              | **Windows Vista y versiones posteriores:** Idioma de la versión localizada, seguido de cualquier reserva.                                                                                                                             | **Antes de Windows Vista:** Idioma de la versión localizada.<br/> **Windows Vista y versiones posteriores:** Idioma de la versión localizada, seguido de cualquier reserva.<br/>                     | Lista de valores NULL                                                                                                                                                                                     |
| **Function**             | [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)                                                                                                                                             | [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage), [ **GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)                                                            | [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)                                                                                                                        |



 



|                          | Idiomas de interfaz de usuario preferidos de proceso                                                                                                                                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propósito**              | **Windows 7 y versiones posteriores:** Determine los idiomas preferidos para un proceso de aplicación. Para obtener más información, consulte Administración del idioma de la [interfaz de usuario](user-interface-language-management.md). |
| **Primer conjunto**            | El valor predeterminado es NULL                                                                                                                                                                                |
| **Cómo los usuarios pueden cambiar** | Opciones de configuración regional y de idioma (solo administradores)                                                                                                                                            |
| **Valor predeterminado**              | **Windows 7 y versiones posteriores:** Idioma de la versión localizada, seguido de cualquier reserva.                                                                                                             |
| **Function**             | [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages), [ **SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)                                             |



 

## <a name="code-page"></a>Página de códigos

La incapacidad de las páginas de códigos de punto de código 256 para admitir la combinación de scripts en un solo texto era uno de los principales motivos del aumento de Unicode. Las páginas de códigos siguen siendo importantes para escribir el código de la consola, para mantener las aplicaciones heredadas o ejecutarse en versiones anteriores de Windows, y para interactuar con algún software que no sea de Microsoft que no esté habilitado para Unicode.

## <a name="input-language"></a>Idioma de entrada

El idioma de entrada se representa mediante una variable de datos por proceso que describe un idioma (por ejemplo, griego) y un método de entrada (por ejemplo, el teclado). Se pueden instalar varios idiomas de entrada y el usuario puede cambiar entre ellos.

Para establecer y recuperar el valor del idioma de entrada, la aplicación llama a [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) y [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout), respectivamente. Los usuarios pueden agregar y quitar idiomas de entrada a través de la ficha **idiomas** de la parte configuración regional y de idioma del panel de control.

El idioma de entrada predeterminado es el idioma localizado del sistema operativo y es el valor que está activo cuando se inicia una nueva aplicación (o cuando se abre una nueva ventana para algunas aplicaciones). El cambio a un idioma de entrada diferente se realiza en función de cada aplicación. En otras palabras, se pueden usar dos idiomas de entrada diferentes en dos aplicaciones diferentes. Por ejemplo, un usuario puede escribir alemán con la Estados Unidos de distribución de teclado internacional, en inglés con entrada de voz (con software que no es de Microsoft) y en español con un IME en tres aplicaciones diferentes.

## <a name="language-for-non-unicode-programs"></a>Idioma para programas no Unicode

El idioma de los programas no Unicode (antes denominados "configuración regional del sistema") determina la página de códigos que se utiliza en el sistema operativo de forma predeterminada. La configuración de idioma para programas no Unicode solo afecta a las aplicaciones no Unicode, es decir, a las aplicaciones ANSI. Establecer el idioma indica a Windows que eMule un sistema operativo no basado en Unicode, adaptado a este idioma. Al cambiar el idioma de los programas no Unicode, se instalan los archivos de fuente de mapa de bits necesarios para admitir aplicaciones no Unicode en el idioma especificado. Para permitir que el usuario seleccione un idioma para programas no Unicode, debe instalarse el grupo de idiomas adecuado. La aplicación necesita compatibilidad con el script para seleccionar un idioma para programas no Unicode. El idioma de los programas no Unicode es una configuración por sistema y requiere la implementación de un reinicio.

A veces no hay ninguna diferencia apreciable entre dos idiomas para programas no Unicode. Por ejemplo, este es el caso de las configuraciones regionales de alemán (neutro) y alemán (Austria). En general, la configuración de un grupo de idiomas es muy similar y solo difiere en la página de códigos OEM o MAC.

Una aplicación ANSI debe comprobar la configuración de idioma para programas no Unicode durante la instalación. Usa [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) o [**GetOEMCP**](/windows/desktop/api/Winnls/nf-winnls-getoemcp) para recuperar el valor. No se admite ninguna función para establecer el idioma para programas no Unicode. Sin embargo, los usuarios pueden cambiarla mediante la pestaña Opciones **avanzadas** de la parte configuración regional y de idioma del panel de control. A continuación se muestran algunos ejemplos de configuración de idioma para programas no Unicode:

1.  Un usuario de alemán que desee ejecutar una aplicación en japonés diseñada para Windows en japonés 95 debe seleccionar japonés como idioma para programas no Unicode. Después de esta selección, las aplicaciones alemanas que no son Unicode tienen problemas. Por ejemplo, la diéresis de alemán (̈) no se muestra correctamente.
2.  Un usuario de alemán que desee escribir texto en japonés en una aplicación de alemán que no sea Unicode debe seleccionar japonés como idioma para programas no Unicode. Como en el primer ejemplo, esto provoca problemas al escribir texto en alemán en aplicaciones no Unicode.
3.  Un usuario en árabe que desee escribir árabe, francés e inglés en una aplicación árabe no Unicode debe seleccionar el árabe como idioma para los programas no Unicode, ya que la página de códigos ANSI árabe contiene la mayoría de los caracteres franceses y todos los caracteres ingleses.

## <a name="language-group"></a>Grupo de idiomas

El grupo de idiomas controla el idioma para programas no Unicode, estándares y formatos, idiomas de entrada e idiomas de la interfaz de usuario que se pueden seleccionar. Para cada versión localizada, el grupo de idiomas especificado es el valor predeterminado y no se puede quitar. Por ejemplo, Windows instala el grupo de idiomas Europa occidental y Estados Unidos de forma predeterminada. Por lo tanto, si la versión en Inglés de Windows está instalada en un país o región que no esté en inglés, el usuario normalmente instalará otro grupo de idiomas.

Al agregar un grupo de idiomas, Windows copia (pero no activa) los archivos de teclado necesarios, los editores de métodos de entrada (IME), los archivos de fuente TrueType, los archivos de fuente de mapa de bits y los archivos de compatibilidad con el idioma nacional (. NLS). Agregar un grupo de idiomas también agrega valores del registro para la vinculación de fuentes e instala motores de scripting para los lenguajes de script complejos (árabe, hebreo, hindú y tailandés).

Además del grupo de idiomas de Europa occidental y Estados Unidos, hay 16 otros grupos de idiomas:



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
<td><dl> Índico<br />
Japonés<br />
Coreano<br />
Chino simplificado<br />
Chino tradicional<br />
Tailandés<br />
Lengua<br />
Vietnamita<br />
</dl></td>
</tr>
</tbody>
</table>



 

Cualquier número y combinación de grupos de idiomas se puede instalar en cualquier sistema operativo. Por ejemplo, un usuario Español puede instalar el grupo de idiomas cirílico para trabajar en textos rusos. En este caso, una aplicación de procesamiento de texto también necesita admitir el grupo de idiomas cirílico.

> [!Note]  
> Agregar el grupo de idiomas adecuado no permite automáticamente que una aplicación acepte texto. Se recomienda realizar pruebas. Por ejemplo, las aplicaciones no Unicode podrían requerir que se cambie el idioma de los programas no Unicode.

 

## <a name="location"></a>Location

**Windows XP:** Una ubicación es un identificador geográfico. Se representa mediante una variable de datos por usuario que define el país o la región donde reside el usuario.

Para establecer el valor, la aplicación llama a [**SetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-setusergeoid). Para recuperar el valor, la aplicación llama a [**GetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-getusergeoid).

## <a name="standards-and-formats"></a>Estándares y formatos

Estándares y formatos (antes "configuración regional del usuario") es una variable por usuario que determina el criterio de ordenación predeterminado y la configuración predeterminada para dar formato a fechas, horas, monedas y números. La variable se presenta como un idioma (a veces en combinación con un país o región), pero no es un idioma. Por ejemplo, si se establece la variable Standards and Formats en hebreo, se indica que el usuario desea usar las convenciones de formato de hebreo, no necesariamente el idioma hebreo. Además, la variable estándares y formatos determina la cadena que se utiliza para los nombres de los días y los meses. Por ejemplo, si un usuario muestra "25 de noviembre de 1998", la cadena "noviembre" puede cambiar en función de la variable estándares y formatos. Al cambiar la variable, se agrega automáticamente una configuración regional de entrada con la configuración predeterminada del idioma.

Para obtener el valor de la variable Standards y Formats, la aplicación llama a [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) o [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename). No hay ninguna función NLS disponible para establecer la variable. Sin embargo, los usuarios pueden cambiarlo a través de la pestaña Opciones de la **región** en la parte configuración regional y de idioma del panel de control.

Normalmente, una aplicación debe usar la configuración de las variables estándares y formatos para mostrar los datos. Sin embargo, una aplicación que usa una configuración regional fija para mostrar los datos debe pasar un identificador de configuración regional específico en lugar de usar el valor predeterminado del usuario de configuración regional \_ \_ .

## <a name="thread-locale"></a>Configuración regional de subprocesos

La configuración regional del subproceso está representada por una variable de datos de configuración regional por subproceso que determina el formato de fechas, horas, monedas y números grandes para el subproceso. De forma predeterminada, es el valor de la configuración regional seleccionada actualmente para estándares y formatos. Para establecer la configuración regional del subproceso, la aplicación llama a [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale). Para recuperar la configuración regional del subproceso, la aplicación llama a [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).

En la mayoría de los casos, no se debe sobrescribir la configuración regional del subproceso. Normalmente, solo se debe usar para sincronizar la configuración regional del subproceso de una aplicación de servidor con la variable Standards y formats de un equipo cliente. Por ejemplo, una aplicación de transacciones de acciones financieras para la bolsa de valores de Nueva York, que se utiliza en los bancos de todo el mundo, tiene que mostrar la hora, la fecha y los precios de las acciones en los formatos de Estados Unidos. Esta aplicación usa [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) para establecer la configuración regional del subproceso en inglés (Estados Unidos) y, a continuación, usa las funciones NLS para dar formato a las fechas, horas y precios de las acciones.

Cambiar la configuración regional del subproceso no afecta a todas las funciones de la API. Por lo tanto, no es siempre una manera confiable de invalidar la variable Standards y Formats. En su lugar, las aplicaciones que controlan estándares y formatos deben usar una configuración regional fija para mostrar los datos, pasando un identificador de configuración regional específico en lugar de usar la configuración regional \_ predeterminada del usuario \_ .

## <a name="nls-example"></a>Ejemplo de NLS

En el ejemplo siguiente se muestra la interacción entre estándares y formatos, el idioma de los programas no Unicode, la ubicación y el idioma de la interfaz de usuario del usuario.

Un usuario que es un nativo de Chile pero que vive en el Estados Unidos tiene un equipo que ejecuta Windows XP en inglés. El usuario establece la ubicación en Estados Unidos para utilizar un proveedor de servicios Internet (ISP) para obtener el tiempo de la Estados Unidos. Sin embargo, la variable Standards and Formats se establece en Español (Chile) para que se dé formato a la información según los estándares de chilena. Además, el usuario utiliza un procesador de textos en Coreano, que es una aplicación ANSI, de modo que el idioma de los programas no Unicode se establezca en Coreano (Corea). Para usar la aplicación, el usuario tiene un teclado en inglés y también instala un IME Coreano para admitir un segundo idioma de entrada. El compañero de trabajo del usuario, que comparte el equipo pero que no se siente cómodo con el inglés, puede establecer el idioma de la interfaz de usuario en Español (España) al usar el equipo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de la compatibilidad con National Language](about-national-language-support.md)
</dt> <dt>

[Configuraciones regionales e idiomas](locales-and-languages.md)
</dt> <dt>

[Interfaz de usuario multilingüe](multilingual-user-interface.md)
</dt> </dl>

 

 
