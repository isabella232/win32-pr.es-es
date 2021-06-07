---
title: Primera experiencia
description: En la primera experiencia ideal, los usuarios instalan el programa y lo usan de forma productiva inmediatamente, sin responder a un grupo de preguntas ni aprender un montón de cosas.
ms.assetid: d925f71c-fc5a-4ff2-8f5d-9434c162b4b4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 04610b75e8ca4ea7602d00b840bbbd9002397d9e
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524459"
---
# <a name="first-experience"></a>Primera experiencia

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

En la primera experiencia ideal, los usuarios instalan el programa y lo usan de forma productiva inmediatamente, sin responder a un grupo de preguntas ni aprender un montón de cosas.

Una interfaz de usuario de primera experiencia ayuda a los usuarios a pasar de su primera exposición a un nuevo programa o característica al uso diario.

En el caso de los programas de Windows, la primera experiencia inicial se produce cuando los usuarios ejecutan el programa de instalación. Programa de instalación normalmente:

-   Requerir que el usuario acepte un Contrato de licencia de usuario final (CLUF).
-   Pida una clave de producto.
-   Presente las opciones necesarias relacionadas con la configuración, incluida la instalación de software opcional.
-   Copie el software en el disco duro del usuario.
-   Presentar opciones de programa que se aplican a todos los usuarios.

![captura de pantalla del cuadro de diálogo "Type your product key" (Escribir la clave de producto) ](images/exper-first-exper-image1.png)

Parte de una experiencia de instalación típica de Windows.

A continuación, la primera experiencia continúa con el primer uso del programa o la característica. Esta primera experiencia de uso puede:

-   Presentar opciones de programa que solo se aplican al usuario actual.
-   Ofrecer tutoriales de productos o características.

![captura de pantalla del cuadro de diálogo "Centro de bienvenida" ](images/exper-first-exper-image2.png)

La primera experiencia de uso.

**Nota:** Las directrices relacionadas [con las opciones del](win-property-win.md) programa se presentan en un artículo independiente.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario adecuada?

Para decidirlo, tenga en cuenta las siguientes preguntas.

### <a name="setup-experience"></a>Experiencia de configuración

¿Se aplican las condiciones siguientes?

-   La configuración correcta es necesaria para usar el programa y se aplica a todos los usuarios.
-   La configuración personaliza una experiencia básica, o una que es fundamental para la identificación personal del usuario con el programa.
-   No hay ningún valor predeterminado seguro, es probable que el usuario elija una configuración que no sea la predeterminada o que la configuración predeterminada requiera el consentimiento del usuario.
-   Es poco probable que el usuario cambie la configuración después de la instalación.
-   El cambio de la configuración requiere elevación.

Si es así, considere la posibilidad de presentar la configuración durante la experiencia de configuración.

### <a name="first-use-experience"></a>Experiencia de primer uso

¿Se aplican las condiciones siguientes?

-   La configuración o las tareas correctas son necesarias para usar el programa o la característica, y se aplican a usuarios individuales.
-   La configuración personaliza una experiencia básica, o una que es fundamental para la identificación personal del usuario con el programa.
-   No hay ningún valor predeterminado seguro, es probable que el usuario elija una configuración que no sea la predeterminada o que la configuración predeterminada requiera el consentimiento del usuario.
-   Es probable que los usuarios to make better choices within the context of the program than within setup.
-   Es poco probable que el usuario cambie la configuración mediante Opciones.

Si es así, considere la posibilidad de presentar las tareas y la configuración durante la primera experiencia de uso del programa o la característica.

## <a name="design-concepts"></a>Conceptos de diseño

En la primera experiencia ideal, los usuarios instalan el programa (o incluso simplemente lo inician si no requiere instalación) y lo usan de forma productiva inmediatamente sin responder a un grupo de preguntas o aprender un montón de cosas.

