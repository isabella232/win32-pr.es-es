---
title: Referencia de e/s de archivos multimedia
description: Referencia de e/s de archivos multimedia
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows multimedia, referencia de e/s de archivo
- multimedia, referencia de e/s de archivos
- entrada multimedia, referencia de e/s de archivo
- e/s de archivos multimedia, referencia
- e/s de archivo, referencia
- entrada y salida (e/s), referencia
- E/s (entrada y salida), referencia
- referencia de e/s de archivos multimedia, acerca de
- referencia de e/s de archivos multimedia, acerca de
- referencia de e/s de archivo, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103789765"
---
# <a name="multimedia-file-io-reference"></a>Referencia de e/s de archivos multimedia

En esta sección se describen las funciones, macros, mensajes y estructuras asociadas a la entrada y salida de archivos multimedia. Estos elementos se agrupan de la siguiente manera.

## <a name="basic-io"></a>E/s básicas

-   [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [**mmioRename**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a>E/s almacenada en búfer

-   [**mmioAdvance**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [**mmioFlush**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [**mmioGetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [**MMIOINFO**](/previous-versions//dd757322(v=vs.85))
-   [**mmioSetBuffer**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [**mmioSetInfo**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a>RIFF E/S

-   [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [**mmioDescend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [**mmioFOURCC**](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [**mmioStringToFOURCC**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a>Procedimientos de e/s personalizados

-   [**IOProc**](/previous-versions//dd757098(v=vs.85))
-   [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [**MMIOM \_ cerrar**](mmiom-close.md)
-   [**MMIOM \_ abrir**](mmiom-open.md)
-   [**MMIOM \_ lectura**](mmiom-read.md)
-   [**MMIOM \_ cambiar nombre**](mmiom-rename.md)
-   [**búsqueda de MMIOM \_**](mmiom-seek.md)
-   [**escritura de MMIOM \_**](mmiom-write.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)
-   [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[E/s de archivos multimedia](multimedia-file-i-o.md)
</dt> </dl>

 

 