---
title: Transcodificar archivos (QASF)
description: Transcodificar archivos (QASF)
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- SDK de Windows Media Format, archivos de transcodificación (QASF)
- Windows Media Format SDK, DirectShow
- Formato de sistemas avanzados (ASF), archivos de transcodificación (QASF)
- ASF (formato de sistemas avanzados), archivos de transcodificación (QASF)
- Advanced Systems Format (ASF), DirectShow
- ASF (formato de sistemas avanzados), DirectShow
- DirectShow, transcodificación de archivos (QASF)
- SDK de Windows Media Format, QASF
- Advanced Systems Format (ASF), QASF
- ASF (formato de sistemas avanzados), QASF
- DirectShow, QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14387a65538d411bcd41b4b907f2adbab2089f71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104551254"
---
# <a name="transcoding-files-qasf"></a>Transcodificar archivos (QASF)

Puede crear un gráfico de filtros de transcodificación de archivos mediante el [escritor ASF de WM](wm-asf-writer-filter.md) de varias maneras. La manera más fácil es crear, configurar y agregar el escritor ASF de WM al gráfico de filtro y, a continuación, usar el método **IGraphBuilder:: RenderFile** para compilar el gráfico automáticamente.

Una manera alternativa es agregar cada filtro manualmente al gráfico y conectar los pin. Después de agregar el escritor ASF de WM, configúrelo con los métodos **IConfigAsfWriter** si el perfil predeterminado no es adecuado y conecte las clavijas de entrada del escritor ASF de WM a los pin de salida correspondientes en los filtros de nivel superior.

En la ilustración siguiente se muestran configuraciones típicas del gráfico de filtros de transcodificación ASF de WM.

![gráficos de filtros de transcodificación típicos](images/asf-transcode.png)

 

 




