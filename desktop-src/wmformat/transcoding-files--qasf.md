---
title: Archivos de transcodificación (QASF)
description: Archivos de transcodificación (QASF)
ms.assetid: c6dad6cf-4781-4204-883b-cdb33aff5e27
keywords:
- Windows SDK de formato multimedia, archivos de transcodificación (QASF)
- Windows SDK de formato multimedia, DirectShow
- Formato de sistemas avanzados (ASF), archivos de transcodificación (QASF)
- ASF (formato de sistemas avanzados), archivos de transcodificación (QASF)
- Formato de sistemas avanzados (ASF),DirectShow
- ASF (formato de sistemas avanzados),DirectShow
- DirectShow archivos de transcodificación (QASF)
- Windows SDK de formato multimedia, QASF
- Formato de sistemas avanzados (ASF),QASF
- ASF (formato de sistemas avanzados),QASF
- DirectShow,QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7465c98edd39d173623f202dfdf7845dfeda648c52106f2241ea596d54caa00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929174"
---
# <a name="transcoding-files-qasf"></a>Archivos de transcodificación (QASF)

Puede crear un gráfico de filtros de transcodificación de archivos mediante [WM ASF Writer](wm-asf-writer-filter.md) de varias maneras. La manera más fácil es crear, configurar y agregar asf writer de WM al gráfico de filtros y, a continuación, usar el método **IGraphBuilder::RenderFile** para compilar el gráfico automáticamente.

Una manera alternativa es agregar cada filtro manualmente al gráfico y conectar los pines. Después de agregar WM ASF Writer, configúrelo mediante los métodos **IConfigAsfWriter** si el perfil predeterminado no es adecuado y conecte los pines de entrada de WM ASF Writer a los pins de salida correspondientes en los filtros ascendentes.

En la ilustración siguiente se muestran las configuraciones de gráficos de filtro de transcodificación de WM ASF Writer típicas.

![gráficos de filtro de transcodificación típicos](images/asf-transcode.png)

 

 




