---
title: Guardar contenido grabado
description: Guardar contenido grabado
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- MCIWndSave macro
- Macro MCIWndSaveDialog
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372464"
---
# <a name="saving-recorded-content"></a>Guardar contenido grabado

Después de completar la grabación, puede guardar el contenido mediante la macro [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) o [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) o mediante la función [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) con **MCIWndSave**. La **macro MCIWndSave** guarda los datos en el archivo asociado a la ventana MCIWnd. La **macro MCIWndSaveDialog** permite al usuario especificar un nombre de archivo y guardar los datos registrados en el archivo especificado. La **función GetSaveFileNamePreview** muestra el cuadro de diálogo **SaveAs** para elegir un archivo y permite al usuario obtener una vista previa (reproducir) del archivo. Cuando se especifica el nombre de un archivo existente en el cuadro de diálogo **SaveAs,** **GetSaveFileNamePreview** proporciona un pequeño control en el cuadro de diálogo para permitir que el usuario obtenga una vista previa del contenido del archivo. Puede guardar los datos registrados en un archivo seleccionado **con GetSaveFileNamePreview** mediante **MCIWndSave**.

 

 




