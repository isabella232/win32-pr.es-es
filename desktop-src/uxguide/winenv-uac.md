---
title: Control de cuentas de usuario (aspectos básicos del diseño)
description: Una experiencia de control de cuentas de usuario bien diseñada ayuda a evitar cambios no deseados en todo el sistema de una forma predecible y requiere un esfuerzo mínimo.
ms.assetid: c4b83537-c600-4b24-bda6-df7a82719ab1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: b346e5cb581ac83ad2ebffabe73c5fbed636d814
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "104570656"
---
# <a name="user-account-control"></a>Control de cuentas de usuario

> [!NOTE]
> Esta guía de diseño se ha creado para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de la guía se sigue aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [Guía de diseño actual](/windows/uwp/design/).

Una experiencia de control de cuentas de usuario bien diseñada ayuda a evitar cambios no deseados en todo el sistema de una forma predecible y requiere un esfuerzo mínimo.

Con el control de cuentas de usuario (UAC) totalmente habilitado, los administradores interactivos normalmente se ejecutan con menos privilegios de usuario, pero pueden realizar una elevación automática para llevar a cabo tareas administrativas dando consentimiento explícito con la interfaz de usuario de consentimiento. Estas tareas administrativas incluyen instalar software y controladores, cambiar la configuración de todo el sistema, ver o cambiar otras cuentas de usuario y ejecutar herramientas administrativas.

En su estado con privilegios mínimos, los administradores se denominan administradores protegidos. En su estado elevado, se hace referencia a ellos como administradores con privilegios elevados. Por el contrario, los usuarios estándar no pueden elevarse por sí mismos, pero pueden pedir a un administrador que los eleve mediante la interfaz de usuario de credenciales. La cuenta predefinida Administrador no requiere elevación.

![captura de pantalla del mensaje de seguridad ' permitir programa ' ](images/winenv-uac-image1.png)

La interfaz de usuario de consentimiento, que se usa para elevar a los administradores protegidos para que tengan privilegios administrativos.

![captura de pantalla del mensaje que solicita la contraseña ](images/winenv-uac-image2.png)

La interfaz de usuario de credenciales, que se usa para elevar los usuarios estándar.

UAC proporciona las siguientes ventajas:

-   Reduce el número de programas que se ejecutan con privilegios elevados, lo que ayuda a impedir que los usuarios cambien accidentalmente la configuración del sistema y ayuda a evitar que "malware" Obtenga acceso a todo el sistema. Cuando se deniega la elevación, el malware solo puede afectar a los datos del usuario actual. Sin elevación, el malware no puede realizar cambios en todo el sistema ni afectar a otros usuarios.
-   En el caso de los [entornos administrados](glossary.md), las experiencias de UAC bien diseñadas permiten a los usuarios ser más productivos cuando se ejecutan como usuarios estándar mediante la eliminación de restricciones innecesarias.
-   Ofrece a los usuarios estándar la posibilidad de solicitar a los administradores que les concedan permisos para realizar tareas administrativas dentro de su sesión actual.
-   En el caso de entornos domésticos, permite un mejor control parental sobre los cambios en todo el sistema, incluido el software que se instala.

**Desarrolladores:** Para obtener información de implementación, consulte [rediseñar la interfaz de usuario para la compatibilidad con UAC](/previous-versions/bb756990(v=msdn.10)).

En Windows Vista, los administradores protegidos pueden elegir recibir notificaciones sobre todos los cambios del sistema o ninguno. La configuración predeterminada de UAC es notificar sobre todos los cambios, con independencia de cuál sea su origen. Cuando se le notifique, el escritorio estará atenuado y debe aprobar o denegar la solicitud en el cuadro de diálogo de UAC antes de poder hacer nada más en el equipo. La atenuación del escritorio se conoce como [escritorio seguro](glossary.md) porque otros programas no se pueden ejecutar mientras está atenuado.

Windows 7 introduce dos valores intermedios de UAC para los administradores protegidos, además de los dos desde Windows Vista. La primera es notificar a los usuarios solo cuando un programa realiza el cambio, por lo que los administradores se elevan automáticamente cuando realizan un cambio. Esta es la configuración predeterminada de UAC en Windows 7 y también hace uso del escritorio seguro.

