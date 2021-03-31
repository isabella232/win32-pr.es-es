---
title: Operaciones de StoClien
description: En el ejemplo StoClien se muestra cómo el cliente usa el almacenamiento estructurado. A continuación se resumen las operaciones de StoClien.
ms.assetid: 55498665-520b-4a83-a3d1-22d3ed15863e
keywords:
- Operaciones de StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1068fcf1e377456211e08020f41279be9b5e3b0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792951"
---
# <a name="stoclien-operations"></a>Operaciones de StoClien

En el ejemplo [StoClien](structured-storage-client-sample--stoclien-.md) se muestra cómo el cliente usa el almacenamiento estructurado. A continuación se resumen las operaciones de StoClien.

El área de cliente de la ventana de la aplicación [StoClien](structured-storage-client-sample--stoclien-.md) se usa para la presentación visual del dibujo de forma libre creado con un mouse o un dispositivo de tableta. Para dibujar con el mouse, mantenga presionado el botón primario del mouse mientras mueve el mouse. Al soltar el botón primario del mouse finaliza el dibujo de una línea.

A continuación se muestra un resumen de las operaciones desde el punto de vista de Stoclien.exe como un cliente COM de la Stoserve.dll servidor COM:

<dl> <dt>

<span id="File_Open"></span><span id="file_open"></span><span id="FILE_OPEN"></span>Archivo/abrir
</dt> <dd>

Muestra el cuadro de diálogo abrir para obtener un nombre y una ruta de acceso de un archivo de dibujo de papel existente para abrirlo. Valor predeterminado. Se supone la extensión de nombre de archivo PAP para estos archivos. Si se realizaron cambios en el dibujo existente cuando se elige este elemento de menú, se mostrará un cuadro de diálogo independiente en el que se preguntará al usuario si el dibujo actual debe guardarse en su archivo compuesto asociado.

</dd> <dt>

<span id="File_Save"></span><span id="file_save"></span><span id="FILE_SAVE"></span>Archivo/guardar
</dt> <dd>

Guarda el dibujo actual en su archivo compuesto asociado.

</dd> <dt>

<span id="File_Save_As"></span><span id="file_save_as"></span><span id="FILE_SAVE_AS"></span>Archivo/guardar como
</dt> <dd>

Muestra el cuadro de diálogo Guardar como para obtener el nombre y la ruta de acceso de un nuevo archivo de dibujo de papel que se va a crear. El dibujo actual se convierte en el contenido guardado del nuevo archivo y el nuevo archivo se convierte en el nuevo archivo compuesto asociado para el dibujo.

</dd> <dt>

<span id="File_Exit"></span><span id="file_exit"></span><span id="FILE_EXIT"></span>Archivo/salir
</dt> <dd>

Sale de [StoClien](structured-storage-client-sample--stoclien-.md).

</dd> <dt>

<span id="Draw_Drawing_On"></span><span id="draw_drawing_on"></span><span id="DRAW_DRAWING_ON"></span>Dibujar y dibujar en
</dt> <dd>

Activa el dibujo entre el cliente de [StoClien](structured-storage-client-sample--stoclien-.md) y el objeto de copaper del servidor. Este comando bloquea el objeto de copapeles para que lo use exclusivamente este cliente y evita que otros clientes tengan acceso a la misma instancia de copaper en el servidor.

</dd> <dt>

<span id="Draw_Drawing_Off"></span><span id="draw_drawing_off"></span><span id="DRAW_DRAWING_OFF"></span>Dibujo/dibujo desactivado
</dt> <dd>

Desactiva el dibujo entre el cliente de [StoClien](structured-storage-client-sample--stoclien-.md) y el objeto de copaper del servidor. Este comando desbloquea el copapel para que este cliente lo use exclusivamente y permite que otros clientes tengan acceso a la misma instancia de copaper en el servidor.

</dd> <dt>

<span id="Draw_Redraw"></span><span id="draw_redraw"></span><span id="DRAW_REDRAW"></span>Dibujar o volver a dibujar
</dt> <dd>

Vuelve a dibujar en el cliente los datos de dibujo actuales contenidos en el objeto de copaper del servidor.

</dd> <dt>

