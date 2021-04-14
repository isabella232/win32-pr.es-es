---
title: La interfaz gráfica de usuario de AccChecker
description: En este tema se describen los elementos que componen la GUI de AccChecker.
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26d847d1bc198958ca28dd77d67b0e99b9d7745
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104555404"
---
# <a name="the-accchecker-graphical-user-interface"></a>La interfaz gráfica de usuario de AccChecker

En este tema se describen los elementos que componen la GUI de AccChecker.

-   [Pestaña comprobaciones](#verifications-tab)
-   [Pestaña resultados](#results-tab)
-   [Pestañas de lector de pantalla de MSAA y UIA](#msaa-and-uia-screen-reader-tabs)
-   [Pestañas de los árboles MSAA y UIA](#msaa-and-uia-tree-tabs)
-   [Menú Archivo](#file-menu)
-   [Temas relacionados](#related-topics)

## <a name="verifications-tab"></a>Pestaña comprobaciones

AccChecker se inicia con la vista predeterminada de la pestaña **comprobaciones** :

![Captura de pantalla que muestra la pestaña ' comprobaciones ' en el comprobador de accesibilidad U I.](images/accchecker-verifications-tab.png)

La pestaña **comprobaciones** contiene los siguientes componentes.

-   **Selector de destino de comprobación** Ofrece las siguientes opciones para seleccionar un control o una aplicación de destino.
    -   Elija un destino en la lista desplegable rellenada previamente. Esta lista contiene todos los HWND de nivel superior identificados en el inicio.
    -   Elija un HWND en función de la ubicación del cursor del mouse (los controles seleccionables se resaltan con un rectángulo rojo). Esta opción permite seleccionar cualquier objeto visible que tenga un HWND.
    -   Escriba un HWND determinado.
-   **Lista de comprobación de rutinas de comprobación** Proporciona la capacidad de seleccionar la rutina de comprobación deseada que se va a realizar en una aplicación o un control. Vea rutinas de comprobación para obtener más información.
-   **Selector de archivos de supresión de errores y advertencias** Los archivos de supresión se generan en la pestaña **resultados** de la comprobación. Al hacer clic con el botón secundario en un mensaje de error o advertencia y seleccionar **suprimir** en el menú contextual, se establece una marca para ese mensaje. Si la casilla de **supresión** está activada, las entradas suprimidas aparecen en la lista. Una entrada suprimida se puede eliminar mediante el mismo menú contextual que se usa para suprimirla.

    Un archivo de supresión se guarda en formato XML seleccionando **Guardar supresión** en el menú **archivo** . Este archivo se usa en ejecuciones de comprobación posteriores en las que se ocultan los mensajes. Para quitar el archivo de supresión, haga clic en **Borrar**. Para obtener información sobre mensajes específicos, vea mensajes de registro de comprobación. Use **Guardar registro** en el menú **archivo** para guardar la lista completa como un archivo de registro en XML o como un archivo de texto con formato.

    ![accchecker pestaña resultados con el elemento de contexto suprimir resaltado](images/accchecker-results-tab-with-suppress.png)

    En el ejemplo siguiente se muestra el contenido de un archivo de supresión generado al ejecutar las comprobaciones de **propiedades** en la aplicación del panel de control de Firewall de Windows. El error con el identificador "ElementHasNoName" se eligió para su supresión en este ejemplo.

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
    -   **Todo** Incluye todos los resultados independientemente de la prioridad.
    -   **Solo P1** Incluya solo los resultados de prioridad 0 y prioridad 1.
    -   **Solo P1 P2** Incluya los resultados de la prioridad 0 a la prioridad 2.
-   **Ejecutar comprobaciones seleccionadas** Proporciona el botón **ejecutar comprobaciones** para iniciar el proceso de comprobación. Mientras se ejecutan las comprobaciones, el botón cambia a **Cancelar comprobaciones** y se puede usar para detener las comprobaciones después de que se complete la actual.

## <a name="results-tab"></a>Pestaña Resultados

La pestaña **resultados** se rellena después de que se hayan completado las tareas de comprobación seleccionadas. Consta de los siguientes componentes.

-   La lista de mensajes, que muestra los mensajes de error, de advertencia e informativos generados por las tareas de comprobación seleccionadas. Los mensajes mostrados se pueden filtrar por tipo mediante las casillas situadas encima de la lista de mensajes.
-   Los detalles del mensaje y una captura de pantalla del destino de la comprobación. Al seleccionar un mensaje en la lista de mensajes se muestran más detalles y se resalta el elemento correspondiente en el panel Captura de pantalla. El botón **visualizar** , cambia AccChecker a la pestaña de **árbol de MSAA** . Si se resalta un error en la pestaña **resultados** , el elemento correspondiente se resalta en la pestaña **árbol de MSAA** .

Al hacer clic con el botón secundario en un mensaje, se expone un menú contextual con los elementos siguientes.

-   **Suprimir** Agrega el mensaje a la lista de supresión.
-   **Copiar al portapapeles** Copia los detalles del mensaje en el portapapeles.
-   **Visualizar** Cambia AccChecker a la pestaña de **árbol de MSAA** . Se resalta el elemento que se corresponde con el error seleccionado.
-   **Ayuda** de Muestra información adicional sobre el mensaje.

## <a name="msaa-and-uia-screen-reader-tabs"></a>Pestañas de lector de pantalla de MSAA y UIA

Las pestañas lector de pantalla de MSAA y lector de pantalla de UIA son similares. Ambos muestran una transcripción de los elementos encontrados en un recorrido simulado del destino de la comprobación por un lector de pantalla, excepto en que se muestra la implementación de MSAA y el otro muestra la implementación de UIA.

Los elementos se desplazan y se registran de la misma forma que un lector de pantalla los leería. La información que se presenta en esta pestaña es esencial para confirmar que solo se anuncia información útil y relevante. Por ejemplo, es aceptable un nombre de control de sonido normal como "MenuItem Edit" o "PushButton Close". sin embargo, el nombre de un control que no tiene sentido, como "CPNavPanel22" o "DefaultValue1", no es aceptable. El botón **visualizar** , hace que AccChecker cambie al árbol de **MSAA** o a la pestaña de **árbol de UIA** . Si un elemento está resaltado en la pestaña **lector de pantalla** , el elemento correspondiente se resalta en la pestaña árbol de **MSAA** o en el **árbol de UIA** .

La rutina de comprobación de **ScreenReader** en la que **se debe realizar** la comprobación debe estar seleccionada en la pestaña **comprobaciones** para que se muestre la **pestaña lector de pantalla de MSAA** . Del mismo modo, se debe seleccionar la rutina de comprobación **UiaScreenReader** para que se muestre la pestaña **lector de pantalla de UIA** .

En la captura de pantalla siguiente se muestra la pestaña lector de pantalla de UIA con una comprobación de ejemplo del Bloc de notas.

![accchecker pestaña lector de pantalla que muestra los resultados de comprobación de ejemplo](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a>Pestañas de los árboles MSAA y UIA

Al ejecutar cualquier rutina de comprobación, AccChecker se compilan todos los elementos visibles en el destino de comprobación y se muestran jerárquicamente en la pestaña de **árbol de MSAA** y en la pestaña de **árbol de UIA** . En la captura de pantalla siguiente se muestra la pestaña árbol de MSAA con la jerarquía de elementos del Bloc de notas.

![accchecker pestaña de árbol de MSAA](images/accchecker-tree-tab.png)

## <a name="file-menu"></a>Menú Archivo



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Menú</th>
<th>Get-Help</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="5"><strong>Archivo</strong>$ {Remove} $<br />
</td>
<td><strong>Abrir</strong></td>
<td>Proporciona las siguientes opciones.<br/>
<ul>
<li><strong>Comprobaciones dll</strong> Abre un archivo DLL de comprobación. Las comprobaciones de AccChecker nativas se encapsulan en un archivo DLL independiente (VerificationRoutines.dll). Este diseño permite a los equipos de pruebas crear su propio conjunto de comprobaciones basadas en la plataforma de interfaz de usuario que se está probando.</li>
<li><strong>Archivo de registro</strong> Permite elegir un archivo de registro de comprobación para abrirlo.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Cargar automáticamente comprobaciones disponibles</strong></td>
<td>Carga automáticamente todas las comprobaciones de AccChecker disponibles.</td>

</tr>
<tr class="odd">
<td><strong>Guardar registro</strong></td>
<td>Guarde el registro de comprobación como XML o como texto sin formato. El texto sin formato es más legible.</td>

</tr>
<tr class="even">
<td><strong>Guardar supresión</strong></td>
<td>Guarde el registro de supresión como XML. Este archivo especifica los mensajes de comprobación que se van a omitir en las pruebas de regresión.</td>

</tr>
<tr class="odd">
<td><strong>Salir</strong></td>
<td>Cierra la herramienta AccChecker.</td>

</tr>
<tr class="even">
<td rowspan="3"><strong>Comprobaciones</strong>$ {Remove} $<br />
</td>
<td><strong>Ejecutar ahora</strong></td>
<td>Ejecute las rutinas de comprobación tal y como se especifica para el destino de comprobación elegido.</td>
</tr>
<tr class="odd">
<td><strong>Habilitar todo</strong></td>
<td>Active todas las casillas de rutina de comprobación.</td>

</tr>
<tr class="even">
<td><strong>Deshabilitar todo</strong></td>
<td>Desactive las casillas de todas las rutinas de comprobación.</td>

</tr>
<tr class="odd">
<td><strong>Opciones</strong></td>
<td><strong>Always On superior</strong></td>
<td>AccChecker la ventana superior en el orden z.</td>
</tr>
<tr class="even">
<td rowspan="2"><strong>Ayuda</strong>$ {Remove} $<br />
</td>
<td><strong>Ayuda</strong></td>
<td>Mostrar información de la ayuda.</td>
</tr>
<tr class="odd">
<td><strong>Acerca de</strong></td>
<td>Muestra la versión de AccChecker y una dirección de correo electrónico para ponerse en contacto con Microsoft sobre AccChecker.</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[UI Accessibility Checker](ui-accessibility-checker.md)
</dt> </dl>

 

 





