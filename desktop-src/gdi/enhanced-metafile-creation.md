---
description: Para crear un metarchivo mejorado, use la función CreateEnhMetaFile y proporcione los argumentos adecuados.
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: Creación de metarchivo mejorada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c89a4a05a18ecce4bc1b1fe3689e4f7a8dc64c833db4eac937da4f9a290dd3ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831995"
---
# <a name="enhanced-metafile-creation"></a>Creación de metarchivo mejorada

Para crear un metarchivo mejorado, use [**la función CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) y proporcione los argumentos adecuados. El sistema usa estos argumentos para mantener dimensiones de imagen, determinar si el metarchivo debe almacenarse en un disco o en memoria, y así sucesivamente.

Para mantener dimensiones de imagen en todos los dispositivos de salida, [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) requiere la resolución del dispositivo de referencia. Este *dispositivo de referencia* es el dispositivo en el que apareció la imagen por primera vez y el *controlador* de dominio de referencia es el contexto de dispositivo *asociado* al dispositivo de referencia. Al llamar a **la función CreateEnhMetaFile,** debe proporcionar un identificador que identifique este controlador de dominio. Puede obtener este identificador llamando a la [**función GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) [**o CreateDC.**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) También puede especificar **NULL como** identificador para usar el dispositivo de visualización actual para el dispositivo de referencia.

La mayoría de las aplicaciones almacenan imágenes de forma permanente y, por tanto, crean un metarchivo mejorado que se almacena en un disco. sin embargo, hay algunas instancias cuando esto no es necesario. Por ejemplo, una aplicación de procesamiento de palabras que proporciona funcionalidades de dibujo de gráficos podría almacenar un gráfico definido por el usuario en memoria como metarchivo mejorado y, a continuación, copiar los bits de metarchivo mejorados de la memoria en el archivo de documento del usuario. Una aplicación que requiere un metarchivo que se almacena permanentemente en un disco debe proporcionar el nombre de archivo cuando llama a [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea). Si no proporciona un nombre de archivo, el sistema trata automáticamente el metarchivo como un archivo temporal y lo almacena en memoria.

Puede agregar una descripción de texto opcional a un metarchivo que contenga información sobre la imagen y el autor. Una aplicación puede mostrar estas cadenas en el cuadro de diálogo Abrir archivo para proporcionar al usuario información sobre el contenido del metarchivo que le ayudará a seleccionar el archivo adecuado. Si una aplicación incluye la descripción de texto, debe proporcionar un puntero a la cadena cuando llama a [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea).

Cuando [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) se realiza correctamente, devuelve un identificador que identifica un contexto de dispositivo de metarchivo especial. Un contexto de dispositivo de metarchivo es único en el sentido de que está asociado a un archivo en lugar de a un dispositivo de salida. Cuando el sistema procesa una función GDI que recibió un identificador en un contexto de dispositivo de metarchivo, convierte la función GDI en un registro de metarchivo mejorado y anexa el registro al final del metarchivo mejorado.

Una vez completada una imagen y anexado el último registro al metarchivo mejorado, la aplicación puede cerrar el archivo llamando a la [**función CloseEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) Esta función cierra y elimina el contexto de dispositivo de metarchivo especial y devuelve un identificador que identifica el metarchivo mejorado.

Para eliminar un metarchivo de formato mejorado o un identificador de metarchivo de formato mejorado, llame a la [**función DeleteEnhMetaFile.**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)

 

 