<span id="Draw_Erase"></span><span id="draw_erase"></span><span id="DRAW_ERASE"></span>Dibujar o borrar
</dt> <dd>

Borra el contenido del dibujo actual y borra la imagen de la ventana. Selección de menú: lápiz/color muestra el cuadro de diálogo elegir color para obtener un nuevo color de lápiz para dibujar.

</dd> <dt>

<span id="Pen_Medium"></span><span id="pen_medium"></span><span id="PEN_MEDIUM"></span>Bolígrafo/medio
</dt> <dd>

Elige el ancho medio del dibujo. Una marca de verificación en esta opción de menú indica que Medium es el ancho actual del lápiz.

</dd> <dt>

<span id="Pen_Thick"></span><span id="pen_thick"></span><span id="PEN_THICK"></span>Lápiz/grueso
</dt> <dd>

Elige el ancho grueso del dibujo. Una marca de verificación en esta opción de menú indica que grueso es el ancho actual del lápiz.

</dd> <dt>

<span id="Pen_Thin"></span><span id="pen_thin"></span><span id="PEN_THIN"></span>Lápiz/fino
</dt> <dd>

Elige el ancho fino del dibujo. Una marca de verificación en esta opción de menú indica que fino es el ancho actual del lápiz.

</dd> <dt>

<span id="Sink_Connect"></span><span id="sink_connect"></span><span id="SINK_CONNECT"></span>Receptor/conexión
</dt> <dd>

Conecta la interfaz IPaperSink de COPaperSink al punto de conexión del objeto de copapeles PaperSink. La repintado de la imagen de dibujo actual en [StoClien](structured-storage-client-sample--stoclien-.md) se basa en la conexión del receptor. Una marca de verificación en esta opción de menú indica que el repintado está conectado.

</dd> <dt>

<span id="Sink_Disconnect"></span><span id="sink_disconnect"></span><span id="SINK_DISCONNECT"></span>Receptor/desconectar
</dt> <dd>

Desconecta la interfaz IPaperSink de COPaperSink del punto de conexión del objeto de copapeles PaperSink. La repintado de la imagen de dibujo actual en [StoClien](structured-storage-client-sample--stoclien-.md) se basa en la conexión del receptor. Una marca de verificación en esta opción de menú indica que la repintado está desconectada.

</dd> <dt>

<span id="Help_StoClien_Tutorial"></span><span id="help_stoclien_tutorial"></span><span id="HELP_STOCLIEN_TUTORIAL"></span>Ayuda/tutorial de StoClien
</dt> <dd>

Abre el archivo de tutorial de STOCLIEN.HTM en el explorador Web.

</dd> <dt>

<span id="Help_StoServe_Tutorial"></span><span id="help_stoserve_tutorial"></span><span id="HELP_STOSERVE_TUTORIAL"></span>Ayuda/tutorial de StoServe
</dt> <dd>

Abre el archivo de tutorial de STOSERVE.HTM en el explorador Web.

</dd> <dt>

<span id="Help_Read_Source_File"></span><span id="help_read_source_file"></span><span id="HELP_READ_SOURCE_FILE"></span>Ayuda/leer archivo de código fuente
</dt> <dd>

Muestra el cuadro de diálogo abrir para que pueda abrir un archivo de código fuente desde esta lección o desde otro en el Bloc de notas de Windows.

</dd> <dt>

<span id="Help_About_StoClien"></span><span id="help_about_stoclien"></span><span id="HELP_ABOUT_STOCLIEN"></span>Ayuda/acerca de StoClien
</dt> <dd>

Muestra el cuadro de diálogo acerca de para esta aplicación.

</dd> </dl>

En el ejemplo [StoClien](structured-storage-client-sample--stoclien-.md) se usan muchas de las clases de utilidad y los servicios proporcionados por [APPUTIL](./using-visual-studio.md). Para obtener más información sobre [APPUTIL](./using-visual-studio.md), consulte el código fuente de la biblioteca de [APPUTIL](./using-visual-studio.md) en el directorio de [APPUTIL](./using-visual-studio.md) relacionado y apputil.MD en el directorio principal del tutorial. Para obtener más información sobre [APPUTIL](./using-visual-studio.md), consulte [cómo compilar ejemplos](how-to-build-samples.md).

 

 