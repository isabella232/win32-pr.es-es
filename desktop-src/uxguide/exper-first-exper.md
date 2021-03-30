---
title: Primera experiencia
description: En la primera experiencia ideal, los usuarios instalan el programa y lo usan de forma productiva de inmediato, sin tener que responder a un montón de preguntas o aprender un montón de cosas.
ms.assetid: d925f71c-fc5a-4ff2-8f5d-9434c162b4b4
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: c965ae77507b0041d17cabb34c4f53dc8216c134
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104279754"
---
# <a name="first-experience"></a>Primera experiencia

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

En la primera experiencia ideal, los usuarios instalan el programa y lo usan de forma productiva de inmediato, sin tener que responder a un montón de preguntas o aprender un montón de cosas.

Una interfaz de usuario de primera experiencia ayuda a los usuarios a pasar de su primera exposición a un nuevo programa o característica a un uso cotidiano.

En el caso de los programas de Windows, la primera experiencia inicial se produce cuando los usuarios ejecutan el programa de instalación. Programas de instalación normalmente:

-   Requerir al usuario que acepte un contrato de licencia para el usuario final (CLUF).
-   Pida una clave de producto.
-   Presente las opciones relacionadas con la configuración requeridas, incluida la instalación de software opcional.
-   Copie el software en el disco duro del usuario.
-   Presenta las opciones del programa que se aplican a todos los usuarios.

![captura de pantalla del cuadro de diálogo ' escriba su clave de producto ' ](images/exper-first-exper-image1.png)

Parte de una experiencia de instalación de Windows típica.

La primera experiencia continúa en el primer uso del programa o la característica. Esta primera experiencia de uso puede:

-   Presenta las opciones del programa que se aplican solo al usuario actual.
-   Ofrezca tutoriales de productos o características.

![captura de pantalla del cuadro de diálogo ' Bienvenido Center ' ](images/exper-first-exper-image2.png)

La primera experiencia de uso.

**Nota:** Las instrucciones relacionadas con [las opciones del programa](win-property-win.md) se presentan en un artículo independiente.

## <a name="is-this-the-right-user-interface"></a>¿Es la interfaz de usuario correcta?

Para decidir, tenga en cuenta las siguientes preguntas.

### <a name="setup-experience"></a>Experiencia de instalación

¿Se aplican las siguientes condiciones?

-   Los valores correctos son necesarios para usar el programa y se aplican a todos los usuarios.
-   La configuración personaliza una experiencia principal o una que es fundamental para la identificación personal del usuario con el programa.
-   No hay ningún valor predeterminado seguro, es probable que el usuario elija valores que no sean los predeterminados o que la configuración predeterminada requiera el consentimiento del usuario.
-   No es probable que el usuario cambie la configuración después de la instalación.
-   El cambio de la configuración requiere elevación.

Si es así, considere la posibilidad de presentar la configuración durante la experiencia de instalación.

### <a name="first-use-experience"></a>Experiencia de primer uso

¿Se aplican las siguientes condiciones?

-   La configuración o las tareas correctas son necesarias para usar el programa o la característica y se aplican a usuarios individuales.
-   La configuración personaliza una experiencia principal o una que es fundamental para la identificación personal del usuario con el programa.
-   No hay ningún valor predeterminado seguro, es probable que el usuario elija valores que no sean los predeterminados o que la configuración predeterminada requiera el consentimiento del usuario.
-   Es probable que los usuarios realicen mejores elecciones en el contexto del programa que en la instalación.
-   No es probable que el usuario cambie la configuración mediante opciones.

Si es así, considere la posibilidad de presentar las tareas y la configuración durante la primera experiencia de uso del programa o la característica.

## <a name="design-concepts"></a>Conceptos de diseño

En la primera experiencia ideal, los usuarios instalan el programa (o incluso lo inician si no se requiere la instalación) y lo usan de forma productiva de inmediato sin responder a un montón de preguntas o aprender un montón de cosas.

