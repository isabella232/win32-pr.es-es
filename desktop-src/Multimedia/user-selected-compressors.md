---
title: User-Selected Descuados
description: User-Selected Descuados
ms.assetid: 38569f9c-2df3-4959-990b-5c33203ff916
keywords:
- administrador de compresión de vídeo (VCM), permisos seleccionados por el usuario
- VCM (administrador de compresión de vídeo), vehículos seleccionados por el usuario
- Función ICCompressorChoose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbbba48b919265ea6e0bab2c3d891f628c4e660a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372265"
---
# <a name="user-selected-compressors"></a>User-Selected Descuados

Al comprimir datos, la aplicación puede usar la función [**ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para crear un cuadro de diálogo en el que el usuario pueda seleccionar el reancho. Puede especificar marcas para esta función para permitir al usuario especificar la frecuencia de fotogramas clave y la velocidad de datos de la película, o para mostrar una ventana de vista previa.

El objeto seleccionado por el usuario se abre automáticamente y su identificador se devuelve en el miembro hic de la estructura [**COMPVARS**](/windows/desktop/api/Vfw/ns-vfw-compvars) especificada en **ICCompressorChoose**.

Si usa **ICCompressorChoose,** use la función [**ICCompressorFree**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree) para cerrar el proceso y liberar todos los recursos asociados a la estructura **COMPVARS.**

 

 




