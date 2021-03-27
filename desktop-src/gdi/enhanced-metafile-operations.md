---
description: 'Puede usar el identificador de un metarchivo mejorado para realizar las tareas siguientes:'
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: Operaciones de metarchivo mejoradas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ba9e2ac2f14c4436c039a66cc3211b471c0461
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155625"
---
# <a name="enhanced-metafile-operations"></a>Operaciones de metarchivo mejoradas

Puede usar el identificador de un metarchivo mejorado para realizar las tareas siguientes:

-   Mostrar la imagen almacenada en un metarchivo mejorado.
-   Cree copias de un metarchivo mejorado.
-   Edite un metarchivo mejorado.
-   Recupere la descripción opcional almacenada en un metarchivo mejorado.
-   Recupera una copia de un encabezado de metarchivo mejorado.
-   Recupera una versión binaria de un metarchivo mejorado.
-   Enumera los colores de la paleta opcional.

Estas tareas se describen en las secciones que se encuentran en el resto de este tema.

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>Mostrar la imagen almacenada en un metarchivo mejorado

Puede mostrar la imagen almacenada en un metarchivo mejorado mediante la función [**PlayEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) . Pase la función a un identificador del metarchivo mejorado, sin tener que preocuparse por el formato de los registros de metarchivos mejorados. Sin embargo, a veces es conveniente enumerar los registros del metarchivo mejorado para buscar una función GDI determinada y modificar los parámetros de la función de alguna manera. Para ello, puede usar [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) y proporcionar una función de devolución de llamada, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), para procesar los registros de metarchivos mejorados. Para modificar los parámetros de un registro de metarchivo mejorado, debe conocer el formato de los parámetros en el registro.

## <a name="create-copies-of-an-enhanced-metafile"></a>Crear copias de un metarchivo mejorado

Algunas aplicaciones crean copias de seguridad (o duplicadas) temporales de un archivo antes de permitir al usuario modificar el original. Una aplicación puede crear una copia de seguridad de un metarchivo mejorado llamando a la función [**CopyEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) , proporcionando un identificador que identifica el metarchivo mejorado y proporcionando un puntero al nombre del nuevo archivo.

Para crear un metarchivo de formato mejorado basado en memoria, llame a la función [**SetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits) .

## <a name="edit-an-enhanced-metafile"></a>Editar un metarchivo mejorado

La mayoría de las aplicaciones de dibujo, Ilustración y diseño asistido por PC (CAD) requieren un medio para editar una imagen almacenada en un metarchivo mejorado. Aunque la edición de un metarchivo mejorado es una tarea compleja, puede usar la función [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) en combinación con otras funciones para proporcionar esta funcionalidad en la aplicación. La función **EnumEnhMetaFile** y su función de devolución de llamada asociada, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), permiten que la aplicación procese registros individuales en un metarchivo mejorado.

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>Recuperar la descripción opcional almacenada en un metarchivo mejorado

Algunas aplicaciones muestran la descripción de texto de un metarchivo mejorado con el nombre de archivo correspondiente en el cuadro de diálogo **abrir** . Puede determinar si esta cadena existe en un metarchivo mejorado recuperando el encabezado del metarchivo con la función [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) y examinando uno de sus miembros. Si la cadena existe, la aplicación la recupera mediante una llamada a la función [**GetEnhMetaFileDescription**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona) .

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>Recuperar una versión binaria de un metarchivo mejorado

Puede recuperar el contenido de un metarchivo mediante una llamada a la función [**GetEnhMetaFileBits**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) . sin embargo, antes de recuperar el contenido, debe especificar el tamaño del archivo. Para obtener el tamaño, puede usar la función [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) y examinar el miembro adecuado.

## <a name="enumerate-the-colors-in-the-optional-palette"></a>Enumerar los colores de la paleta opcional

Para lograr colores coherentes cuando se muestra una imagen en varios dispositivos de salida, puede llamar a la función [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) y almacenar una paleta lógica en un metarchivo mejorado. Una aplicación que muestra la imagen almacenada en el metarchivo mejorado recupera esta paleta y llama a la función [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) antes de mostrar la imagen. Para determinar si una paleta está almacenada en un metarchivo mejorado, recupere el encabezado del metarchivo y examine el miembro adecuado. Si existe una paleta, puede llamar a la función [**GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) para recuperar la paleta lógica.

 

 
