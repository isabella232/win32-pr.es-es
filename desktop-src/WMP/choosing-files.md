---
title: Elección de archivos
description: Elección de archivos
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- crear máscaras, elegir archivos
- Reproductor de Windows Media máscaras, elegir archivos
- máscaras, elegir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed90a5813880c87dbaf297808cc79c65ed066eb1585ba63ddd97d0305199230
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764255"
---
# <a name="choosing-files"></a>Elección de archivos

Si desea elegir un archivo, puede usar código similar al ejemplo de lista de reproducción, pero sustituya lo siguiente por la sección PLAYELEMENT:


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



Esta línea usará el método **openDialog** de **THEME** para definir una **dirección URL** para el reproductor. Puede usarlo para elegir archivos que no estén en listas de reproducción.

Puede ver un ejemplo de **openDialog** de trabajo similar en la sección de ejemplo del SDK.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Guía de creación de máscaras**](skin-creation-guide.md)
</dt> </dl>

 

 




