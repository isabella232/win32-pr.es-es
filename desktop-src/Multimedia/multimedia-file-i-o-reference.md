---
title: Referencia de E/S de archivos multimedia
description: Referencia de E/S de archivos multimedia
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows multimedia, referencia de E/S de archivos
- multimedia, referencia de E/S de archivo
- entrada multimedia, referencia de E/S de archivo
- E/S de archivos multimedia, referencia
- E/S de archivo, referencia
- entrada y salida (E/S),referencia
- E/S (entrada y salida),referencia
- referencia de E/S de archivos multimedia, acerca de
- Referencia de E/S de archivos multimedia, acerca de
- referencia de E/S de archivo, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06d61b06c16b12a9276adc0d858a3170dae2f7d636cc63a9ac6cc032a65c978c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136906"
---
# <a name="multimedia-file-io-reference"></a>Referencia de E/S de archivos multimedia

En esta sección se describen las funciones, macros, mensajes y estructuras asociados a la entrada y salida de archivos multimedia. Estos elementos se agrupan como se muestra a continuación.

## <a name="basic-io"></a>E/S básica

-   [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a>E/S en búfer

-   [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))
-   [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a>E/S de RIFF

-   [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a>Procedimientos de E/S personalizados

-   [**IOProc**](/previous-versions//dd757098(v=vs.85))
-   [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [**MMIOM \_ CLOSE**](mmiom-close.md)
-   [**MMIOM \_ OPEN**](mmiom-open.md)
-   [**MMIOM \_ READ**](mmiom-read.md)
-   [**CAMBIO DE NOMBRE DE MMIOM \_**](mmiom-rename.md)
-   [**MMIOM \_ SEEK**](mmiom-seek.md)
-   [**MMIOM \_ WRITE**](mmiom-write.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)
-   [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[E/S de archivos multimedia](multimedia-file-i-o.md)
</dt> </dl>

 

 