La segunda configuración intermedia en Windows 7 es la misma que la primera, salvo que no usa el escritorio seguro.

![captura de pantalla de cuatro configuraciones de UAC en Windows 7 ](images/winenv-uac-image3.png)

Windows 7 introduce dos valores intermedios de UAC.

**Nota:** Las instrucciones relacionadas con la escritura de [código para admitir el control de cuentas de usuario](/previous-versions/aa905330(v=msdn.10)) se presentan en un artículo independiente.

## <a name="design-concepts"></a>Conceptos de diseño

**Objetivos**

Una experiencia de control de cuentas de usuario bien diseñada tiene los siguientes objetivos:

-   **Elimine la elevación innecesaria.** Los usuarios deben tener que elevar solo para realizar tareas que requieren privilegios administrativos. Todas las demás tareas deben diseñarse para eliminar la necesidad de elevación. A menudo, el software heredado requiere privilegios de administrador innecesariamente escribiendo en las secciones del registro HKLM o HKCR, o bien en los archivos de programa o en las carpetas del sistema de Windows.
-   **Ser de predicción.** Los usuarios estándar necesitan saber qué tareas requieren que un administrador realice o no se pueden realizar en todos los entornos administrados. Los administradores deben saber qué tareas requieren elevación. Si no pueden predecir la necesidad de elevación con precisión, es más probable que den su consentimiento para las tareas administrativas cuando no lo hagan.
-   **Requiere un esfuerzo mínimo.** Las tareas que requieren privilegios administrativos deben diseñarse para que requieran una sola elevación. Las tareas que requieren varias elevaciones se vuelven tediosas rápidamente.
-   **Vuelva a los privilegios mínimos.** Una vez que se completa una tarea que requiere privilegios administrativos, el programa debe volver al estado de privilegios mínimos.

**Flujo de tareas de elevación**

Cuando una tarea requiere elevación, tiene los siguientes pasos:

1.  **Punto de entrada.** Las tareas que requieren la elevación inmediata cuando UAC está totalmente habilitado tienen puntos de entrada marcados con el escudo de UAC. En este caso, los usuarios deberían esperar ver una interfaz de usuario de elevación inmediatamente después de hacer clic en estos comandos y deben tener especial cuidado cuando vean la interfaz de usuario de elevación de las tareas que no tienen un escudo.

    ![captura de pantalla de iconos de escudo de UAC y sus etiquetas ](images/winenv-uac-image4.png)

    En este ejemplo, el control parental y los elementos del panel de control de cuentas de usuario requieren elevación.

    Cuando UAC está parcialmente habilitado o desactivado por completo, se sigue mostrando el escudo de UAC para indicar que la tarea implica cambios de nivel de sistema y, por tanto, requiere elevación, incluso si es posible que el usuario no vea la UI de elevación. Mostrar siempre el escudo de UAC para las tareas que requieren elevación mantiene la interfaz de usuario sencilla y predecible.

2.  **Indicador.** Para los administradores protegidos, la tarea solicita el consentimiento mediante la interfaz de usuario de consentimiento. Para los usuarios estándar, la tarea solicita credenciales de administrador mediante la interfaz de usuario de credenciales.

    ![captura de pantalla de dos tipos de elevación ](images/winenv-uac-image5.png)

    En estos ejemplos se muestra la interfaz de usuario de credenciales y la interfaz de usuario de consentimiento.

3.  **Proceso elevado independiente.** Internamente, se crea un nuevo proceso con privilegios elevados para realizar la tarea.
4.  **Revertir a los privilegios mínimos.** Si es necesario, revierta a los privilegios mínimos para completar los pasos que no requieren elevación.

Tenga en cuenta que las tareas no "recuerdan" los Estados elevados. Por ejemplo, si el usuario navega hacia atrás y hacia delante por un punto de entrada de elevación en un asistente, el usuario debe elevar cada vez.

## <a name="usage-patterns"></a>Patrones de uso

