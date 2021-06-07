---
title: Control de cuentas de usuario (conceptos básicos de diseño)
description: Una experiencia de control de cuentas de usuario bien diseñada ayuda a evitar cambios no deseados en todo el sistema de una manera predecible y requiere un esfuerzo mínimo.
ms.assetid: c4b83537-c600-4b24-bda6-df7a82719ab1
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: bb1424254a91f935073e57bbde2c7124fd838b32
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443216"
---
# <a name="user-account-control"></a>Control de cuentas de usuario

> [!NOTE]
> Esta guía de diseño se creó para Windows 7 y no se ha actualizado para las versiones más recientes de Windows. Gran parte de las instrucciones se siguen aplicando en principio, pero la presentación y los ejemplos no reflejan nuestra [guía de diseño actual.](/windows/uwp/design/)

Una experiencia de control de cuentas de usuario bien diseñada ayuda a evitar cambios no deseados en todo el sistema de una manera predecible y requiere un esfuerzo mínimo.

Con control de cuentas de usuario (UAC) totalmente habilitado, los administradores interactivos normalmente se ejecutan con privilegios de usuario mínimos, pero pueden elevarse automáticamente para realizar tareas administrativas mediante el consentimiento explícito con la interfaz de usuario de consentimiento. Estas tareas administrativas incluyen instalar software y controladores, cambiar la configuración de todo el sistema, ver o cambiar otras cuentas de usuario y ejecutar herramientas administrativas.

En su estado con menos privilegios, los administradores se conocen como administradores protegidos. En su estado elevado, se hace referencia a ellos como administradores con privilegios elevados. Por el contrario, los usuarios estándar no pueden elevarse por sí mismos, pero pueden pedir a un administrador que los eleve mediante la interfaz de usuario de credenciales. La cuenta de administrador integrada no requiere elevación.

![captura de pantalla del mensaje de seguridad "permitir programa" ](images/winenv-uac-image1.png)

Interfaz de usuario de consentimiento, que se usa para elevar los privilegios administrativos a los administradores protegidos.

![captura de pantalla del mensaje que solicita la contraseña ](images/winenv-uac-image2.png)

La interfaz de usuario de credenciales, que se usa para elevar los usuarios estándar.

UAC proporciona las siguientes ventajas:

-   Reduce el número de programas que se ejecutan con privilegios elevados, lo que ayuda a evitar que los usuarios cambien accidentalmente la configuración del sistema y a evitar que el "malware" obtenga acceso a todo el sistema. Cuando se deniega la elevación, el malware solo puede afectar a los datos del usuario actual. Sin elevación, el malware no puede realizar cambios en todo el sistema ni afectar a otros usuarios.
-   En [el caso de los entornos administrados,](glossary.md)las experiencias de UAC bien diseñadas permiten a los usuarios ser más productivos cuando se ejecutan como usuarios estándar mediante la eliminación de restricciones innecesarias.
-   Ofrece a los usuarios estándar la capacidad de pedir a los administradores que les den permiso para realizar tareas administrativas dentro de su sesión actual.
-   En el caso de los entornos particulares, permite un mejor control parental sobre los cambios en todo el sistema, incluido el software instalado.

**Desarrolladores:** Para obtener información sobre la implementación, vea [Rediseñar la interfaz de usuario para la compatibilidad con UAC.](/previous-versions/bb756990(v=msdn.10))

En Windows Vista, los administradores protegidos pueden optar por recibir notificaciones sobre todos los cambios del sistema o ninguno. La configuración predeterminada de UAC es notificar todos los cambios, independientemente de su origen. Cuando se le notifique, el escritorio se atenuará y debe aprobar o denegar la solicitud en el cuadro de diálogo UAC para poder hacer cualquier otra cosa en el equipo. La atenuación del escritorio se conoce [](glossary.md) como escritorio seguro porque otros programas no se pueden ejecutar mientras está atenuado.

Windows 7 presenta dos configuraciones de UAC intermedias para administradores protegidos, además de las dos de Windows Vista. La primera es notificar a los usuarios solo cuando un programa realiza el cambio, por lo que los administradores se elevan automáticamente cuando ellos mismos hacen un cambio. Esta es la configuración predeterminada de UAC en Windows 7 y también usa el escritorio seguro.

