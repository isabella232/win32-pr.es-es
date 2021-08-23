---
title: Interacción con IMAPI
description: En los pasos siguientes se describe una interacción típica entre una aplicación e IMAPI.
ms.assetid: e57a86c4-7e27-40cf-a9c1-081b3f20d9d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab97d1a9d76d1e82dab64fb777ef5207d3d47560b2a889981c698ab78e3622b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726995"
---
# <a name="interacting-with-imapi"></a>Interacción con IMAPI

En los pasos siguientes se describe una interacción típica entre una aplicación e IMAPI.

1.  Cree una instancia de **MSDiscMasterObj** (mediante **CoCreateInstance**, punteros inteligentes desde una importación, y así sucesivamente) y solicite la [**interfaz IDiscMaster.**](/windows/desktop/api/Imapi/nn-imapi-idiscmaster)
2.  Adquiera acceso a IMAPI mediante una [**llamada a IDiscMaster::Open**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-open). Si esta llamada se realiza correctamente, la aplicación tiene acceso total a todas las interfaces y métodos implementados en **MSDiscMasterObj**.
3.  Recupere el enumerador de formato maestro de disco [**mediante EnumDiscMasterFormats**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscmasterformats). Enumere el conjunto de formatos que admite el objeto maestro de disco y, a continuación, seleccione el formato activo. Los formatos devueltos por el enumerador son los IID de las interfaces para [**IJolietDiscMaster**](/windows/desktop/api/Imapi/nn-imapi-ijolietdiscmaster) e [**IRedbookDiscMaster.**](/windows/desktop/api/Imapi/nn-imapi-iredbookdiscmaster)
4.  Recupere el enumerador de la grabadora de discos [**mediante EnumDiscRecorders**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-enumdiscrecorders). Enumere la lista de grabadoras de discos compatibles (específicas del formato activo) y, a continuación, seleccione la grabadora activa. La [**interfaz IDiscRecorder**](/windows/desktop/api/Imapi/nn-imapi-idiscrecorder) representa un dispositivo físico.
5.  Use [**IDiscMaster::P rogressAdvise para**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-progressadvise) registrarse para las devoluciones de llamada de progreso.
6.  Use la interfaz para el formato seleccionado para compilar contenido. El contenido se compila de forma incremental, por lo que las pistas o el contenido de la carpeta se pueden agregar a un disco por pieza. La creación de este contenido se denomina *almacenamiento provisional de una imagen.* El contenido de la imagen de almacenamiento provisional no se puede eliminar incrementalmente (no se puede quitar una pista que se ha agregado), pero es posible borrar el contenido de una imagen por fases para que el almacenamiento provisional pueda iniciarse de nuevo. Use [**IDiscMaster::ClearFormatContent para**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) reiniciar el almacenamiento provisional.

**Para audio: **

1.  Use [**IRedbookDiscMaster::CreateAudioTrack para**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-createaudiotrack) indicar que se está iniciando una nueva pista de audio en el disco.
2.  Use [**IRedbookDiscMaster::AddAudioTrackBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-addaudiotrackblocks) para agregar datos de audio sin procesar a una pista. La aplicación puede usar [**GetAvailableAudioTrackBlocks,**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getavailableaudiotrackblocks) [**GetTotalAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-gettotalaudioblocks)y [**GetUsedAudioBlocks**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-getusedaudioblocks) para recuperar información estadística.
3.  Use [**IRedbookDiscMaster::CloseAudioTrack para**](/windows/desktop/api/Imapi/nf-imapi-iredbookdiscmaster-closeaudiotrack) cerrar una pista de audio.
4.  Repita los pasos del 1 al 3 hasta que no haya espacio suficiente o se hayan escrito todas las pistas de audio.

**Para datos: **

1.  Use [**IJolietDiscMaster::AddData**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-adddata) para agregar el contenido de una carpeta a la imagen. Los elementos de una carpeta se colocan en la raíz del archivo de imagen. Use [**GetTotalDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-gettotaldatablocks) y [**GetUsedDataBlocks**](/windows/desktop/api/Imapi/nf-imapi-ijolietdiscmaster-getuseddatablocks) para recuperar información estadística.
2.  Repita el paso anterior hasta que se haya quedado sin espacio o se hayan agregado todos los datos.

**Para todos los discos: **

1.  Use [**IDiscMaster::RecordDisc para**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) grabar el disco.
2.  Cierre la sesión IMAPI mediante [**IDiscMaster::Close**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-close). Al cerrar la sesión, se borra el contenido del stash del disco.

 

 




