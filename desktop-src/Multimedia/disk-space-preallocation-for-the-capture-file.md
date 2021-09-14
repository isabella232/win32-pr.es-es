---
title: Asignación previa del espacio en disco para el archivo de captura
description: Asignación previa del espacio en disco para el archivo de captura
ms.assetid: 7a11b769-65b9-4eaa-bc42-5d1d744bf181
keywords:
- WM_CAP_FILE_ALLOCATE mensaje
- capFileAlloc (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7442b08170fb6f018555c043c59d96860701ed4f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069538"
---
# <a name="disk-space-preallocation-for-the-capture-file"></a>Asignación previa del espacio en disco para el archivo de captura

La preasignación del espacio en disco para el archivo de captura compila un archivo de un tamaño especificado en el disco antes del inicio de una operación de captura. La preasignación de un archivo de captura reduce el procesamiento necesario mientras la captura está en curso y da como resultado menos fotogramas descartados. Puede asignar previamente un archivo de captura mediante el mensaje [**WM \_ CAP FILE \_ \_ ALLOCATE**](wm-cap-file-allocate.md) (o la [**macro capFileAlloc).**](/windows/desktop/api/Vfw/nf-vfw-capfilealloc)

Normalmente, la aplicación debe preasignar suficiente espacio en disco para contener el archivo de captura más grande previsto. La preasignación del espacio en disco no restringe el tamaño del archivo capturado. El tamaño del archivo se amplía automáticamente si los datos capturados superan el espacio asignado. Las operaciones de escritura posteriores en el archivo de captura reutilizan las partes del espacio en disco asignado al archivo, conservando el tamaño y la fragmentación del archivo.

También puede mejorar el rendimiento de la captura desfragmentando el archivo de captura. Para desfragmentar el archivo, use una utilidad de desfragmentación como Desfragmentador de disco. Si usa un archivo de captura desfragmentado y posteriormente lo amplía, debe desfragmentar el archivo ampliado. La ampliación de un archivo de captura desfragmentado puede fragmentar la parte expandida del archivo y reducir el rendimiento en la operación de captura.

También puede mejorar el rendimiento mediante el uso de un disco sin comprimir para la captura de vídeo. La compresión de datos durante la captura puede limitar el rendimiento de la captura en el disco.

Una aplicación puede reservar un archivo de captura permanente para eliminar el tiempo necesario para preasignar y desfragmentar un archivo cada vez que se inicia. Dado que un archivo de captura puede requerir un espacio en disco considerable y la preasignación de un archivo de captura quita todos los datos de un archivo de captura existente, una aplicación debe permitir que el usuario decida si el archivo es permanente o temporal.

 

 