La segunda configuración intermedia en Windows 7 es la misma que la primera, salvo que no usa el escritorio seguro.

![captura de pantalla de cuatro configuraciones de uac en Windows 7 ](images/winenv-uac-image3.png)

Windows 7 presenta dos configuraciones de UAC intermedias.

**Nota:** Las instrucciones relacionadas con la escritura [de código para admitir](/previous-versions/aa905330(v=msdn.10)) el control de cuentas de usuario se presentan en un artículo independiente.

## <a name="design-concepts"></a>Conceptos de diseño

**Objetivos**

Una experiencia de control de cuentas de usuario bien diseñada tiene los siguientes objetivos:

-   **Elimine la elevación innecesaria.** Los usuarios deben tener que elevar solo para realizar tareas que requieren privilegios administrativos. Todas las demás tareas deben diseñarse para eliminar la necesidad de elevación. A menudo, el software heredado requiere privilegios de administrador innecesariamente escribiendo en las secciones del Registro HKLM o HKCR, o en las carpetas Archivos de programa o Sistema de Windows.
-   **Sea predecible.** Los usuarios estándar deben saber qué tareas requieren que un administrador realice o no se pueden realizar en entornos administrados. Los administradores deben saber qué tareas requieren elevación. Si no pueden predecir la necesidad de elevación con precisión, es más probable que den su consentimiento para las tareas administrativas cuando no deberían.
-   **Requiere un esfuerzo mínimo.** Las tareas que requieren privilegios administrativos deben diseñarse para requerir una sola elevación. Las tareas que requieren varias elevaciones rápidamente se vuelven tediosas.
-   **Revertir a privilegios mínimos.** Una vez completada una tarea que requiere privilegios administrativos, el programa debe revertir al estado de privilegios mínimos.

**Flujo de tareas de elevación**

Cuando una tarea requiere elevación, tiene los pasos siguientes:

1.  **Punto de entrada.** Las tareas que requieren elevación inmediata cuando UAC está totalmente habilitado tienen puntos de entrada marcados con el escudo de UAC. En este caso, los usuarios deben esperar ver una interfaz de usuario de elevación inmediatamente después de hacer clic en estos comandos y deben tener cuidado adicional cuando ven la interfaz de usuario de elevación de tareas que no tienen un escudo.

    ![captura de pantalla de iconos de escudo uac y sus etiquetas ](images/winenv-uac-image4.png)

    En este ejemplo, los elementos del panel de control de cuentas de usuario y control de control parental requieren elevación.

    Cuando UAC está parcialmente habilitado o desactivado por completo, el escudo de UAC todavía se muestra para indicar que la tarea implica cambios en el nivel del sistema y, por tanto, requiere elevación, incluso si es posible que el usuario no vea la interfaz de usuario de elevación. Mostrar siempre el escudo de UAC para las tareas que requieren elevación hace que la interfaz de usuario sea sencilla y predecible.

2.  **Elevación.** En el caso de los administradores protegidos, la tarea solicita consentimiento mediante la interfaz de usuario de consentimiento. Para los usuarios estándar, la tarea solicita las credenciales de administrador mediante la interfaz de usuario de credenciales.

    ![captura de pantalla de dos tipos de elevación ](images/winenv-uac-image5.png)

    En estos ejemplos se muestran la interfaz de usuario de credenciales y la interfaz de usuario de consentimiento.

3.  **Separe el proceso con privilegios elevados.** Internamente, se crea un nuevo proceso con privilegios elevados para realizar la tarea.
4.  **Revierta al privilegio mínimo.** Si es necesario, revierta al privilegio mínimo para completar los pasos que no requieran elevación.

Tenga en cuenta que las tareas no "recuerda" los estados elevados. Por ejemplo, si el usuario navega hacia delante y hacia atrás sobre un punto de entrada de elevación en un asistente, el usuario debe elevar cada vez.

## <a name="usage-patterns"></a>Patrones de uso

