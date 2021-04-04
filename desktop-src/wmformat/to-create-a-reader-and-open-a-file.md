---
title: Para crear un lector y abrir un archivo
description: Para crear un lector y abrir un archivo
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- Advanced Systems Format (ASF), crear lectores
- ASF (formato de sistemas avanzados), creación de lectores
- Advanced Systems Format (ASF), abrir archivos
- ASF (formato de sistemas avanzados), abrir archivos
- lectores asincrónicos, crear
- lectores asincrónicos, abrir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8e714f51b56a7d9f3b18a774cd3b8c74bf05352
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789214"
---
# <a name="to-create-a-reader-and-open-a-file"></a>Para crear un lector y abrir un archivo

Para poder trabajar con el lector, debe crear un objeto de lector y cargar un archivo para leerlo. Para inicializar el lector y abrir un archivo, realice los pasos siguientes.

1.  Cree un objeto lector mediante una llamada a la función [**WMCreateReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) . Debe especificar el nivel deseado de Rights Management para el nuevo objeto de lector. Los modos disponibles se enumeran en el tipo de enumeración de [**\_ derechos WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights) .
2.  Especifique el archivo que se va a leer llamando a [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open). Debe especificar una interfaz de devolución de llamada de lector para que la use el lector. Para obtener más información sobre la devolución de llamada del lector, vea [para implementar mensajes de lector en la devolución de llamada de estado](to-implement-reader-messages-in-the-onstatus-callback.md).
3.  Espere a que el lector Abra el archivo. Cuando se llama a **Open** para cargar un archivo, devuelve casi inmediatamente y continúa el procesamiento en otro subproceso. Debe esperar a que se completen las operaciones, mediante la señalización de un evento cuando la devolución de llamada de **Estado** reciba el \_ mensaje de estado abierto de WMT.

El lector también admite el uso de la interfaz com **IStream** para abrir archivos. Puede implementar la interfaz **IStream** de la forma que elija. Después de abrir el archivo deseado en **IStream**, puede seguir los pasos indicados anteriormente, salvo que debe llamar a [**IWMReaderAdvanced2:: OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) en lugar de **IWMReader:: Open** en el paso 2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaz IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**Interfaz IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