Este ideal se puede obtener para la mayoría de los programas, por lo que debe procurar esta experiencia ideal siempre que pueda. Sin embargo, este objetivo a menudo no se puede obtener para los programas que requieren una integración significativa del sistema, tienen muchas características opcionales o tienen implicaciones en la privacidad. Por ejemplo, si el programa tiene características que podrían revelar información [](https://www.microsoft.com/mscorp/twc/default.mspx) personal a terceros que no son de confianza, los principios de la informática de confianza requieren que obtenga el consentimiento del usuario antes de habilitar estas características.

### <a name="questions-arent-choices"></a>Las preguntas no son opciones

Las preguntas requieren respuestas que deben responderse antes de que los usuarios puedan continuar. Las preguntas durante la primera experiencia son obstáculos que los usuarios deben saltar para poder usar el programa de forma productiva. Por el contrario, las opciones son opcionales. Los usuarios no tienen que responder a ellos o pueden elegir verlos solo cuando quieran.

Por lo tanto, la configuración que se presenta en el flujo principal de un asistente para la instalación son preguntas, mientras que la configuración fuera del flujo de instalación principal o en un cuadro de diálogo de opciones de programa son opciones. Las preguntas innecesarias hacen que la primera experiencia del programa sea complicada y larga, lo que elimina de forma eficaz la anticipación positiva y los usuarios emocionantes tienen que empezar a trabajar con el programa.

### <a name="use-the-first-experience-when-you-must"></a>Use la primera experiencia cuando deba

Presente la configuración y las tareas a los usuarios durante las primeras experiencias cuando sea necesario, pero normalmente hay mejores alternativas:



| Primera experiencia  | Alternativas       |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Preguntas de configuración<br/>                  | Seleccione los valores predeterminados adecuados.<br/> Permitir que los usuarios cambien de las opciones del programa.<br/> Proporcione rutas de instalación típicas frente a rutas de instalación personalizadas. <br/> |
| Preguntas de primer uso<br/>              | Seleccione los valores predeterminados adecuados y permita que los usuarios cambien de las opciones del programa.<br/>                                                            |
| Tareas de primer uso<br/>                  | En su lugar, presente contextualmente.<br/>                                                                                                           |
| Anuncios de características de primer uso<br/> | Hacer que las tareas más comunes e importantes se detecte y contextualmente.<br/>                                                                   |
| Tutoriales de primer uso<br/>              | Haga que las características del programa se explican por sí solas.<br/>                                                                                                 |
| Registro de productos<br/>             | Proporcione el comando en el menú Ayuda y en el cuadro Acerca de.<br/>                                                                                             |



 

**Si solo hace una cosa...**

Mantenga su primera experiencia lo más sencilla posible. Haga que el programa funcione de inmediato. Elija valores predeterminados seguros, seguros y prácticos y haga preguntas durante la instalación y el primer uso solo cuando sea necesario.

Solo tiene una oportunidad de crear una buena primera impresión y esa primera impresión es duradera.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Limite las primeras experiencias a las tareas y la configuración necesarias para usar un programa o una característica, y solo incluya estas experiencias cuando no haya ninguna alternativa mejor.** Consulte la tabla anterior para ver alternativas.
    -   **Excepción:** Agregue la personalización o la configuración de personalización del programa a la primera experiencia si su personalización forma parte de la experiencia principal o es fundamental para la identificación personal del usuario con el programa.

![captura de pantalla del cuadro de diálogo "Type a computer name" (Escribir un nombre de equipo) ](images/exper-first-exper-image3.png)

Windows pide a los usuarios el nombre del equipo y la elección del fondo durante la instalación, ya que esta configuración ayuda a formar una conexión emocional con el producto.

-   **Use la experiencia de configuración para** tareas y configuraciones si se aplican a todos los usuarios o si cambiar la configuración requiere elevación.
-   **Use la primera experiencia de uso para** las tareas y la configuración si se aplican a usuarios individuales.

### <a name="presentation"></a>Presentación

-   **Prefiere las tareas y la configuración opcionales a las tareas y configuraciones necesarias.** Evite forzar a los usuarios a configurar el programa.

    ![captura de pantalla del cuadro de diálogo "Nuevo hardware encontrado" ](images/exper-first-exper-image4.png)

    El cuadro de diálogo Nuevo hardware encontrado hace que sea opcional instalar software de controlador en lugar de convertirla en una tarea necesaria.

-   **Tome tareas y configuraciones opcionales del flujo de tareas principal siempre que sea práctico.** Por ejemplo, muchos programas de instalación proporcionan una ruta de instalación personalizada para quitar la configuración cambiada con poca frecuencia del flujo de tareas principal.

    ![captura de pantalla de botones de radio completos y personalizados ](images/exper-first-exper-image5.png)

    Una experiencia de configuración que facilita el flujo de tareas principales si el usuario no pretende personalizar la instalación.

-   **No sobrecargar a los usuarios con tareas y configuraciones:**
    -   **Empiece por algo simple.** Comience con una configuración sencilla de personalización y avance hacia tareas y configuraciones más complejas y técnicas. Por ejemplo, el programa de instalación de Windows comienza con información personal y termina con la configuración de red.
    -   **Use una primera experiencia contextual para** las tareas y la configuración si solo se aplican a características que no son fundamentales para el programa principal.

        ![captura de pantalla del cuadro de diálogo "Configuración de audio y vídeo" ](images/exper-first-exper-image6.png)

        Windows Live Messenger tiene una configuración contextual para audio y vídeo porque las usan las características secundarias.

-   **No presente todo a la vez.** Consolide para usar una sola interfaz de usuario en lugar de varias superficies de interfaz de usuario, o bien muestre tareas en momentos diferentes en lugar de todas a la vez.

    **Incorrecto:**

    ![captura de pantalla de cinco cuadros de diálogo superpuestos ](images/exper-first-exper-image7.png)

    En este ejemplo, la primera experiencia de uso es abrumadora.

-   **Expresar preguntas y opciones en términos de objetivos y tareas de los usuarios, no en términos de tecnología.** Proporcione opciones que los usuarios entiendan y diferencian claramente. Asegúrese de proporcionar suficiente información a los usuarios para tomar decisiones informadas.
-   **Si la necesidad de información personal no es obvia, explique por qué el programa necesita la información y cómo se usará.**

    ![captura de pantalla de texto que indica el uso de la dirección de correo electrónico ](images/exper-first-exper-image8.png)

    En este ejemplo, una aplicación de comercio electrónico explica cómo se usará la información personal.

-   **Presentar las primeras experiencias a pantalla completa solo si los usuarios no pueden realizar otras tareas de forma productiva.** Por ejemplo, el programa de instalación de Windows se presenta a pantalla completa para disuadir a los usuarios de realizar otras tareas mientras se instala Windows. La mayoría de las primeras experiencias no deben ser de pantalla completa.

### <a name="settings"></a>Configuración

-   **Para todas las configuraciones, seleccione el valor más seguro (para evitar la pérdida de datos o del sistema), el valor más seguro y privado de forma predeterminada.** Si la seguridad y la seguridad no son factores, seleccione el valor más probable o conveniente. Elegir valores predeterminados buenos es una manera eficaz de simplificar la primera experiencia.
-   **Requerir que los usuarios opten por:**

    -   Configuración con implicaciones legales, como contratos de licencias de usuario final (EUA). Esta configuración no puede tener selecciones predeterminadas.
    -   Características que realizan cambios automáticos en la configuración del sistema, como las actualizaciones automáticas de Windows.
    -   Características que revelan información de identificación personal (PII) o información del sistema.
    -   Cambios en el escritorio del usuario más allá de agregar entradas al menú Inicio, como agregar iconos al escritorio o a la barra de inicio rápido.
    -   Software opcional, como mejoras de productos, suscripciones y productos de terceros.

    ![captura de pantalla del cuadro de diálogo Elegir características que quiera ](images/exper-first-exper-image9.png)

    En este ejemplo, los usuarios optan por mejoras de productos, suscripciones y productos de terceros.

-   **Si se recomienda encarecidamente una configuración, agregue "(recommended)" a la etiqueta.** En el caso de los botones de radio y las casillas, asegúrese de agregar a la etiqueta de control, no a las notas complementarias.
-   **Si una configuración está pensada solo para usuarios avanzados, agregue "(advanced)" a la etiqueta.** En el caso de los botones de radio y las casillas, asegúrese de agregar a la etiqueta de control, no a las notas complementarias.

### <a name="tasks"></a>Tareas

-   **Ayudar a los usuarios a superar el tiempo de espera de forma productiva.**
    -   Si el tiempo de espera suele oscilar entre uno y dos minutos, considere la posibilidad de proporcionar información útil mientras los usuarios esperan, como una presentación de las novedades durante la instalación.
    -   Si el tiempo de espera suele ser superior a dos minutos, facilita a los usuarios la realización de otras tareas. Muestre el tiempo de espera estimado, recomiende que los usuarios hagan otra cosa mientras tanto y que la finalización de la tarea sea obvia cambiando significativamente la pantalla.
-   **Replantearse la presentación de tutoriales durante la primera experiencia.** Lo más probable es que los usuarios quieran usar el programa de inmediato y estén interesados en los tutoriales en un momento posterior.
-   **No use notificaciones de anuncios de características en la primera experiencia.** En lugar de usar una notificación de anuncio de [características,](mess-notif.md)diseñe la característica para que sea más fácil de detectar en contextos en los que sea necesaria o no haga nada especial y permita que los usuarios descubran la característica por sí mismos.
-   **No use ninguna notificación durante la experiencia inicial de Windows.** Para mejorar su primera experiencia, Windows 7 suprime todas las notificaciones mostradas durante las primeras horas de uso. Diseñe el programa suponiendo que los usuarios no verán dichas notificaciones.

 

