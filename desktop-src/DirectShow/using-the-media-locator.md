---
description: Uso del localizador de medios
ms.assetid: 07840a37-7065-41e8-aee5-855c9f89fb77
title: Uso del localizador de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fce934b06d92c0bec66d9260a485516d3acaf5a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891580"
---
# <a name="using-the-media-locator"></a>Uso del localizador de medios

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

El localizador de medios es un objeto auxiliar que comprueba los nombres de archivo y busca los archivos que faltan en directorios locales o de red. El detector de medios mantiene una caché de rutas de acceso de directorio donde ha encontrado correctamente archivos en búsquedas anteriores. Para buscar un archivo, busca en los directorios de su memoria caché. Si no lo hace, el detector de medios puede mostrar un cuadro de diálogo Abrir archivo para que el usuario localice un archivo manualmente. Suponiendo que el usuario localiza el archivo, el localizador de medios agrega el nuevo directorio a su memoria caché. El localizador de medios expone la [**interfaz IMediaLocator.**](imedialocator.md)

Normalmente, la aplicación no crea directamente una instancia del localizador de medios. En su lugar, la escala de tiempo y el motor de representación proporcionan los métodos siguientes para validar los nombres de archivo mediante el detector de medios.

-   Para validar los nombres de archivo en la escala de tiempo, llame [**a IAMTimeline::ValidateSourceNames**](iamtimeline-validatesourcenames.md). Opcionalmente, este método también actualiza los objetos de origen con los nombres de archivo correctos.
-   Para validar los nombres de archivo cuando se representa el proyecto, llame a [**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md).

Ambos métodos toman marcas que controlan el comportamiento del localizador de medios. Por ejemplo, puede restringir la búsqueda a directorios locales.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con orígenes](working-with-sources.md)
</dt> </dl>

 

 



