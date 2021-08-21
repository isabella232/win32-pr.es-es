---
title: User-Selected de datos
description: User-Selected de datos
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Administrador de compresión de vídeo (VCM), los dispositivos seleccionados por el usuario
- VCM (administrador de compresión de vídeo), elementos seleccionados por el usuario
- Función ICCompressorChoose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c855acb1ecd69876009d0cc3eb6a3b3f4129cc252183e40c5b2d00289be82842
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370805"
---
# <a name="user-selected-compressors"></a>User-Selected de datos

Al comprimir los datos, la aplicación puede usar la función [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para crear un cuadro de diálogo en el que el usuario pueda seleccionar el objeto. Puede especificar marcas para esta función para permitir al usuario especificar la frecuencia de fotogramas clave y la velocidad de datos de la película, o para mostrar una ventana de vista previa.

El objeto seleccionado por el usuario se abre automáticamente y su identificador se devuelve en el miembro hic de la estructura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) especificada en **ICCompressorChoose**.

Si usa **ICCompressorChoose,** use la función [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) para cerrar el árbol y liberar los recursos asociados a la **estructura COMPVARS.**

 

 




