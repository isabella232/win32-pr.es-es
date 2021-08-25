---
title: Acerca de los complementos de conversión
description: Acerca de los complementos de conversión
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Reproductor de Windows Media complementos de conversión
- Reproductor de Windows Media complementos,conversión
- complementos, conversión
- complementos de conversión, acerca de
- Formato ASF
- ASF (formato de sistemas avanzados)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4331f2cc0cdf8726e2ba26e834c56546ee614e012a9dd6acdad56906d450b66e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903557"
---
# <a name="about-conversion-plug-ins"></a>Acerca de los complementos de conversión

Puede crear un complemento Reproductor de Windows Media para convertir los archivos multimedia digitales creados mediante tecnologías no proporcionadas por Microsoft, en formato de sistemas avanzados (ASF).

Los complementos de conversión son objetos del Modelo de objetos componentes (COM) que se empaquetan y distribuyen como archivos ejecutables (.exe). Reproductor de Windows Media crea instancias de complementos de conversión para convertir formatos de medios digitales de terceros en los escenarios siguientes:

-   El contenido multimedia digital se copia en el equipo desde un dispositivo portátil.
-   El contenido multimedia digital se agrega a la biblioteca mediante **IWMPMediaCollection::add**.
-   El contenido multimedia digital se agrega a la biblioteca mediante la característica de búsqueda de Reproductor de Windows Media.
-   El contenido multimedia digital se agrega a la biblioteca mediante la característica de supervisión de carpetas de Reproductor de Windows Media.
-   El contenido multimedia digital se agrega a la lista de sincronización cuando el usuario arrastra y coloca un archivo.

Después Reproductor de Windows Media crear una instancia de un complemento de conversión, el complemento debe convertir el archivo proporcionado en ASF o WMA y agregar los metadatos pertinentes. (No use el complemento de conversión para transcodificar el archivo). A continuación, el complemento debe copiar el archivo convertido en la carpeta especificada y devolver la ruta de acceso al nuevo archivo para Reproductor de Windows Media.

Los complementos de conversión deben implementar la **interfaz IWMPConvert.** Vea [Referencia de programación de complementos de conversión.](conversion-plug-ins-programming-reference.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Acerca del proceso de conversión**](about-the-conversion-process.md)
</dt> <dt>

[**Agregar metadatos a archivos convertidos**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Reproductor de Windows Media Complementos de conversión**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