El control de cuentas de usuario tiene varios patrones de uso (en orden de preferencia):

1.  **Trabajo para usuarios estándar.** Diseñe la característica para todos los usuarios limitando su ámbito al usuario actual. Al limitar la configuración al usuario actual (en lugar de todo el sistema), se elimina completamente la necesidad de una interfaz de usuario de elevación y se permite a los usuarios completar la tarea.

    **Incorrecto:**

    ![captura de pantalla del mensaje: no tiene privilegios ](images/winenv-uac-image6.png)

    En este ejemplo, los usuarios de Windows XP tenían que tener privilegios administrativos para ver o cambiar la zona horaria actual.

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo fecha y hora ](images/winenv-uac-image7.png)

    En este ejemplo, la característica de zona horaria se ha rediseñado en Windows 7 y Windows Vista para que funcione con todos los usuarios.

2.  **Tienen elementos de interfaz de usuario independientes para los administradores y usuarios estándar.** Separe claramente las tareas de usuario estándar de las tareas administrativas. Conceda a todos los usuarios acceso a información útil de solo lectura. Identifique claramente las tareas administrativas con el escudo de UAC.

    ![gráfico de escudo de UAC que muestra la elevación necesaria ](images/winenv-uac-image8.png)

    En este ejemplo, el elemento del panel de control del sistema muestra su estado a todos los usuarios, pero cambiar la configuración de todo el sistema requiere elevación.

3.  **Permitir a los usuarios estándar que intenten realizar tareas y elevar en caso de error.** Si los usuarios estándar pueden ver la información y realizar algunos cambios sin elevación, les permite tener acceso a la interfaz de usuario y hacer que se eleve solo si se produce un error en la tarea. Este enfoque es adecuado cuando los usuarios estándar tienen acceso limitado, como las propiedades de sus propios archivos en el explorador de Windows. También es adecuado para la configuración en las páginas del concentrador híbrido del panel de control.

    ![captura de pantalla del mensaje de acceso denegado ](images/winenv-uac-image9.png)

    En este ejemplo, el usuario intentó cambiar las propiedades del archivo de programa pero no tiene privilegios suficientes. El usuario puede elevar y volver a intentarlo.

4.  **Trabajar solo para administradores.** Use este enfoque solo para características y programas de administrador. Si una característica está destinada únicamente a los administradores (y no tiene ninguna ruta de navegación ni información útil de solo lectura para los usuarios estándar), puede solicitar credenciales de administrador en el punto de entrada antes de mostrar cualquier interfaz de usuario. Use este enfoque para los asistentes largos y los [flujos de página](glossary.md) cuando todas las rutas de acceso requieren privilegios administrativos.

    Si todo el programa es solo para administradores, márquelo para solicitar credenciales de administrador para poder iniciarlo. Windows muestra estos iconos de programa con la superposición de escudo de UAC.

    ![captura de pantalla del logotipo de Windows y la superposición de escudo de UAC ](images/winenv-uac-image10.png)

    En este ejemplo, el programa requiere privilegios administrativos para iniciarse.

## <a name="guidelines"></a>Directrices

### <a name="uac-shield-icon"></a>Icono de escudo de UAC

-   **Muestre los controles con el escudo de UAC para indicar que la tarea requiere una elevación inmediata cuando UAC está totalmente habilitado,** incluso aunque UAC no esté totalmente habilitado. Si todas las rutas de acceso de un asistente y un [flujo de página](glossary.md) requieren elevación, muestre la pantalla de UAC en el punto de entrada de la tarea. El uso correcto del escudo de UAC ayuda a los usuarios a predecir cuándo se requiere la elevación.
-   **Si el programa admite varias versiones de Windows, muestre la pantalla de UAC si al menos una versión requiere elevación.** Dado que Windows XP nunca requiere elevación, considere la posibilidad de quitar las pletinas de UAC para Windows XP si puede hacerlo de manera coherente y sin dañar el rendimiento.
-   **No muestre el escudo de UAC para las tareas que no requieren elevación en la mayoría de los contextos.** Dado que este enfoque a veces será engañoso, el método preferido es usar en su lugar un comando contextual blindado correctamente.

    ![captura de pantalla de archivos de fotos en el explorador de Windows ](images/winenv-uac-image11.png)

    Dado que el comando nueva carpeta solo requiere elevación cuando se usa en carpetas del sistema, se muestra sin un escudo de UAC.

