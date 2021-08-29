---
title: Para crear un lector y abrir un archivo
description: Para crear un lector y abrir un archivo
ms.assetid: 82b194d6-7cb7-4b88-9ed7-944b8b43bc29
keywords:
- Formato de sistemas avanzados (ASF), creación de lectores
- ASF (formato de sistemas avanzados), creación de lectores
- Formato de sistemas avanzados (ASF), abrir archivos
- ASF (formato de sistemas avanzados), abrir archivos
- lectores asincrónicos, crear
- lectores asincrónicos, abrir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc9dad56efa9556618a71bdd6c18500c43545085bdadaf4c6465fc3bf2e3aab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807645"
---
# <a name="to-create-a-reader-and-open-a-file"></a>Para crear un lector y abrir un archivo

Para poder realizar cualquier trabajo con el lector, deberá crear un objeto de lector y cargar un archivo para leerlo. Para inicializar el lector y abrir un archivo, realice los pasos siguientes.

1.  Cree un objeto de lector mediante una llamada a [**la función WMCreateReader.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatereader) Debe especificar el nivel deseado de rights management para el nuevo objeto de lector. Los modos disponibles se muestran en el tipo [**de enumeración WMT \_ RIGHTS.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_rights)
2.  Especifique un archivo para leer llamando a [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open). Debe especificar una interfaz de devolución de llamada de lector para que la use el lector. Para obtener más información sobre la devolución de llamada del lector, vea [Para implementar mensajes de lector en la devolución de llamada OnStatus](to-implement-reader-messages-in-the-onstatus-callback.md).
3.  Espere a que el lector abra el archivo. Cuando se llama **a Open** para cargar un archivo, se devuelve casi inmediatamente y continúa el procesamiento en otro subproceso. Debe esperar a que se completen las operaciones mediante la señalización de un evento cuando la devolución de llamada **OnStatus** recibe el mensaje de estado WMT \_ OPENED.

El lector también admite el uso de la interfaz COM **de IStream** para abrir archivos. Puede implementar la **interfaz IStream** de la manera que elija. Después de abrir el archivo deseado en **IStream,** puede seguir los pasos indicados anteriormente, salvo que debe llamar a [**IWMReaderAdvanced2::OpenStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-openstream) en lugar de **IWMReader::Open** en el paso 2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMReader (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**IWMReaderAdvanced2 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[**IWMStatusCallback (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback)
</dt> <dt>

[**Leer archivos con el lector asincrónico**](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[**Usar los métodos de devolución de llamada**](using-the-callback-methods.md)
</dt> </dl>

 

 