El control de cuentas de usuario tiene varios patrones de uso (en orden de preferencia):

1.  **Trabajo para usuarios estándar.** Diseñe la característica para todos los usuarios limitando su ámbito al usuario actual. Al limitar la configuración al usuario actual (en lugar de a todo el sistema), se elimina la necesidad de una interfaz de usuario de elevación completamente y se permite a los usuarios completar la tarea.

    **Incorrecto:**

    ![captura de pantalla del mensaje: no tiene privilegios ](images/winenv-uac-image6.png)

    En este ejemplo, los usuarios de Windows XP tenían que tener privilegios administrativos para ver o cambiar la zona horaria actual.

    **Correcto:**

    ![captura de pantalla del cuadro de diálogo fecha y hora ](images/winenv-uac-image7.png)

    En este ejemplo, la característica de zona horaria se ha rediseñado en Windows 7 y Windows Vista para que funcione para todos los usuarios.

2.  **Tener elementos de interfaz de usuario independientes para usuarios y administradores estándar.** Separe claramente las tareas de usuario estándar de las tareas administrativas. Proporcionar a todos los usuarios acceso a información útil de solo lectura. Identifique claramente las tareas administrativas con el escudo de UAC.

    ![gráfico del escudo de uac que muestra la elevación necesaria ](images/winenv-uac-image8.png)

    En este ejemplo, el elemento panel de control Sistema muestra su estado a todos los usuarios, pero cambiar la configuración de todo el sistema requiere elevación.

3.  **Permitir que los usuarios estándar intenten realizar tareas y elevar los privilegios en caso de error.** Si los usuarios estándar pueden ver la información y pueden realizar algunos cambios sin elevación, permita que accedan a la interfaz de usuario y que los eleven solo si se produce un error en la tarea. Este enfoque es adecuado cuando los usuarios estándar tienen acceso limitado, como con propiedades de sus propios archivos en Explorador de Windows. También es adecuado para la configuración en Panel de control de centro híbrido.

    ![captura de pantalla del mensaje de acceso denegado ](images/winenv-uac-image9.png)

    En este ejemplo, el usuario intentó cambiar las propiedades del archivo de programa, pero no tenía privilegios suficientes. El usuario puede elevar e intentarlo de nuevo.

4.  **Solo para administradores.** Use este enfoque solo para características y programas de administrador. Si una característica está pensada solo para administradores (y no tiene rutas de navegación ni información útil de solo lectura para los usuarios estándar), puede solicitar credenciales de administrador en el punto de entrada antes de mostrar cualquier interfaz de usuario. Use este enfoque para largos asistentes y flujos [de página](glossary.md) cuando todas las rutas de acceso requieran privilegios administrativos.

    Si todo el programa es solo para administradores, móntelo para solicitar credenciales de administrador con el fin de iniciarse. Windows muestra estos iconos de programa con la superposición de escudo de UAC.

    ![captura de pantalla del logotipo de Windows y la superposición del escudo de uac ](images/winenv-uac-image10.png)

    En este ejemplo, el programa requiere privilegios administrativos para iniciarse.

## <a name="guidelines"></a>Directrices

### <a name="uac-shield-icon"></a>Icono de escudo de UAC

-   **Mostrar controles con el escudo de UAC** para indicar que la tarea requiere elevación inmediata cuando UAC está totalmente habilitado, incluso si UAC no está habilitado actualmente. Si todas las rutas de acceso de un asistente y un flujo [de](glossary.md) página requieren elevación, muestre el escudo de UAC en el punto de entrada de la tarea. El uso adecuado del escudo de UAC ayuda a los usuarios a predecir cuándo se requiere elevación.
-   **Si el programa admite varias versiones de Windows, muestre el escudo de UAC si al menos una versión requiere elevación.** Dado que Windows XP nunca requiere elevación, considere la posibilidad de quitar los escudos UAC para Windows XP si puede hacerlo de forma coherente y sin dañar el rendimiento.
-   **No muestre el escudo de UAC para las tareas que no requieren elevación en la mayoría de los contextos.** Dado que este enfoque a veces será confuso, el enfoque preferido es usar un comando contextual blindado correctamente en su lugar.

    ![captura de pantalla de archivos de fotos en el Explorador de Windows ](images/winenv-uac-image11.png)

    Dado que el comando Nueva carpeta solo requiere elevación cuando se usa en carpetas del sistema, se muestra sin un escudo UAC.

