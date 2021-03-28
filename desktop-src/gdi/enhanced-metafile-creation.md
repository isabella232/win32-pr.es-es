---
description: Puede crear un metarchivo mejorado mediante la función CreateEnhMetaFile, proporcionando los argumentos adecuados.
ms.assetid: b012e50e-a7f5-4687-9833-38dacc113d77
title: Creación mejorada de metarchivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080c350e41e895c5d4bf834a6f407cca5907743d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811960"
---
# <a name="enhanced-metafile-creation"></a>Creación mejorada de metarchivos

Puede crear un metarchivo mejorado mediante la función [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) , proporcionando los argumentos adecuados. El sistema utiliza estos argumentos para mantener las dimensiones de la imagen, determinar si el metarchivo debe almacenarse en un disco o en la memoria, etc.

Para mantener las dimensiones de la imagen en los dispositivos de salida, [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) requiere la resolución del dispositivo de referencia. Este *dispositivo de referencia* es el dispositivo en el que apareció por primera vez y el *controlador de dominio de referencia* es el contexto de *dispositivo* asociado al dispositivo de referencia. Al llamar a la función **CreateEnhMetaFile** , debe proporcionar un identificador que identifique este controlador de dominio. Para obtener este identificador, puede llamar a la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) o [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) . También puede especificar **null** como identificador para usar el dispositivo de pantalla actual para el dispositivo de referencia.

La mayoría de las aplicaciones almacenan imágenes de forma permanente y, por tanto, crean un metarchivo mejorado que se almacena en un disco. sin embargo, hay algunos casos en los que no es necesario. Por ejemplo, una aplicación de procesamiento de texto que proporciona funciones de dibujo de gráficos podría almacenar un gráfico definido por el usuario en la memoria como un metarchivo mejorado y, a continuación, copiar los bits de metarchivo mejorados de la memoria en el archivo de documento del usuario. Una aplicación que requiere un metarchivo almacenado permanentemente en un disco debe proporcionar el nombre de archivo cuando llama a [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea). Si no proporciona un nombre de archivo, el sistema lo trata automáticamente como un archivo temporal y lo almacena en la memoria.

Puede Agregar una descripción de texto opcional a un metarchivo que contenga información sobre la imagen y el autor. Una aplicación puede mostrar estas cadenas en el cuadro de diálogo Abrir archivo para proporcionar al usuario información sobre el contenido del metarchivo que le ayudará a seleccionar el archivo adecuado. Si una aplicación incluye la descripción del texto, debe proporcionar un puntero a la cadena cuando llama a [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea).

Cuando [**CreateEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea) se ejecuta correctamente, devuelve un identificador que identifica un contexto de dispositivo de metarchivo especial. Un contexto de dispositivo de metarchivo es único en que está asociado a un archivo en lugar de a un dispositivo de salida. Cuando el sistema procesa una función GDI que ha recibido un identificador de un contexto de dispositivo de metarchivo, convierte la función GDI en un registro de metarchivo mejorado y anexa el registro al final del metarchivo mejorado.

Una vez que se completa una imagen y se anexa el último registro al metarchivo mejorado, la aplicación puede cerrar el archivo mediante una llamada a la función [**CloseEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile) . Esta función cierra y elimina el contexto de dispositivo de metarchivo especial y devuelve un identificador que identifica el metarchivo mejorado.

Para eliminar un metarchivo de formato mejorado o un controlador de metarchivo con formato mejorado, llame a la función [**DeleteEnhMetaFile**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile) .

 

 



