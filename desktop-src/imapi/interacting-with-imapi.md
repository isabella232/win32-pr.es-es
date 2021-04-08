---
title: Interactuar con IMAPi
description: En los pasos siguientes se describe una interacción típica entre una aplicación y IMAPi.
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e68bee24cfe0724ed14d439b0789f5023338853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994299"
---
# <a name="interacting-with-imapi"></a>Interactuar con IMAPi

En los pasos siguientes se describe una interacción típica entre una aplicación y IMAPi.

1.  Cree una instancia de **MSDiscMasterObj** (mediante **CoCreateInstance**, punteros inteligentes a partir de una importación, etc.) y solicite la interfaz [**IDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster) .
2.  Obtenga acceso a IMAPi llamando a [**IDiscMaster:: Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open). Si esta llamada se realiza correctamente, la aplicación tiene acceso completo a todas las interfaces y métodos implementados en **MSDiscMasterObj**.
3.  Recupere el enumerador de formato del maestro de disco mediante [**EnumDiscMasterFormats**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats). Enumere el conjunto de formatos que admite el objeto de maestro de disco y, a continuación, seleccione el formato activo. Los formatos devueltos por el enumerador son los IID de las interfaces para [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) y [**IRedbookDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster).
4.  Recupere el enumerador de grabadora de CD mediante [**EnumDiscRecorders**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders). Enumerar la lista de grabadores de disco compatibles (específicos del formato activo) y, a continuación, seleccione la grabadora activa. La interfaz [**IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) representa un dispositivo físico.
5.  Use [**IDiscMaster::P rogressadvise**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) para registrar las devoluciones de llamada de progreso.
6.  Use la interfaz para el formato seleccionado para crear contenido. El contenido se compila de forma incremental, por lo que las pistas o el contenido de la carpeta se pueden agregar a un disco por pieza. La creación de este contenido se denomina *almacenamiento provisional de una imagen*. El contenido de la imagen almacenada provisionalmente no se puede eliminar de forma incremental (no se puede quitar una pista agregada), pero es posible borrar el contenido de una imagen almacenada provisionalmente para que se pueda volver a iniciar. Use [**IDiscMaster:: ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) para reiniciar el almacenamiento provisional.

**Para audio:  **

1.  Use [**IRedbookDiscMaster:: CreateAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) para indicar que se está iniciando una nueva pista de audio en el disco.
2.  Use [**IRedbookDiscMaster:: AddAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) para agregar datos de audio sin procesar a una pista. La aplicación puede usar [**GetAvailableAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks), [**GetTotalAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)y [**GetUsedAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) para recuperar información estadística.
3.  Use [**IRedbookDiscMaster:: CloseAudioTrack**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) para cerrar una pista de audio.
4.  Repita los pasos del 1-3 hasta quedarse sin espacio o se hayan escrito todas las pistas de audio.

**Para datos:  **

1.  Use [**IJolietDiscMaster:: AddData**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) para agregar el contenido de una carpeta a la imagen. Los elementos de una carpeta se colocan en la raíz del archivo de imagen. Use [**GetTotalDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) y [**GetUsedDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) para recuperar información estadística.
2.  Repita el paso anterior hasta que quede espacio insuficiente o se hayan agregado todos los datos.

**Para todos los discos:  **

1.  Use [**IDiscMaster:: RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) para grabar el disco.
2.  Cierre la sesión de IMAPi mediante [**IDiscMaster:: Close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close). Al cerrar la sesión, se borra el contenido del espacio provisional del disco.

 

 




