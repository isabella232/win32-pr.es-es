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
ms.openlocfilehash: 39ef5449e8d4e985217ee60f075d22b16dcc5c3b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265780"
---
# <a name="monitoring-the-progress-of-compressors-and-decompressors"></a>Supervisar el progreso de los descompresores y descomprimir

La aplicación puede supervisar el progreso de una operación larga realizada por un descomprimidor o descompresión mediante el envío de la dirección de una función de devolución de llamada. Puede usar la [**función ICSetStatusProc**](/windows/desktop/api/Vfw/nf-vfw-icsetstatusproc) para enviar la dirección al módulo o descompresión. Cuando el descomprimidor o descomprimido recibe esta dirección, envía mensajes de estado a la función. Estos mensajes indican si la operación se está iniciando, deteniendo, generando o continuando.

 

 