-   La pletina de UAC se puede mostrar en los siguientes controles:

    **Botones de comando:**

    ![captura de pantalla del botón de comando con el icono de escudo de UAC ](images/winenv-uac-image12.png)

    Botón de comando que requiere elevación inmediata.

    **Vínculos de comandos:**

    ![captura de pantalla del vínculo de comando con el icono de escudo de UAC ](images/winenv-uac-image13.png)

    Vínculo de comando que requiere la elevación inmediata.

    **Vínculos**

    ![captura de pantalla del vínculo cambiar cuenta con escudo de UAC ](images/winenv-uac-image14.png)

    Vínculo que requiere la elevación inmediata.

    **Restringi**

    ![captura de pantalla del menú con escudo de UAC ](images/winenv-uac-image15.png)

    Menú desplegable que requiere elevación inmediata.

-   Dado que las tareas no recuerdan los Estados elevados, **no cambie el escudo de UAC para reflejar el estado.**
-   **Mostrar el escudo de UAC incluso si se ha desactivado el control de cuentas de usuario o si el usuario está usando la cuenta de administrador integrada.** Mostrar de forma coherente el escudo de UAC es más fácil de programar y proporciona a los usuarios información sobre la naturaleza de la tarea.

### <a name="elevation"></a>Elevation

-   **Siempre que sea posible, diseñe las tareas que deben realizar los usuarios estándar sin elevación.** Conceda a todos los usuarios acceso a información útil de solo lectura.
-   **Elevar en función de cada tarea, no por cada configuración.** No mezcle la configuración de usuario estándar con la configuración administrativa en una sola página o cuadro de diálogo. Por ejemplo, si los usuarios estándar pueden cambiar algunas opciones de configuración, pero no todas, divida dichas configuraciones como una superficie de interfaz de usuario independiente.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo Configuración de fecha y hora ](images/winenv-uac-image16.png)

    En este ejemplo, la configuración de usuario estándar se combina incorrectamente con la configuración administrativa.

    **Correcto:**

    ![captura de pantalla del mismo cuadro de diálogo sin escudos de UAC ](images/winenv-uac-image17.png)

    En este ejemplo, la configuración para cambiar la fecha y la hora está en un cuadro de diálogo independiente, solo está disponible para los administradores. La configuración de zona horaria está disponible para los usuarios estándar y no se combina con la configuración administrativa.

-   **No tenga en cuenta la necesidad de elevar a la hora de determinar si se debe mostrar o deshabilitar un control.** El motivo es el siguiente:
    -   En entornos no administrados, supongamos que los usuarios estándar pueden elevar el control solicitando a un administrador. La deshabilitación de los controles que requieren elevación impedirá que los usuarios tengan privilegios de elevación.
    -   En entornos administrados, supongamos que los usuarios estándar no pueden elevar en absoluto. La eliminación de controles que requieren elevación impedirá que los usuarios sepan cuándo dejar de buscar.
-   **Para eliminar la elevación innecesaria:**
    -   **Si una tarea puede requerir elevación, eleve lo más tarde posible.** Si una tarea necesita una [confirmación](mess-confirm.md), muestre la interfaz de usuario de elevación solo después de que el usuario haya confirmado. Si una tarea requiere siempre elevación, eleve en su punto de entrada.
    -   **Una vez elevado, Manténgase elevado hasta que ya no se necesiten privilegios elevados.** Los usuarios no deben tener que elevar varias veces para realizar una sola tarea.
    -   **Si los usuarios deben elevar para realizar un cambio pero decide no realizar ningún cambio, deje habilitados los botones de confirmación positivos, pero controle la confirmación como cancelación.** Al hacerlo, se evita que los usuarios tengan que elevar solo para cerrar una ventana.
    -   **Incorrecto:**
    -   ![captura de pantalla de la ventana con un solo botón activo ](images/winenv-uac-image18.png)
    -   En este ejemplo, el botón Guardar cambios está deshabilitado para evitar una elevación innecesaria, pero se habilita cuando los usuarios cambian la selección. Sin embargo, el botón de confirmación deshabilitado hace que parezca que los usuarios realmente no tienen una opción.
