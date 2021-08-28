---
title: El gráfico accChecker Interfaz de usuario
description: En este tema se describen los elementos que son la GUI de AccChecker.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf645a3afd35bdd906d1ab26453d16672311cb4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473391"
---
# <a name="the-accchecker-graphical-user-interface"></a>El gráfico accChecker Interfaz de usuario

En este tema se describen los elementos que son la GUI de AccChecker.

-   [Pestaña Comprobaciones](#verifications-tab)
-   [Pestaña Resultados](#results-tab)
-   [Pestañas Lector de pantalla de MSAA y UIA](#msaa-and-uia-screen-reader-tabs)
-   [Pestañas árbol MSAA y UIA](#msaa-and-uia-tree-tabs)
-   [Menú Archivo](#file-menu)
-   [Temas relacionados](#related-topics)

## <a name="verifications-tab"></a>Pestaña Comprobaciones

AccChecker comienza con la vista predeterminada de la **pestaña Comprobaciones:**

![Captura de pantalla que muestra la pestaña "Comprobaciones" en el Comprobador de accesibilidad de UI.](images/accchecker-verifications-tab.png)

La **pestaña Comprobaciones** contiene los componentes siguientes.

-   **Selector de destino de comprobación** Ofrece las siguientes opciones para seleccionar una aplicación o un control de destino.
    -   Elija un destino en la lista desplegable rellenada previamente. Esta lista contiene todos los HWND de nivel superior identificados en el inicio.
    -   Elija un HWND en función de la ubicación del cursor del mouse (los controles seleccionables se resaltan con un rectángulo rojo). Esta opción le permite seleccionar cualquier objeto visible que tenga un HWND.
    -   Escriba un HWND determinado.
-   **Lista de comprobación de rutinas de comprobación** Proporciona la capacidad de seleccionar la rutina de comprobación deseada que se va a realizar en una aplicación o control. Consulte Rutinas de comprobación para obtener más información.
-   **Selector de archivos de supresión de errores y advertencias** Los archivos de supresión se generan desde la pestaña **Resultados de** la comprobación. Al hacer clic con el botón derecho en un mensaje de error o advertencia y seleccionar **Suprimir** en el menú contextual, se establece una marca para ese mensaje. Si la **casilla Supresiones** está activada, las entradas suprimidas aparecen en la lista. Una entrada suprimida se puede eliminar mediante el mismo menú contextual que se usa para suprimirla.

    Un archivo de supresión se guarda en formato XML seleccionando **Guardar supresión** en el **menú** Archivo. Este archivo se consume en ejecuciones de comprobación posteriores donde se ocultarán los mensajes. Para quitar el archivo de supresión, haga clic **en Borrar**. Para obtener información sobre mensajes específicos, vea Mensajes de registro de comprobación. Use **Guardar registro** en el **menú** Archivo para guardar toda la lista como un archivo de registro en XML o como un archivo de texto con formato.

    ![pestaña de resultados de accchecker con el elemento de contexto suprimir resaltado](images/accchecker-results-tab-with-suppress.png)

    En el ejemplo siguiente se muestra el  contenido de un archivo de supresión generado mediante la ejecución de las comprobaciones de propiedades en la Windows panel de control firewall. El error con un identificador de "ElementHasNoName" se eligió para la supresión en este ejemplo.

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   **Mostrar resultados con prioridad** Ofrece las siguientes opciones para filtrar los resultados de la comprobación por prioridad.
    -   **Todos** Incluya todos los resultados independientemente de la prioridad.
    -   **Solo P1** Incluya solo los resultados de prioridad 0 y prioridad 1.
    -   **Solo P1 P2** Incluya los resultados de prioridad 0 a 2.
-   **Ejecución de las comprobaciones seleccionadas** Proporciona el **botón Ejecutar comprobaciones** para iniciar el proceso de comprobación. Mientras se ejecutan las comprobaciones, el botón cambia a **Cancelar** comprobaciones y se puede usar para detener las comprobaciones una vez completada la actual.

## <a name="results-tab"></a>Pestaña Resultados

La **pestaña Resultados** se rellena una vez completadas las tareas de comprobación seleccionadas. Consta de los siguientes componentes.

-   Lista de mensajes, que muestra los mensajes de error, advertencia e información generados por las tareas de comprobación seleccionadas. Los mensajes mostrados se pueden filtrar por tipo mediante las casillas situadas encima de la lista de mensajes.
-   Los detalles del mensaje y una captura de pantalla del destino de comprobación. Al seleccionar un mensaje de la lista de mensajes, se muestran más detalles y se resalta el elemento correspondiente en el panel de captura de pantalla. El **botón** Visualizar cambia AccChecker a la **pestaña Árbol de MSAA.** Si se resalta un error en la **pestaña Resultados,** el elemento correspondiente se resalta en la **pestaña Árbol de MSAA.**

Al hacer clic con el botón derecho en un mensaje se expone un menú contextual con los siguientes elementos.

-   **Suprimir** Agrega el mensaje a la lista de supresión.
-   **Copiar en el Portapapeles** Copia los detalles del mensaje en el Portapapeles.
-   **Visualizar** Cambia AccChecker a la **pestaña Árbol de MSAA.** El elemento que corresponde al error seleccionado está resaltado.
-   **Ayuda** Muestra información adicional sobre el mensaje.

## <a name="msaa-and-uia-screen-reader-tabs"></a>Pestañas Lector de pantalla de MSAA y UIA

Las pestañas Lector de pantalla de MSAA y Lector de pantalla de UIA son similares. Ambos muestran una transcripción de los elementos encontrados en un recorrido simulado del destino de comprobación por un lector de pantalla, salvo que uno muestra la implementación de MSAA y el otro muestra la implementación de UIA.

Los elementos se navegan y registran tal y como los leería un lector de pantalla. La información presentada en esta pestaña es esencial para confirmar que solo se anuncia información útil y pertinente. Por ejemplo, un nombre de control de sonido normal como "MenuItem Edit" o "PushButton Close" es aceptable; Sin embargo, un nombre de control que no tenga sentido, como "CPNavPanel22" o "DefaultValue1", no es aceptable. El **botón** Visualizar hace que AccChecker cambie a la **pestaña Árbol de MSAA** **o Árbol de UIA.** Si un elemento está  resaltado en la pestaña Lector de pantalla, el elemento correspondiente se resalta en la pestaña Árbol **de MSAA** **o Árbol de UIA.**

La **rutina de comprobación ScreenReader** de **Consistence** debe estar seleccionada en la pestaña **Comprobaciones** para que se muestre la pestaña Lector de pantalla **MSAA.** De forma similar, se **debe seleccionar la rutina de comprobación UiaScreenReader** para que se muestre la pestaña Lector de pantalla de **UIA.**

En la siguiente captura de pantalla se muestra la pestaña Lector de pantalla de UIA con una comprobación de ejemplo Bloc de notas.

![Pestaña del lector de pantalla de accchecker que muestra los resultados de la comprobación de ejemplo](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a>Pestañas árbol MSAA y UIA

La ejecución de cualquier rutina de comprobación hace que AccChecker compile todos los elementos visibles en el destino de comprobación y los muestre jerárquicamente en la pestaña Árbol **de MSAA** y en la pestaña **Árbol de UIA.** En la siguiente captura de pantalla se muestra la pestaña Árbol de MSAA con la jerarquía de elementos para Bloc de notas.

![accchecker msaa tree tab (pestaña de árbol de accchecker msaa)](images/accchecker-tree-tab.png)

## <a name="file-menu"></a>Menú Archivo




| Menú | Comando | Descripción | 
|------|---------|-------------|
| <strong>Archivo</strong>${REMOVE}$<br /> | <strong>Abrir</strong> | Proporciona las siguientes opciones.<br /><ul><li><strong>DLL de comprobaciones</strong> Abre un archivo DLL de verificación. Las comprobaciones nativas de AccChecker se encapsulan en un archivo DLL independiente (VerificationRoutines.dll). Este diseño permite a los equipos de prueba crear su propio conjunto de comprobaciones en función de la plataforma de interfaz de usuario que se está probando.</li><li><strong>Archivo de registro</strong> Permite elegir un archivo de registro de comprobación para abrir.</li></ul> | 
| <strong>Carga automática de las comprobaciones disponibles</strong> | Carga automáticamente todas las comprobaciones de AccChecker disponibles. | 
| <strong>Guardar registro</strong> | Guarde el registro de comprobación como XML o como texto sin formato. El texto sin formato es más legible. | 
| <strong>Guardar supresión</strong> | Guarde el registro de supresión como XML. Este archivo especifica los mensajes de comprobación que se omitirán en las pruebas de regresión. | 
| <strong>Salir</strong> | Cierra la herramienta AccChecker. | 
| <strong>Comprobaciones</strong>${REMOVE}$<br /> | <strong>Ejecutar ahora</strong> | Ejecute las rutinas de comprobación especificadas para el destino de comprobación elegido. | 
| <strong>Habilitar todo</strong> | Active todas las casillas de verificación rutinarias. | 
| <strong>Deshabilitar todo</strong> | Desactive todas las casillas de verificación rutinarias. | 
| <strong>Opciones</strong> | <strong>Always On superior</strong> | Haga que AccChecker sea la ventana más alta en el orden Z. | 
| <strong>Ayuda</strong>${REMOVE}$<br /> | <strong>Ayuda</strong> | Mostrar información de ayuda. | 
| <strong>Acerca de</strong> | Muestre la versión de AccChecker y una dirección de correo electrónico para ponerse en contacto con Microsoft sobre AccChecker. | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





