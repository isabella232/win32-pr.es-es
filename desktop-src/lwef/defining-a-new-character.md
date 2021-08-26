---
title: Definir un nuevo carácter
description: Definir un nuevo carácter
ms.assetid: 4102cb7d-2fec-45d2-882a-04704c7f5a48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1f3d9aee78893ebc4796781947be92366baa10b9ad1e123a73121df24646ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963105"
---
# <a name="defining-a-new-character"></a>Definir un nuevo carácter

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Para definir un carácter nuevo, ejecute el Editor de caracteres del agente. Si tiene un archivo de caracteres existente cargado, elija el **comando Nuevo** en el **menú** Archivo. Esto muestra un submenú de opciones. Si crea un carácter para su propio uso, elija **Carácter personalizado.** Si desea crear un carácter que se pueda usar como carácter predeterminado del Agente, elija **Carácter predeterminado.** Esto configurará previamente el editor con todos los nombres de animación y asignaciones de estado de animación necesarios, así como establecerá la opción **Supports Standard Animation Set (Admite** conjunto de animaciones estándar). Del mismo modo, si elige Office Assistant Character (Carácter del asistente), el editor está preconfigurado con los nombres de animación y la asignación de estado de animación necesarios para un carácter Office Assistant. Esta acción selecciona el icono **Carácter** del árbol y muestra sus páginas de propiedades en el lado derecho de la ventana. En las secciones siguientes se describe cómo establecer las propiedades del carácter y cómo crear animaciones para el carácter.

### <a name="setting-your-characters-general-information"></a>Establecimiento de la información general del carácter

Para empezar a definir un carácter, escriba el nombre del carácter en el **cuadro de** texto Nombre (32 caracteres como máximo). Dado que Microsoft Agent usa el nombre para permitir que los usuarios accedan al carácter, especifique un nombre descriptivo. Proporcione un nombre que se pueda pronunciar con ortografía convencional, o bien puede deshabilitar la entrada de voz para el carácter. También puede especificar una breve descripción opcional (256 caracteres) para el carácter en el cuadro de texto Descripción. El servidor expone lo que escriba en el cuadro de texto Descripción a las aplicaciones cliente.

También puede almacenar sus propios datos como parte del carácter mediante el campo ExtraData. Puede usar esta funcionalidad para incluir información especial sobre el carácter u otros datos. Una vez compilado con el Editor de caracteres, se puede acceder a esta información mediante la propiedad ExtraData en tiempo de ejecución cuando se carga el carácter.

Puede establecer el nombre, la descripción y la información de datos adicionales del carácter en función de la configuración del identificador de idioma del carácter. Para establecer estos datos para otro idioma, seleccione Idioma y escriba el texto. También debe tener instaladas las páginas de códigos de idioma en el sistema donde se compila el archivo de caracteres. Si no lo hace, la configuración de idioma adecuada no se incluirá en el archivo de caracteres compilado. No es necesario proporcionar información en otros idiomas. Si estas propiedades se consultan en tiempo de ejecución mediante la API del agente y no hay ninguna configuración específica para ese idioma, se devuelve la configuración de inglés (valor predeterminado).

### <a name="setting-your-characters-output-options"></a>Establecer las opciones de salida del carácter

Si establece la opción Supports Standard Animation Set (Admite conjunto de animaciones estándar), el Editor de caracteres comprobará que ha incluido todas las animaciones y asignaciones de estado de animación necesarias para un carácter predeterminado al intentar compilar el carácter. Si falta algo, un cuadro de mensaje mostrará los elementos que faltan. Para obtener más información sobre el conjunto de animaciones estándar, [**vea Designing Characters for Microsoft Agent**](designing-characters-for-microsoft-agent.md).

Para la salida hablada del carácter, Microsoft Agent proporciona la opción de una voz sintetizada de texto a voz (TTS) o una voz que usa archivos de sonido grabados. Si desea usar una voz sintetizada, active la opción Usar voz sintetizada para la salida de voz. Esto agregará una página Voz para seleccionar las características de la voz. Elija la página Voz y use los controles de la página para seleccionar una voz, velocidad y tono de los motores TTS compatibles que haya instalado. El intervalo de parámetros de voz que puede seleccionar depende de los motores de TTS. Si aún no ha instalado un motor de TTS, la lista de identificadores de voz estará vacía. Debe tener un motor de TTS instalado antes de definir la configuración de voz del carácter en el Editor de caracteres del agente.

Si tiene previsto usar un motor de TTS para la salida del carácter, también debe instalar ese motor en el sistema del usuario. Si selecciona una voz basada en un motor de TTS determinado, pero el usuario tiene un motor de TTS diferente instalado, el servidor intenta coincidir con la voz en función de las características definidas en el Editor de caracteres del agente.

Si tiene previsto usar archivos de sonido grabados (. Archivos WAV) para la salida hablada del carácter, no es necesario comprobar la opción Usar voz sintetizada para la salida de voz. En su lugar, deberá grabar los archivos de audio de salida hablados por separado y cargarlos desde el código de la aplicación.

La opción **Usar globo** de palabras le permite determinar si desea admitir un globo de palabras para el carácter. Esta característica también se puede establecer en tiempo de ejecución.

Cuando se **activa la opción Usar globo** de palabras, puede acceder a la página Globo **de** palabras. Las opciones de la **página Globo** de palabras permiten cambiar las características predeterminadas del globo de palabras. El **valor Caracteres por** línea permite definir el ancho del globo en función del número medio de caracteres por línea. Puede establecer el alto predeterminado en función de un número fijo de líneas que quiera mostrar a la vez o ajustar automáticamente el tamaño del texto que proporcione en el [**método Speak.**](speak-method.md) También puede establecer si el globo se oculta automáticamente una vez completado un método **Speak** y si el globo muestra automáticamente o "marca" las palabras a la configuración de velocidad de salida de voz del carácter.

La **página Globo** de palabras también permite establecer la fuente predeterminada para el globo de palabras del carácter y los colores para mostrar del globo. Sin embargo, tenga en cuenta que los usuarios pueden invalidar la configuración de fuente del globo de palabras mediante la hoja de propiedades de Microsoft Agent.

### <a name="setting-your-characters-identifier"></a>Establecer el identificador del carácter

Cada carácter requiere un identificador único (GUID). El servidor usa el identificador para diferenciar caracteres. Cuando se crea un carácter, el Editor crea automáticamente un nuevo identificador para el carácter. Solo debe cambiar el identificador de un carácter si copió el archivo de definición de caracteres de otro carácter o si desea diferenciar intencionadamente un carácter de una versión anterior. Para cambiar el identificador de un carácter, haga clic en el botón Nuevo GUID y el Editor generará un identificador nuevo.

 

 




