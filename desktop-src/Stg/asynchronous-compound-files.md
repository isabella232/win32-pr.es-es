---
title: Archivos compuestos asincrónicos
description: Los archivos compuestos asincrónicos, la implementación proporcionada por el sistema del almacenamiento asincrónico, permiten la descarga eficaz de archivos compuestos de Internet en general y de la Web en particular.
ms.assetid: 6cad074e-07a8-434f-a402-e29cb66a1a18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04de2162b50283b12bc8deed6ec908d92e7584d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068924"
---
# <a name="asynchronous-compound-files"></a>Archivos compuestos asincrónicos

Los archivos compuestos asincrónicos, la implementación proporcionada por el sistema del almacenamiento asincrónico, permiten la descarga eficaz de archivos compuestos de Internet en general y de la Web en particular. La arquitectura básica de los archivos compuestos asincrónicos se muestra en el diagrama siguiente.

![arquitectura básica de archivos compuestos asincrónicos](images/asy-stor.png)

La implementación de archivos compuestos asincrónicos puede funcionar con nuevos tipos de moniker asincrónicos que comprenden los protocolos de Internet y pueden enlazarse a un objeto identificado por una dirección URL. Este moniker devolvería un puntero [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) o [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) asincrónico desde la llamada del cliente a [**IMoniker::BindToStorage**](/windows/win32/api/objidl/nf-objidl-imoniker-bindtostorage).

Los archivos compuestos en general se implementan sobre un objeto de matriz de bytes, una abstracción de un archivo que representa los datos de un objeto como una matriz de bytes planos. El objeto de matriz de bytes expone su funcionalidad a través de [**la interfaz ILockBytes.**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Si una matriz de bytes admite el almacenamiento asincrónico sin bloqueo, devuelve E PENDING a la implementación de archivo compuesto, que a su vez propaga el error al \_ autor de la llamada.

Para realizar un seguimiento de los datos disponibles durante una descarga, una matriz de bytes que admite el almacenamiento asincrónico expone la interfaz [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) en un objeto contenedor proporcionado por el sistema específicamente para este propósito. El código de descarga proporcionado por un moniker asincrónico llama a esta interfaz para rellenar la matriz de bytes de forma asincrónica, ya que los datos están disponibles. El objeto contenedor también expone una interfaz **ILockBytes,** que la implementación de archivos compuestos asincrónicos usa para leer y escribir datos desde y en la matriz.

Los objetos de flujo y almacenamiento asincrónico proporcionan un punto de conexión para la interfaz [**IProgressNotify,**](/windows/win32/api/objidl/nn-objidl-iprogressnotify) que se implementa mediante el código de descarga del moniker asincrónico. La implementación de archivos compuestos asincrónicos llama a **IProgressNotify** para proporcionar al descargador información sobre el estado de la operación de descarga.

 

 