-   El escudo de UAC se puede mostrar en los controles siguientes:

    **Botones de comando:**

    ![captura de pantalla del botón de comando con el icono de escudo de uac ](images/winenv-uac-image12.png)

    Botón de comando que requiere elevación inmediata.

    **Vínculos de comandos:**

    ![captura de pantalla del vínculo de comando con el icono de escudo de uac ](images/winenv-uac-image13.png)

    Vínculo de comando que requiere elevación inmediata.

    **Enlaces:**

    ![captura de pantalla del vínculo cambiar la cuenta con el escudo de uac ](images/winenv-uac-image14.png)

    Vínculo que requiere elevación inmediata.

    **Menús:**

    ![captura de pantalla del menú con uac shield ](images/winenv-uac-image15.png)

    Menú desplegable que requiere elevación inmediata.

-   Dado que las tareas no recuerda los estados elevados, **no cambie el escudo de UAC para reflejar el estado.**
-   **Muestre el escudo de UAC incluso si el control de cuentas de usuario se ha desactivado o si el usuario usa la cuenta de administrador integrada.** Mostrar de forma coherente el escudo de UAC es más fácil de programar y proporciona a los usuarios información sobre la naturaleza de la tarea.

### <a name="elevation"></a>Elevation

-   **Siempre que sea posible, diseñe las tareas que realizarán los usuarios estándar sin elevación.** Proporcionar a todos los usuarios acceso a información útil de solo lectura.
-   **Elevar por tarea, no por configuración.** No mezcle la configuración de usuario estándar con la configuración administrativa en una sola página o cuadro de diálogo. Por ejemplo, si los usuarios estándar pueden cambiar algunas opciones, pero no todas, divida esa configuración como una superficie de interfaz de usuario independiente.

    **Incorrecto:**

    ![captura de pantalla del cuadro de diálogo de configuración de fecha y hora ](images/winenv-uac-image16.png)

    En este ejemplo, la configuración de usuario estándar se mezcla incorrectamente con la configuración administrativa.

    **Correcto:**

    ![captura de pantalla del mismo cuadro de diálogo sin escudos uac ](images/winenv-uac-image17.png)

    En este ejemplo, la configuración para cambiar la fecha y hora se encuentra en un cuadro de diálogo independiente, disponible solo para los administradores. La configuración de zona horaria está disponible para los usuarios estándar y no se mezcla con la configuración administrativa.

-   **No considere la necesidad de elevar al determinar si se debe mostrar o deshabilitar un control.** El motivo es el siguiente:
    -   En entornos no administrados, suponga que los usuarios estándar pueden elevarlo solicitando a un administrador. Deshabilitar los controles que requieren elevación impediría que los usuarios elevara el nivel de los administradores.
    -   En entornos administrados, suponga que los usuarios estándar no pueden elevar en absoluto. La eliminación de controles que requieren elevación impediría que los usuarios sepan cuándo dejar de buscar.
-   **Para eliminar la elevación innecesaria:**
    -   **Si una tarea puede requerir elevación, eleve lo más tarde posible.** Si una tarea necesita una [confirmación,](mess-confirm.md)muestre la interfaz de usuario de elevación solo después de que el usuario lo haya confirmado. Si una tarea siempre requiere elevación, eleve en su punto de entrada.
    -   **Una vez elevado, mantenga los privilegios elevados hasta que ya no sean necesarios.** Los usuarios no deben tener que elevar el nivel varias veces para realizar una sola tarea.
    -   **Si los usuarios deben elevar los privilegios para realizar un cambio pero deciden no realizar cambios, deje habilitados los botones de confirmación positiva, pero controle la confirmación como una cancelación.** Al hacerlo, se elimina la necesidad de elevar los usuarios solo para cerrar una ventana.
    -   **Incorrecto:**
    -   ![captura de pantalla de la ventana con un solo botón activo ](images/winenv-uac-image18.png)
    -   En este ejemplo, el botón Guardar cambios está deshabilitado para evitar una elevación innecesaria, pero se habilita cuando los usuarios cambian la selección. Sin embargo, el botón de confirmación deshabilitado hace que parezca que los usuarios realmente no tienen una opción.
