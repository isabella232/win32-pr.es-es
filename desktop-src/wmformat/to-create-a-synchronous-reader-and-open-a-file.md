---
title: Para crear un lector sincrónico y abrir un archivo
description: Para crear un lector sincrónico y abrir un archivo
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Formato de sistemas avanzados (ASF), creación de lectores
- ASF (formato de sistemas avanzados), creación de lectores
- Formato de sistemas avanzados (ASF), abrir archivos
- ASF (formato de sistemas avanzados), abrir archivos
- lectores sincrónicos, crear
- lectores sincrónicos, abrir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d1c6897c05bb0d843e5818f078df5235a5afac4a485d6a719ab86b8e4f8267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807655"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>Para crear un lector sincrónico y abrir un archivo

Para poder realizar cualquier trabajo con el lector sincrónico, deberá crear un objeto de lector sincrónico y cargar un archivo para leerlo. Para inicializar el lector sincrónico y abrir un archivo, realice los pasos siguientes.

1.  Cree un objeto de lector sincrónico llamando a [**la función WMCreateSyncReader.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) Debe especificar el nivel deseado de rights management para el nuevo objeto de lector. Los modos disponibles se muestran en el tipo **de enumeración WMT \_ RIGHTS.**
2.  Especifique un archivo para leer llamando a [**IWMSyncReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).

El lector sincrónico también admite el uso de la interfaz COM **de IStream** para abrir archivos. Puede implementar la **interfaz IStream** de la manera que elija. Después de abrir el archivo deseado en **IStream,** puede seguir los pasos indicados anteriormente, salvo que debe llamar a [**IWMSyncReader::OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) en lugar de **IWMSyncReader::Open** en el paso 2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMSyncReader (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lectura de archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