-   **No se muestra un mensaje de error cuando se produce un error en las tareas, ya que los usuarios deciden no elevarlas.** Suponga que los usuarios decidieron intencionadamente no continuar, por lo que no tendrán en cuenta esta situación como un error.

    **Incorrecto:**

    ![captura de pantalla del mensaje: fabrikam restore no se puede ejecutar ](images/winenv-uac-image19.png)

    En este ejemplo, Fabrikam restore proporciona incorrectamente un mensaje de error cuando el usuario decide no elevarlo.

-   **No muestre advertencias para explicar que los usuarios pueden necesitar elevar sus privilegios para realizar tareas.** Permita que los usuarios detecten este hecho por su cuenta.
-   **Muestre la interfaz de usuario de escudo y elevación de UAC basada en la tabla siguiente:**

    |                       |                                                                                                                                                                  |                                                                                                                                                                                                                       |                                                                                                      |
    |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | **Object**      | **Circunstancia**                                                                                                                                                | **Dónde colocar el escudo de UAC**                                                                                                                                                                               | **Cuándo elevar**                                                                            |
    | Programa<br/>    | Todo el programa es solo para administradores.<br/>                                                                                                            | ![captura de pantalla del logotipo de Windows y la superposición de escudo de UAC ](images/winenv-uac-image10.png)<br/> Icono superpuesto de escudo de UAC en el programa.<br/>                                                                       | Mostrar la interfaz de usuario de elevación en el inicio.<br/>                                                           |
    | Get-Help<br/>    | El comando completo es solo para administradores.<br/>                                                                                                            | ![captura de pantalla del vínculo cambiar cuenta y escudo de UAC ](images/winenv-uac-image14.png)<br/> Escudo de UAC en el botón de comando o vínculo.<br/>                                                                      | Muestra la interfaz de usuario de elevación cuando se hace clic en el botón de comando o en el vínculo, pero después de las confirmaciones.<br/> |
    | Get-Help<br/>    | El comando muestra información útil de solo lectura adecuada para todos los usuarios, pero los cambios requieren privilegios administrativos.<br/>                               | ![captura de pantalla del vínculo cambiar configuración y escudo de UAC ](images/winenv-uac-image8.png)<br/> Escudo de UAC en el botón de comando o vínculo para realizar cambios.<br/>                                                      | Muestra la interfaz de usuario de elevación cuando se hace clic en el botón de comando, pero después de las confirmaciones.<br/>         |
    | Get-Help<br/>    | Los usuarios estándar pueden ver la información y, posiblemente, realizar algunos cambios sin elevación. permita que los usuarios estándar intenten y eleve en caso de error.<br/> | ![captura de pantalla de error con el icono de UAC en el botón reintentar ](images/winenv-uac-image9.png)<br/> No muestre el escudo de UAC para el comando, pero lo mostrará para el punto de entrada de elevación si se produce un error en el comando.<br/> | Muestra la interfaz de usuario de elevación cuando el usuario vuelve a intentar el comando.<br/>                                       |
    | Paso de tarea<br/>  | Todos los pasos siguientes requieren elevación.<br/>                                                                                                               | ![captura de pantalla del botón de comando siguiente con el escudo de UAC ](images/winenv-uac-image20.png)<br/> Escudo de UAC en el botón siguiente (o equivalente).<br/>                                                                | Mostrar la interfaz de usuario de elevación cuando se haga clic en siguiente o en otro botón de confirmación.<br/>                         |
    | Paso de tarea<br/>  | Algunas ramas requieren elevación.<br/>                                                                                                                      | ![captura de pantalla del vínculo de comando con el escudo de UAC ](images/winenv-uac-image21.png)<br/> Escudo de UAC en vínculos de comandos que requieren elevación.<br/>                                                              | Mostrar la interfaz de usuario de elevación cuando se haga clic en los vínculos de comando con UAC Shield.<br/>                      |

    

     

