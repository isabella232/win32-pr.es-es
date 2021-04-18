---
title: Para crear un lector sincrónico y abrir un archivo
description: Para crear un lector sincrónico y abrir un archivo
ms.assetid: 6349d05e-20db-4ce8-83fd-cad4cec666f2
keywords:
- Advanced Systems Format (ASF), crear lectores
- ASF (formato de sistemas avanzados), creación de lectores
- Advanced Systems Format (ASF), abrir archivos
- ASF (formato de sistemas avanzados), abrir archivos
- lectores sincrónicos, crear
- lectores sincrónicos, abrir archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e222c046a685885fa9e17baa52d0161176551ff3
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105704917"
---
# <a name="to-create-a-synchronous-reader-and-open-a-file"></a>Para crear un lector sincrónico y abrir un archivo

Antes de poder realizar cualquier trabajo con el lector sincrónico, debe crear un objeto de lector sincrónico y cargar un archivo para leerlo. Para inicializar el lector sincrónico y abrir un archivo, realice los pasos siguientes.

1.  Cree un objeto de lector sincrónico llamando a la función [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader) . Debe especificar el nivel deseado de Rights Management para el nuevo objeto de lector. Los modos disponibles se enumeran en el tipo de enumeración de **\_ derechos WMT** .
2.  Especifique el archivo que se va a leer llamando a [**IWMSyncReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-open).

El lector sincrónico también admite el uso de la interfaz com **IStream** para abrir archivos. Puede implementar la interfaz **IStream** de la forma que elija. Después de abrir el archivo deseado en **IStream**, puede seguir los pasos indicados anteriormente, salvo que debe llamar a [**IWMSyncReader:: OpenStream**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-openstream) en lugar de **IWMSyncReader:: Open** en el paso 2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Leer archivos con el lector sincrónico**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