-   **No muestre un mensaje de error cuando se produce un error en las tareas porque los usuarios optaron por no elevar.** Supongamos que los usuarios optaron intencionadamente por no continuar, por lo que no considerarán esta situación como un error.

    **Incorrecto:**

    ![captura de pantalla del mensaje: no se puede ejecutar la restauración de fabrikam ](images/winenv-uac-image19.png)

    En este ejemplo, Restauración de Fabrikam genera incorrectamente un mensaje de error cuando el usuario decide no elevar.

-   **No muestre advertencias para explicar que los usuarios pueden necesitar elevar sus privilegios para realizar tareas.** Permitir que los usuarios descubran este hecho por sí mismos.
-   **Muestre el escudo UAC y la interfaz de usuario de elevación en función de la tabla siguiente:**

    | Object | Circunstancia | Dónde colocar el escudo de UAC | Cuándo elevar |
    |-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
    | Programa<br/>    | Todo el programa es solo para administradores.<br/>                                                                                                            | ![captura de pantalla del logotipo de Windows y la superposición del escudo de uac ](images/winenv-uac-image10.png)<br/> Superposición de escudo de UAC en el icono del programa.<br/>                                                                       | Mostrar la interfaz de usuario de elevación en el inicio.<br/>                                                           |
    | Comando<br/>    | El comando completo es solo para administradores.<br/>                                                                                                            | ![captura de pantalla del vínculo cambiar la cuenta y el escudo de uac ](images/winenv-uac-image14.png)<br/> Escudo de UAC en el botón de comando o vínculo.<br/>                                                                      | Mostrar la interfaz de usuario de elevación cuando se hace clic en el botón o vínculo del comando, pero después de cualquier confirmación.<br/> |
    | Comando<br/>    | El comando muestra información útil de solo lectura adecuada para todos los usuarios, pero los cambios requieren privilegios administrativos.<br/>                               | ![captura de pantalla del vínculo cambiar la configuración y el escudo de uac ](images/winenv-uac-image8.png)<br/> Escudo de UAC en el botón de comando o vínculo para realizar cambios.<br/>                                                      | Muestra la interfaz de usuario de elevación cuando se hace clic en el botón de comando, pero después de cualquier confirmación.<br/>         |
    | Comando<br/>    | Los usuarios estándar pueden ver la información y posiblemente realizar algunos cambios sin elevación. permitir que los usuarios estándar intenten y elevar en caso de error.<br/> | ![captura de pantalla de error con el icono de uac en el botón reintentar ](images/winenv-uac-image9.png)<br/> No muestre el escudo de UAC para el comando, sino que lo muestre para el punto de entrada de elevación si se produce un error en el comando.<br/> | Muestra la interfaz de usuario de elevación cuando el usuario vuelve a inste el comando.<br/>                                       |
    | Paso de tarea<br/>  | Todos los pasos posteriores requieren elevación.<br/>                                                                                                               | ![captura de pantalla del siguiente botón de comando con el escudo de uac ](images/winenv-uac-image20.png)<br/> Escudo de UAC en el botón Siguiente (o equivalente).<br/>                                                                | Muestra la interfaz de usuario de elevación cuando se hace clic en el botón Siguiente u otro botón de confirmación.<br/>                         |
    | Paso de tarea<br/>  | Algunas ramas requieren elevación.<br/>                                                                                                                      | ![captura de pantalla del vínculo de comando con uac shield ](images/winenv-uac-image21.png)<br/> Escudo de UAC en vínculos de comandos que requieren elevación.<br/>                                                              | Muestra la interfaz de usuario de elevación cuando se hace clic en los vínculos de comandos con el escudo de UAC.<br/>                      |

    

     

