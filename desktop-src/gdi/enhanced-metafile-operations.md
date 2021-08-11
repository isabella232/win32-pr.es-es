---
description: 'Puede usar el identificador de un metarchivo mejorado para realizar las siguientes tareas:'
ms.assetid: 8f887c38-6cfa-4918-aa44-dd5fb837b40b
title: Operaciones mejoradas de metarchivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5daf08ef5d8d48b81aea4daa5d2696ececec3fce44b1303c9ff7ccd692151a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118250289"
---
# <a name="enhanced-metafile-operations"></a>Operaciones mejoradas de metarchivo

Puede usar el identificador de un metarchivo mejorado para realizar las siguientes tareas:

-   Muestra la imagen almacenada en un metarchivo mejorado.
-   Cree copias de un metarchivo mejorado.
-   Edite un metarchivo mejorado.
-   Recupere la descripción opcional almacenada en un metarchivo mejorado.
-   Recupera una copia de un encabezado de metarchivo mejorado.
-   Recuperar una versión binaria de un metarchivo mejorado.
-   Enumere los colores de la paleta opcional.

Estas tareas se de abordan en las secciones del resto de este tema.

## <a name="display-the-picture-stored-in-an-enhanced-metafile"></a>Mostrar la imagen almacenada en un metarchivo mejorado

Puede mostrar la imagen almacenada en un metarchivo mejorado mediante la [**función PlayEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile) Pase a la función un identificador al metarchivo mejorado, sin preocuparse por el formato de los registros de metarchivo mejorados. Sin embargo, a veces es conveniente enumerar los registros del metarchivo mejorado para buscar una función GDI determinada y modificar los parámetros de la función de alguna manera. Para ello, puede usar [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) y proporcionar una función de devolución de llamada, [**EnhMetaFileProc**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc), para procesar los registros de metarchivo mejorados. Para modificar los parámetros de un registro de metarchivo mejorado, debe conocer el formato de los parámetros dentro del registro.

## <a name="create-copies-of-an-enhanced-metafile"></a>Crear copias de un metarchivo mejorado

Algunas aplicaciones crean copias de seguridad temporales (o duplicadas) de un archivo antes de permitir que el usuario modifique el original. Una aplicación puede crear una copia de seguridad de un metarchivo mejorado llamando a la función [**CopyEnhMetaFile,**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea) suministrando un identificador que identifica el metarchivo mejorado y suministrando un puntero al nombre del nuevo archivo.

Para crear un metarchivo de formato mejorado basado en memoria, llame a la [**función SetEnhMetaFileBits.**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)

## <a name="edit-an-enhanced-metafile"></a>Edición de un metarchivo mejorado

La mayoría de las aplicaciones de dibujo, ilustración y diseño asistido por PC (CAD) requieren un medio para editar una imagen almacenada en un metarchivo mejorado. Aunque editar un metarchivo mejorado es una tarea compleja, puede usar la función [**EnumEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile) en combinación con otras funciones para proporcionar esta funcionalidad en la aplicación. La **función EnumEnhMetaFile** y su función de devolución de llamada asociada, [**EnhMetaFileProc,**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)permiten a la aplicación procesar registros individuales en un metarchivo mejorado.

## <a name="retrieve-the-optional-description-stored-in-an-enhanced-metafile"></a>Recuperar la descripción opcional almacenada en un metarchivo mejorado

Algunas aplicaciones muestran la descripción de texto de un metarchivo mejorado con el nombre de archivo correspondiente en el **cuadro de diálogo** Abrir. Puede determinar si esta cadena existe en un metarchivo mejorado recuperando el encabezado del metarchivo con la función [**GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) y examinando uno de sus miembros. Si la cadena existe, la aplicación la recupera mediante una llamada a la [**función GetEnhMetaFileDescription.**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)

## <a name="retrieve-a-binary-version-of-an-enhanced-metafile"></a>Recuperar una versión binaria de un metarchivo mejorado

Puede recuperar el contenido de un metarchivo llamando a la [**función GetEnhMetaFileBits;**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits) sin embargo, antes de recuperar el contenido, debe especificar el tamaño del archivo. Para obtener el tamaño, puede usar la [**función GetEnhMetaFileHeader**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader) y examinar el miembro adecuado.

## <a name="enumerate-the-colors-in-the-optional-palette"></a>Enumerar los colores de la paleta opcional

Para lograr colores coherentes cuando se muestra una imagen en varios dispositivos de salida, puede llamar a la función [**CreatePalette**](/windows/desktop/api/Wingdi/nf-wingdi-createpalette) y almacenar una paleta lógica en un metarchivo mejorado. Una aplicación que muestra la imagen almacenada en el metarchivo mejorado recupera esta paleta y llama a la función [**RealizePalette**](/windows/desktop/api/Wingdi/nf-wingdi-realizepalette) antes de mostrar la imagen. Para determinar si una paleta está almacenada en un metarchivo mejorado, recupere el encabezado del metarchivo y examine el miembro adecuado. Si existe una paleta, puede llamar a la [**función GetEnhMetaFilePaletteEntries**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) para recuperar la paleta lógica.

 

 
