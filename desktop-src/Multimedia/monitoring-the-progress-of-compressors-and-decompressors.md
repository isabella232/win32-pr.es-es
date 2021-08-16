---
title: Supervisar el progreso de los descompresores y descomprimir
description: Supervisar el progreso de los descompresores y descomprimir
ms.assetid: 6507be44-1916-46b2-bae3-c4fe633cdc5a
keywords:
- administrador de compresión de vídeo (VCM), supervisión
- VCM (administrador de compresión de vídeo), supervisión
- Función ICSetStatusProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44707cb6a8fbdb19b1d71fed6c71498b51936b9d089354277c6767586b4b8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373582"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Supervisar el progreso de los descompresores y descomprimir

La aplicación puede supervisar el progreso de una operación larga realizada por un descomprimidor o descompresión mediante el envío de la dirección de una función de devolución de llamada. Puede usar la [**función ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) para enviar la dirección al módulo o descompresión. Cuando el descomprimidor o descomprimido recibe esta dirección, envía mensajes de estado a la función. Estos mensajes indican si la operación se está iniciando, deteniendo, cediendo o continuando.

 

 




