---
title: User-Selected compresores
description: User-Selected compresores
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- Administrador de compresión de vídeo (VCM), compresores seleccionados por el usuario
- VCM (Administrador de compresión de vídeo), compresores seleccionados por el usuario
- ICCompressorChoose función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994391"
---
# <a name="user-selected-compressors"></a>User-Selected compresores

Al comprimir los datos, la aplicación puede usar la función [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para crear un cuadro de diálogo en el que el usuario pueda seleccionar el compresor. Puede especificar marcas para esta función para permitir que el usuario especifique la frecuencia del fotograma clave y la velocidad de datos de la película, o para mostrar una ventana de vista previa.

El compresor seleccionado por el usuario se abre automáticamente y su identificador se devuelve en el miembro HIC de la estructura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) especificada en **ICCompressorChoose**.

Si usa **ICCompressorChoose**, use la función [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) para cerrar el compresor y liberar los recursos asociados a la estructura **COMPVARS** .

 

 




