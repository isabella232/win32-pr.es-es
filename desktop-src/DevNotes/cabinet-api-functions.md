---
description: 'Más información sobre: funciones de la API de archivos. cab'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funciones de la API de archivo. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907121"
---
# <a name="cabinet-api-functions"></a>Funciones de la API de archivo. cab

En esta sección se describen las siguientes funciones de la API de archivo. cab:

## <a name="fci-functions"></a>Características de FCI

La biblioteca FCI (interfaz de compresión de archivos) proporciona la capacidad de crear archivadores (también conocidos como "archivos. CAB"). Además, la biblioteca proporciona compresión para reducir el tamaño de los datos de archivo almacenados en los archivadores.



| Función                                   | Descripción                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**FCIAddFile**](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | Agrega un archivo al archivo. cab que se está construye.<br/>                                           |
| [**FCICreate**](/windows/desktop/api/Fci/nf-fci-fcicreate)             | Crea un contexto de FCI.<br/>                                                                          |
| [**FCIDestroy**](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | Elimina un contexto de FCI abierto, liberando la memoria y los archivos temporales asociados al contexto.<br/> |
| [**FCIFlushCabinet**](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | Completa el archivo. cab actual.<br/>                                                                   |
| [**FCIFlushFolder**](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | Fuerza la finalización inmediata de la carpeta actual en construcción.<br/>                        |



 

## <a name="fdi-functions"></a>Funciones FDI

La biblioteca FDI (interfaz de descompresión de archivos) proporciona la capacidad de extraer archivos de los archivadores.



| Función                                         | Descripción                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**FDICopy**](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | Extrae archivos de los archivadores.<br/>                                                          |
| [**FDICreate**](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | Crea un contexto FDI.<br/>                                                                |
| [**FDIDestroy**](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | Elimina un contexto FDI abierto.<br/>                                                           |
| [**FDIIsCabinet**](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | Determina si un archivo es un contenedor y, si es así, devuelve información descriptiva.<br/> |
| [**FDITruncateCabinet**](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | Trunca un archivo. cab a partir del número de carpeta especificado.<br/>                      |



 

## <a name="deprecated-functions"></a>Funciones en desuso

-   [**DeleteExtractedFiles**](deleteextractedfiles.md)
-   [**DllGetVersion**](dllgetversion.md)
-   [**Extracción**](extract.md)
-   [**GetDllVersion**](getdllversion.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de la API de contenedor](cabinet-api-reference.md)
</dt> <dt>

[Uso de la API de archivo. cab](using-the-cabinet-api.md)
</dt> </dl>

 

 