### <a name="elevation-ui"></a>Interfaz de usuario de elevación

-   **Si el usuario proporciona una cuenta que no es válida (nombre o contraseña) o no tiene privilegios de administrador, simplemente vuelva a mostrar la interfaz de usuario de credenciales.** No muestre un mensaje de error.
-   **Si el usuario cancela la interfaz de usuario de credenciales, vuelva a devolver el usuario a la interfaz de usuario original.** No muestre un mensaje de error.
-   Si control de cuentas de usuario se ha desactivado y un usuario estándar intenta realizar una tarea que requiere elevación, proporcione un mensaje de error que indica "Esta tarea requiere privilegios de administrador. Para realizar esta tarea, debe iniciar sesión con una cuenta de administrador".

![captura de pantalla de la tarea requiere un mensaje de privilegios ](images/winenv-uac-image22.png)

En este ejemplo, el control de cuentas de usuario se ha desactivado, por lo que un mensaje de error explica que el usuario debe usar una cuenta de administrador.

### <a name="wizards"></a>Asistentes

-   **No eleve el nivel varias veces.** Una vez que un asistente tiene privilegios elevados, debe permanecer con privilegios elevados.
-   Si la tarea se realiza dentro del asistente, coloque un escudo UAC en el botón "Siguiente" de la página Confirmar (a la que se le debe proporcionar una [etiqueta más específica).](win-wizards.md) Cuando el usuario confirma:
    -   Si la página siguiente es una página Progreso, avance a esa página y muestre modalmente la interfaz de usuario de elevación. Después de la elevación correcta, realice la tarea.
    -   Si la página siguiente es una página Finalización, avance a esa página (pero reemplace temporalmente su contenido por "Esperando permiso...") y muestre modalmente la interfaz de usuario de elevación. Después de la elevación correcta, realice la tarea y, a continuación, muestre el contenido de la página Finalización.
    -   Si el usuario cancela la interfaz de usuario de elevación, vuelva a la página Confirmar. Si lo hace, el usuario puede intentarlo de nuevo.
-   Si la tarea se realiza una vez completado el asistente, coloque un escudo de UAC en el botón "Finalizar" de la página de confirmación (al que se le debe proporcionar una etiqueta [más específica).](win-wizards.md) Cuando el usuario confirma:
    -   Permanezca en la página Confirmar y muestre de forma modal la interfaz de usuario de elevación. Después de la elevación correcta, cierre el asistente.
    -   Si el usuario cancela la interfaz de usuario de elevación, vuelva a la página Confirmar. Si lo hace, el usuario puede intentarlo de nuevo.
-   Para los asistentes largos destinados solo a administradores, puede solicitar credenciales de administrador en el punto de entrada antes de mostrar cualquier interfaz de usuario.

## <a name="text"></a>Texto

-   **No use puntos suspensivos solo porque un comando requiere elevación.** La necesidad de elevar se indica con el escudo de UAC.

## <a name="documentation"></a>Documentación

Al hacer referencia a Control de cuentas de usuario:

-   Consulte la característica como Control de cuentas de usuario (en la primera mención) o UAC (en la siguiente mención), no cuenta de usuario con privilegios mínimos o LUA.
-   Consulte usuarios que no son administradores como Usuarios estándar.
-   Consulte administradores de equipos integrados como administradores integrados.

En la documentación del usuario:

-   Consulte el acto de dar su consentimiento para realizar una tarea administrativa como dar permiso.

En programación y otra documentación técnica:

-   Consulte el acto de dar su consentimiento para realizar una tarea administrativa como elevación.
-   En el contexto de UAC, haga referencia a los administradores como Administradores protegidos cuando no tienen privilegios elevados y Administradores con privilegios elevados después de la elevación.
-   Consulte el cuadro de diálogo que se usa para escribir contraseñas como la interfaz de usuario de credenciales. Consulte el cuadro de diálogo que se usa para dar su consentimiento como interfaz de usuario de consentimiento. Haga referencia a ambos generalmente como Interfaz de usuario de elevación.

