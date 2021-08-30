---
title: Guardar contenido grabado
description: Guardar contenido grabado
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- Macro MCIWndSave
- Macro MCIWndSaveDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c097da1970aafa67fd9d5e94dc37024da2d2a29c3a04f2b2f5739f434b87e21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805475"
---
# <a name="saving-recorded-content"></a>Guardar contenido grabado

Después de completar la grabación, puede guardar el contenido mediante la macro [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) o [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) o mediante la función [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) con **MCIWndSave**. La **macro MCIWndSave** guarda los datos en el archivo asociado a la ventana MCIWnd. La **macro MCIWndSaveDialog** permite al usuario especificar un nombre de archivo y guardar los datos registrados en el archivo especificado. La **función GetSaveFileNamePreview** muestra el cuadro de diálogo **SaveAs** para elegir un archivo y permite al usuario obtener una vista previa (reproducir) del archivo. Cuando se especifica el nombre de un archivo existente en el cuadro de diálogo **SaveAs,** **GetSaveFileNamePreview** proporciona un pequeño control en el cuadro de diálogo para permitir que el usuario obtenga una vista previa del contenido del archivo. Puede guardar los datos registrados en un archivo seleccionado con **GetSaveFileNamePreview** mediante **MCIWndSave**.

 

 