### <a name="elevation-ui"></a>Interfaz de usuario de elevación

-   **Si el usuario proporciona una cuenta que no es válida (nombre o contraseña) o que no tiene privilegios de administrador, simplemente vuelva a mostrar la interfaz de usuario de credenciales.** No mostrar un mensaje de error.
-   **Si el usuario cancela la interfaz de usuario de credenciales, devuelva el usuario a la interfaz de usuario original.** No mostrar un mensaje de error.
-   Si se ha desactivado el control de cuentas de usuario y un usuario estándar intenta realizar una tarea que requiere elevación, proporcione un mensaje de error que indique "esta tarea requiere privilegios de administrador. Para realizar esta tarea, debe iniciar sesión con una cuenta de administrador ".

![captura de pantalla de la tarea requiere el mensaje privileges ](images/winenv-uac-image22.png)

En este ejemplo, se ha desactivado el control de cuentas de usuario, por lo que un mensaje de error explica que el usuario debe usar una cuenta de administrador.

### <a name="wizards"></a>Asistentes

-   **No eleve varias veces.** Una vez que se eleva un asistente, debe permanecer elevado.
-   Si la tarea se realiza en el asistente, coloque un escudo de UAC en el botón "siguiente" de la página de confirmación (al que se le debe dar una [etiqueta más específica](win-wizards.md)). Cuando el usuario confirma:
    -   Si la página siguiente es una página de progreso, avance hasta esa página y muestre de forma modal la interfaz de usuario de elevación. Después de la elevación correcta, realice la tarea.
    -   Si la página siguiente es una página de finalización, avance hasta esa página (pero reemplace temporalmente su contenido por "en espera de permiso...") y muestre de forma modal la interfaz de usuario de elevación. Después de la elevación correcta, realice la tarea y, a continuación, muestre el contenido de la página de finalización.
    -   Si el usuario cancela la interfaz de usuario de elevación, vuelva a la página de confirmación. Esto permite al usuario volver a intentarlo.
-   Si la tarea se realiza una vez finalizado el asistente, coloque un escudo de UAC en el botón "finalizar" de la página de confirmación (que debe recibir una [etiqueta más específica](win-wizards.md)). Cuando el usuario confirma:
    -   Permanezca en la página de confirmación y muestre la interfaz de usuario de elevación de forma modal. Después de la elevación correcta, cierre el asistente.
    -   Si el usuario cancela la interfaz de usuario de elevación, vuelva a la página de confirmación. Esto permite al usuario volver a intentarlo.
-   En el caso de los asistentes extensos destinados solo a los administradores, puede solicitar credenciales de administrador en el punto de entrada antes de mostrar la interfaz de usuario.

## <a name="text"></a>Texto

-   **No use puntos suspensivos solo porque un comando requiere elevación.** La necesidad de elevar se indica con el escudo de UAC.

## <a name="documentation"></a>Documentación

Al hacer referencia al control de cuentas de usuario:

-   Consulte la característica control de cuentas de usuario (en la primera mención) o UAC (en las menciones posteriores), no cuenta de usuario con privilegios mínimos o LUA.
-   Consulte a los usuarios que no son administradores como usuarios estándar.
-   Consulte a los administradores de equipos integrados como administradores integrados.

En la documentación del usuario:

-   Consulte el acto de dar su consentimiento para realizar una tarea administrativa como conceder permiso.

En programación y otra documentación técnica:

-   Consulte el acto de dar su consentimiento para realizar una tarea administrativa como elevación.
-   En el contexto de UAC, consulte administradores como administradores protegidos cuando no se eleva y administradores elevados después de la elevación.
-   Consulte el cuadro de diálogo que se usa para escribir contraseñas como la interfaz de usuario de credenciales. Consulte el cuadro de diálogo que se usa para dar su consentimiento como la interfaz de usuario de consentimiento. Haga referencia a ambos normalmente como la interfaz de usuario de elevación.

