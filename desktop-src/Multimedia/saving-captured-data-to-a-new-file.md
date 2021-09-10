---
title: Guardar los datos capturados en un nuevo archivo
description: Guardar los datos capturados en un nuevo archivo
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS mensaje
- capFileSaveAs macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372073"
---
# <a name="saving-captured-data-to-a-new-file"></a>Guardar los datos capturados en un nuevo archivo

Si el usuario desea guardar los datos capturados, la aplicación debe guardar el contenido del archivo de captura en otro archivo mediante el mensaje [**\_ \_ \_ SAVEAS**](wm-cap-file-saveas.md) de ARCHIVO CAP de WM (o la macro [**capFileSaveAs).**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) Este mensaje no cambia el nombre ni el contenido del archivo de captura. La aplicación debe especificar un nombre para el nuevo archivo porque el archivo de captura conserva su nombre de archivo original.

Normalmente, un archivo de captura se preasigna para el segmento de captura más grande previsto y solo se puede usar una parte de él para capturar datos. Este mensaje copia solo la parte del archivo de captura que contiene los datos de captura.

 

 




