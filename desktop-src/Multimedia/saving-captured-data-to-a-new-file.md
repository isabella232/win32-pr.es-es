---
title: Guardar los datos capturados en un nuevo archivo
description: Guardar los datos capturados en un nuevo archivo
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS mensaje
- capFileSaveAs macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f6f2f94ed1a7c7f7f8cae20b20c6fa4b5aa27e8105ab3f5dc33e60b7aff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892915"
---
# <a name="saving-captured-data-to-a-new-file"></a>Guardar los datos capturados en un nuevo archivo

Si el usuario desea guardar los datos capturados, la aplicación debe guardar el contenido del archivo de captura en otro archivo mediante el mensaje [**\_ \_ \_ SAVEAS**](wm-cap-file-saveas.md) de ARCHIVO CAP de WM (o la macro [**capFileSaveAs).**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) Este mensaje no cambia el nombre ni el contenido del archivo de captura. La aplicación debe especificar un nombre para el nuevo archivo porque el archivo de captura conserva su nombre de archivo original.

Normalmente, un archivo de captura se preasigna para el segmento de captura más grande previsto y solo se puede usar una parte de él para capturar datos. Este mensaje copia solo la parte del archivo de captura que contiene los datos de captura.

 

 