Esta solución ideal se obtiene para la mayoría de los programas, por lo que debe procurar esta experiencia ideal siempre que pueda. Sin embargo, este objetivo no suele obtenerse para los programas que requieren una integración significativa del sistema, tienen muchas características opcionales o tienen implicaciones de privacidad. Por ejemplo, si el programa tiene características que podrían revelar información personal a partes que no son de confianza, los principios de la [informática de confianza](https://www.microsoft.com/mscorp/twc/default.mspx) requieren que obtenga el consentimiento del usuario antes de habilitar estas características.

### <a name="questions-arent-choices"></a>Las preguntas no son elecciones

Las preguntas requieren respuestas que deben responder antes de que los usuarios puedan continuar. Las preguntas que se produzcan durante la primera experiencia son los obstáculos que los usuarios deben saltar antes de que puedan usar su programa de manera productiva. Por el contrario, las opciones son opcionales. Los usuarios no tienen que responder a ellos o pueden verlos solo cuando lo desean.

Por lo tanto, los valores que se presentan en el flujo principal de un asistente para la instalación son preguntas, mientras que los valores que se encuentran fuera del flujo de configuración principal o de un cuadro de diálogo Opciones de programa son opciones. Las preguntas innecesarias hacen que la primera experiencia del programa sea complicada y larga, lo que elimina de forma eficaz la anticipación positiva y los usuarios emocionantes tienen que empezar a trabajar con el programa.

### <a name="use-the-first-experience-when-you-must"></a>Use la primera experiencia cuando deba

Presente la configuración y las tareas a los usuarios durante las primeras experiencias cuando sea necesario, pero normalmente hay mejores alternativas:



|                                             |                                                                                                                                                    |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Primera experiencia**<br/>             | **Alternativas**<br/>                                                                                                                        |
| Preguntas de configuración<br/>                  | Seleccione los valores predeterminados adecuados.<br/> Permitir a los usuarios cambiar desde opciones del programa.<br/> Proporcione rutas de instalación típicas y personalizadas. <br/> |
| Preguntas de primer uso<br/>              | Seleccione los valores predeterminados adecuados y permita que los usuarios cambien de las opciones del programa.<br/>                                                            |
| Primeras tareas de uso<br/>                  | Presente en su lugar contextualmente.<br/>                                                                                                           |
| Primer uso de anuncios de características<br/> | Haga que las tareas más comunes y importantes sean reconocibles y contextuales.<br/>                                                                   |
| Primer uso de tutoriales<br/>              | Haga que las características del programa sean autoexplicativas.<br/>                                                                                                 |
| Registro del producto<br/>             | Proporcione el comando en el menú ayuda y el cuadro acerca de.<br/>                                                                                             |



 

**Si solo hace algo...**

Mantenga su primera experiencia lo más sencilla posible. Consiga que el programa funcione de inmediato. Elija los valores predeterminados seguros, seguros y cómodos y formule preguntas durante la instalación y use primero solo cuando sea necesario.

Solo tiene una oportunidad para crear una buena impresión y esa primera impresión es duradera.

## <a name="guidelines"></a>Directrices

### <a name="general"></a>General

-   **Limite las experiencias primeras a las tareas y la configuración necesarias para usar un programa o una característica, y solo incluirlas cuando no haya ninguna alternativa mejor.** Vea la tabla anterior para ver alternativas.
    -   **Excepción:** Agregue la configuración de personalización o personalización de programas a la primera experiencia si su personalización forma parte de la experiencia principal o fundamental para la identificación personal del usuario con el programa.

![captura de pantalla del cuadro de diálogo ' escribir un nombre de equipo ' ](images/exper-first-exper-image3.png)

Windows solicita al usuario el nombre del equipo y la opción de fondo durante la instalación, ya que estas opciones de configuración le ayudan a establecer una conexión emocional con el producto.

-   **Utilice la experiencia de instalación** para las tareas y la configuración si se aplican a todos los usuarios o si cambia la configuración requiere elevación.
-   **Use la primera experiencia de uso** para las tareas y la configuración si se aplican a usuarios individuales.

### <a name="presentation"></a>Presentación

-   **Prefiere tareas y configuraciones opcionales a las tareas y configuraciones necesarias.** Evite obligar a los usuarios a configurar el programa.

    ![captura de pantalla del cuadro de diálogo "se encontró el nuevo hardware" ](images/exper-first-exper-image4.png)

    El cuadro de diálogo nuevo hardware encontrado hace que sea opcional instalar el software de controlador en lugar de convertirlo en una tarea necesaria.

-   **Realice tareas y configuraciones opcionales fuera del flujo de tareas principal siempre que sea práctico.** Por ejemplo, muchos programas de instalación proporcionan una ruta de instalación personalizada para quitar la configuración modificada con poca frecuencia del flujo de tareas principal.

    ![captura de pantalla de botones de radio completos y personalizados ](images/exper-first-exper-image5.png)

    Una experiencia de instalación que facilita el flujo de tareas principal si el usuario no tiene previsto personalizar la instalación.

-   **No sobrecargar a los usuarios con tareas y configuraciones:**
    -   **Empiece por algo simple.** Comience con una configuración de personalización y un progreso sencillos hacia tareas y configuraciones más complejas y técnicas. Por ejemplo, el programa de instalación de Windows se inicia con información personal y termina con la configuración de red.
    -   **Use una primera experiencia contextual** para las tareas y la configuración si solo se aplican a las características que no son fundamentales para el programa principal.

        ![captura de pantalla del cuadro de diálogo Configuración de audio y vídeo ](images/exper-first-exper-image6.png)

        Windows Live Messenger tiene una configuración contextual para audio y vídeo porque lo usan las características secundarias.

-   **No presente todo de una vez.** Consolide para usar una sola interfaz de usuario en lugar de varias superficies de la interfaz de usuario o para mostrar las tareas en distintos momentos en lugar de todos a la vez.

    **Incorrecto:**

    ![captura de pantalla de cinco cuadros de diálogo superpuestos ](images/exper-first-exper-image7.png)

    En este ejemplo, la primera experiencia de uso es abrumadora.

-   **Exprese las preguntas y las opciones en cuanto a los objetivos y las tareas de los usuarios, no en términos de tecnología.** Proporcionar opciones que los usuarios entienden y diferencian claramente. Asegúrese de proporcionar información suficiente para que los usuarios tomen decisiones informadas.
-   **Si la necesidad de información personal no es obvia, explique por qué el programa necesita la información y cómo se va a usar.**

    ![captura de pantalla de texto que indica el uso de la dirección de correo electrónico ](images/exper-first-exper-image8.png)

    En este ejemplo, una aplicación de comercio electrónico explica cómo se utilizará la información personal.

-   **Presente las primeras experiencias solo en la pantalla completa si los usuarios no pueden realizar otras tareas de manera productiva.** Por ejemplo, el programa de instalación de Windows se presenta a pantalla completa para impedir que los usuarios realicen otras tareas mientras se instala Windows. La mayoría de las experiencias primeras no deben ser de pantalla completa.

### <a name="settings"></a>Configuración

-   **Para todas las opciones de configuración, seleccione la más segura (para evitar la pérdida de datos o el acceso al sistema), el valor más seguro y privado de forma predeterminada.** Si seguridad y seguridad no son factores, seleccione el valor más probable o adecuado. Elegir buenos valores predeterminados es una manera eficaz de simplificar la primera experiencia.
-   **Requerir a los usuarios que participen en:**

    -   Configuración con implicaciones legales, como los contratos de licencia para el usuario final (CLUF). Esta configuración no puede tener selecciones predeterminadas.
    -   Características que realizan cambios de configuración automáticos del sistema, como actualizaciones automáticas de Windows.
    -   Características que revelan información de identificación personal (PII) o información del sistema.
    -   Cambios en el escritorio del usuario más allá de agregar entradas al menú Inicio, como agregar iconos al escritorio o a la barra de inicio rápido.
    -   Software opcional, como mejoras de productos, suscripciones y productos de terceros.

    ![captura de pantalla del cuadro de diálogo elegir características que desea ](images/exper-first-exper-image9.png)

    En este ejemplo, los usuarios optan por las mejoras del producto, las suscripciones y los productos de terceros.

-   **Si se recomienda un valor de configuración, agregue "(recomendado)" a la etiqueta.** En el caso de los botones de radio y las casillas, asegúrese de agregar a la etiqueta de control, no a las notas complementarias.
-   **Si una configuración está destinada solo a usuarios avanzados, agregue "(avanzado)" a la etiqueta.** En el caso de los botones de radio y las casillas, asegúrese de agregar a la etiqueta de control, no a las notas complementarias.

### <a name="tasks"></a>Tareas

-   **Ayudar a los usuarios a pasar el tiempo de espera de manera productiva.**
    -   Si el tiempo de espera está normalmente entre uno y dos minutos, considere la posibilidad de proporcionar información útil mientras los usuarios están esperando, como una presentación de las novedades durante la instalación.
    -   Si el tiempo de espera es normalmente superior a dos minutos, facilite a los usuarios que realicen otras tareas. Mostrar el tiempo de espera estimado, se recomienda que los usuarios hagan algo más mientras tanto, y que la finalización de la tarea sea obvia cambiando la pantalla de forma significativa.
-   **Considere la posibilidad de presentar tutoriales durante la primera experiencia.** Lo más probable es que los usuarios quieran usar su programa de inmediato y estén interesados en los tutoriales en un momento posterior.
-   **No use las notificaciones de anuncios de características en la primera experiencia.** En lugar de usar una [notificación de anuncios de características](mess-notif.md), diseñe la característica para que sea más fácil de detectar en contextos donde sea necesario o no haga nada especial y deje que los usuarios detecten la característica por su cuenta.
-   **No utilice ninguna notificación durante la experiencia inicial de Windows.** Para mejorar su primera experiencia, Windows 7 suprime todas las notificaciones que se muestran en las primeras horas de uso. Diseñe el programa, suponiendo que los usuarios no vean estas notificaciones.

 

