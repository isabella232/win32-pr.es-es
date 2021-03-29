---
title: Definir un nuevo carácter
description: Definir un nuevo carácter
ms.assetid: 4102cb7d-2fec-45d2-882a-04704c7f5a48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586312ac9d913a27d2df0be112cbcf92c47f4fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994348"
---
# <a name="defining-a-new-character"></a>Definir un nuevo carácter

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Para definir un nuevo carácter, ejecute el editor de caracteres del agente. Si tiene cargado un archivo de caracteres, elija el **nuevo** comando en el menú **archivo** . Esto muestra un submenú de opciones. Si crea un carácter para su propio uso, elija **carácter personalizado**. Si desea crear un carácter que se puede usar como un carácter predeterminado del agente, elija **carácter predeterminado**. Esto configurará previamente el editor con todos los nombres de animación y las asignaciones de estado de animación necesarios, así como establecer la opción **compatible con el conjunto de animaciones estándar** . Del mismo modo, si elige el carácter del ayudante de Office, el editor se configura previamente con los nombres de animación y la asignación de estado de animación necesarios para un carácter del ayudante de Office. Esta acción selecciona el icono de **carácter** en el árbol y muestra las páginas de propiedades en el lado derecho de la ventana. En las secciones siguientes se describe cómo establecer las propiedades del carácter y cómo crear animaciones para el carácter.

### <a name="setting-your-characters-general-information"></a>Establecer la información general del carácter

Para empezar a definir un carácter, escriba el nombre del carácter en el cuadro de texto **nombre** (máximo de 32 caracteres). Dado que el agente de Microsoft usa el nombre para permitir que los usuarios tengan acceso al carácter, especifique un nombre descriptivo. Proporcione un nombre que se pueda pronunciar mediante la ortografía convencional o puede deshabilitar la entrada de voz para el carácter. También puede especificar una breve descripción opcional (256 caracteres) para el carácter en el cuadro de texto Descripción. El servidor expone lo que se escribe en el cuadro de texto Descripción a las aplicaciones cliente.

También puede almacenar sus propios datos como parte del carácter mediante el campo ExtraData. Puede usar esta funcionalidad para incluir información especial sobre el carácter u otros datos. Una vez compilada con el editor de caracteres, se puede tener acceso a esta información utilizando la propiedad ExtraData en tiempo de ejecución cuando se carga el carácter.

Puede establecer el nombre, la descripción y la información adicional de datos del carácter en función del valor del identificador de idioma del carácter. Para establecer estos datos para otro idioma, seleccione idioma y escriba el texto. También debe tener instaladas las páginas de códigos de idioma en el sistema para compilar el archivo de caracteres. Si no la configuración de idioma adecuada no se incluirá en el archivo de caracteres compilados. No es necesario proporcionar información en otros idiomas. Si estas propiedades se consultan en tiempo de ejecución mediante la API del agente y no hay ninguna configuración específica para ese idioma, se devuelve la configuración de inglés (valor predeterminado).

### <a name="setting-your-characters-output-options"></a>Establecer las opciones de salida de los caracteres

Si establece la opción compatible con el conjunto de animaciones estándar, el editor de caracteres comprobará que ha incluido todas las animaciones necesarias y las asignaciones de estado de animación para un carácter predeterminado al intentar generar el carácter. Si falta algo, aparecerá un cuadro de mensaje en el que se enumerarán los elementos que faltan. Para obtener más información sobre el conjunto de animaciones estándar, vea [**diseñar caracteres para el agente de Microsoft**](designing-characters-for-microsoft-agent.md).

En el caso de la salida hablada del carácter, el agente de Microsoft ofrece la opción de una voz sintetizada, de texto a voz (TTS) o una voz que utiliza archivos de sonido grabados. Si desea usar una voz sintetizada, active la opción usar voz sintetizada para la salida de voz. Se agregará una página de voz para seleccionar las características de la voz. Elija la página voz y use la página controles en ella para seleccionar una voz, una velocidad y un tono de cualquier motor de TTS compatible que haya instalado. El intervalo de parámetros de voz que puede seleccionar depende de los motores TTS. Si aún no ha instalado un motor TTS, la lista ID. de voz estará vacía. Debe tener un motor de TTS instalado antes de definir la configuración de voz del carácter en el editor de caracteres del agente.

Si tiene previsto usar un motor TTS para la salida de su carácter, también debe instalar el motor en el sistema del usuario. Si selecciona una voz basada en un motor TTS determinado, pero el usuario tiene instalado otro motor TTS, el servidor intentará hacer coincidir la voz en función de las características que haya definido en el editor de caracteres del agente.

Si piensa usar archivos de sonido grabados (. WAV) para la salida hablada de su carácter, no es necesario que active la opción usar voz sintetizada para la salida de voz. En su lugar, tendrá que registrar los archivos de audio de salida hablados por separado y cargarlos desde el código de la aplicación.

La opción usar **globo de palabras** le permite determinar si desea admitir un globo de palabras para el carácter. Esta característica también se puede establecer en tiempo de ejecución.

Cuando se activa la opción **usar globo de palabras** , puede tener acceso a la página de **globo de palabras** . Las opciones de la página de **globo de palabras** permiten cambiar las características predeterminadas del globo de palabras. La configuración **caracteres por línea** permite definir el ancho del globo en función del número promedio de caracteres por línea. Puede establecer el alto predeterminado en función de un número fijo de líneas que desee que se muestren al mismo tiempo o de tamaño automático para el texto que proporcione en el método [**Speak**](speak-method.md) . También puede establecer si el globo se oculta automáticamente después de que se complete un método **Speak** y si el globo muestra automáticamente o "Pace" las palabras a la configuración de la velocidad de salida de voz del carácter.

La página de **globo de palabras** también le permite establecer la fuente predeterminada para el globo de palabras del carácter y los colores de visualización del globo. Sin embargo, tenga en cuenta que los usuarios pueden invalidar la configuración de fuente de globo de palabras mediante la hoja de propiedades del agente de Microsoft.

### <a name="setting-your-characters-identifier"></a>Establecer el identificador del carácter

Cada carácter requiere un identificador único (GUID). El servidor utiliza el identificador para diferenciar los caracteres. Al crear un nuevo carácter, el editor crea automáticamente un nuevo identificador para el carácter. Solo debe cambiar el identificador de un carácter si ha copiado el archivo de definición de caracteres de otro carácter o si desea diferenciar intencionadamente un carácter de una versión anterior. Para cambiar el identificador de un carácter, haga clic en el botón nuevo GUID y el editor generará un nuevo identificador.

 

 




