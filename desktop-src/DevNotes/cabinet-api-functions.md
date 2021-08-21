---
description: 'Más información sobre: Funciones de API de gabinete'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funciones de API de gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b08234a47c84a604c78275632d88be2bcdeef68e47fd092bbf50e4d97dcf925
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668359"
---
# <a name="cabinet-api-functions"></a>Funciones de API de gabinete

En esta sección se describen las siguientes funciones de La API de gabinete:

## <a name="fci-functions"></a>Funciones de FCI

La biblioteca FCI (Interfaz de compresión de archivos) proporciona la capacidad de crear gabinetes (también conocidos como "archivos CAB"). Además, la biblioteca proporciona compresión para reducir el tamaño de los datos de archivo almacenados en los gabinetes.



| Función                                   | Descripción                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Agrega un archivo al gabinete que se está contrucndo actualmente.<br/>                                           |
| [**FCICreate**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Crea un contexto de FCI.<br/>                                                                          |
| [**FCIDestroy**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Elimina un contexto de FCI abierto, liberando la memoria y los archivos temporales asociados al contexto.<br/> |
| [**FCIFlushCabinet**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Completa el gabinete actual.<br/>                                                                   |
| [**FCIFlushFolder**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Obliga a que la carpeta actual en construcción se complete inmediatamente.<br/>                        |



 

## <a name="fdi-functions"></a>Funciones de FDI

La biblioteca FDI (interfaz de descompresión de archivos) proporciona la capacidad de extraer archivos de los archivadores.



| Función                                         | Descripción                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**FDICopy**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Extrae archivos de los gabinetes.<br/>                                                          |
| [**FDICreate**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Crea un contexto de FDI.<br/>                                                                |
| [**FDIDestroy**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Elimina un contexto FDI abierto.<br/>                                                           |
| [**FDIIsCabinet**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Determina si un archivo es un archivador y, si es así, devuelve información descriptiva.<br/> |
| [**FDITruncateCabinet**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Trunca un archivo de archivador a partir del número de carpeta especificado.<br/>                      |



 

## <a name="deprecated-functions"></a>Funciones en desuso

-   [**DeleteExtractedFiles**](deleteextractedfiles.md)
-   [**DllGetVersion**](dllgetversion.md)
-   [**Extracto**](extract.md)
-   [**GetDllVersion**](getdllversion.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de La API de Archivador](cabinet-api-reference.md)
</dt> <dt>

[Uso de Cabinet API](using-the-cabinet-api.md)
</dt> </dl>

 

 




