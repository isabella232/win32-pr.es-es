---
title: Compresión de secuencia
description: Compresión de secuencia
ms.assetid: ea24088d-6a52-4d4e-8496-5b6a6616f684
keywords:
- administrador de compresión de vídeo (VCM), compresión de secuencia
- VCM (administrador de compresión de vídeo), compresión de secuencia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8485c31361540ae0e0e9569453bc610d10d88d3d
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372253"
---
# <a name="sequence-compression"></a>Compresión de secuencia

La aplicación puede usar las funciones [**ICSeqCompressFrame,**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe) [**ICSeqCompressFrameStart**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)y [**ICSeqCompressFrameEnd**](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend) para comprimir una secuencia de fotogramas. Estas funciones usan los datos almacenados en la [**estructura COMPVARS.**](/windows/desktop/api/Vfw/ns-vfw-compvars) Las aplicaciones usan [**la función ICCompressorChoose**](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose) para permitir al usuario seleccionar un reancho, abrirlo y establecer los parámetros de compresión en la estructura **COMPVARS.** sin embargo, las aplicaciones pueden establecer los parámetros de la estructura manualmente.

Para que una aplicación pueda empezar a comprimir una secuencia de fotogramas, debe usar **ICSeqCompressFrameStart para** asignar los recursos necesarios. Una vez asignados los recursos, la aplicación puede usar **ICSeqCompressFrame** para comprimir cada fotograma individualmente. La frecuencia de fotogramas y la frecuencia de fotogramas clave que se usan para comprimir la secuencia se especifican en los miembros de la **estructura COMPVARS.** El valor devuelto de **ICSeqCompressFrame** apunta a los datos comprimidos.

Cuando una aplicación termina de comprimir una secuencia, puede usar **ICSeqCompressFrameEnd** para liberar los recursos del sistema asignados para **ICSeqCompressFrameStart.** Para liberar los recursos asignados para la estructura **COMPVARS,** la aplicación puede usar la [**función ICCompressorFree.**](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)

 

 




