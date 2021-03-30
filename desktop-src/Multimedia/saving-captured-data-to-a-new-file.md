---
title: Guardar los datos capturados en un archivo nuevo
description: Guardar los datos capturados en un archivo nuevo
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- Mensaje WM_CAP_FILE_SAVEAS
- capFileSaveAs (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775985"
---
# <a name="saving-captured-data-to-a-new-file"></a>Guardar los datos capturados en un archivo nuevo

Si el usuario desea guardar los datos capturados, la aplicación debe guardar el contenido del archivo de captura en otro archivo mediante el [**mensaje \_ \_ \_ SaveAs archivo Cap de WM**](wm-cap-file-saveas.md) (o la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ). Este mensaje no cambia el nombre ni el contenido del archivo de captura. La aplicación debe especificar un nombre para el nuevo archivo, ya que el archivo de captura conserva su nombre de archivo original.

Normalmente, un archivo de captura está preasignado para el segmento de captura más grande previsto y solo una parte de él podría usarse para capturar los datos. Este mensaje solo copia la parte del archivo de captura que contiene los datos de captura.

 

 




