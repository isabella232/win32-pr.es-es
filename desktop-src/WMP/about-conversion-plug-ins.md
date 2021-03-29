---
title: Acerca de los complementos de conversión
description: Acerca de los complementos de conversión
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player, Complementos de conversión
- Complementos de Windows Media Player, conversión
- complementos, conversión
- Complementos de conversión, acerca de
- Formato ASF
- ASF (formato de sistemas avanzados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773590"
---
# <a name="about-conversion-plug-ins"></a>Acerca de los complementos de conversión

Puede crear un complemento de Media Player de Windows para convertir archivos multimedia digitales creados con tecnologías no proporcionadas por Microsoft, en formato de sistema avanzado (ASF).

Los complementos de conversión son objetos del modelo de objetos componentes (COM) que se empaquetan y distribuyen como archivos ejecutables (. exe). Windows Media Player crea una instancia de los complementos de conversión para convertir formatos de medios digitales de terceros en los escenarios siguientes:

-   El contenido multimedia digital se copia en el equipo desde un dispositivo portátil.
-   El contenido multimedia digital se agrega a la biblioteca mediante **IWMPMediaCollection:: Add**.
-   El contenido multimedia digital se agrega a la biblioteca mediante la característica de búsqueda de Windows Media Player.
-   La característica de supervisión de carpetas de Windows Media Player agrega el contenido multimedia digital a la biblioteca.
-   El contenido multimedia digital se agrega a la lista de sincronización cuando el usuario arrastra y coloca un archivo.

Después de que Windows Media Player crea una instancia de un complemento de conversión, el complemento debe convertir el archivo proporcionado en ASF o WMA y agregar los metadatos pertinentes. (No use el complemento de conversión para transcodificar el archivo). A continuación, el complemento debe copiar el archivo convertido en la carpeta especificada y devolver la ruta de acceso al nuevo archivo a Windows Media Player.

Los complementos de conversión deben implementar la interfaz **IWMPConvert** . Consulte [referencia de programación de complementos de conversión](conversion-plug-ins-programming-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del proceso de conversión**](about-the-conversion-process.md)
</dt> <dt>

[**Agregar metadatos a archivos convertidos**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Complementos de conversión de Windows Media Player**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




