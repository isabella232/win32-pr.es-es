---
description: Características de compatibilidad de DVD en DirectShow
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: Características de compatibilidad de DVD en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f143bab35a8b9a4a0cb12af20c2c2c3b66a0822a24cfc054b1f5d30bd4bc3dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107905"
---
# <a name="dvd-support-features-in-directshow"></a>Características de compatibilidad de DVD en DirectShow

La funcionalidad del filtro [DVD Navigator](dvd-navigator-filter.md) se expone a través de dos interfaces, [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), que proporciona los métodos "set" para DVD Navigator e [**IDvdInfo2,**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)que proporciona los métodos "get".

DVD Navigator admite las siguientes características:

-   Compatibilidad con Dvd: puede escribir una aplicación DVD-dvd mediante DVD Navigator. (Esto requiere un descodificador compatible).
-   Acceso simplificado a las cadenas de información de texto de DVD: el navegador de DVD analiza estas cadenas y permite que las aplicaciones las enumeren, identifiquen y recuperen fácilmente.
-   Control de volumen de audio a [ **través de IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   Compatibilidad para personalizar el comportamiento del navegador de DVD cuando se emite el comando Detener: las aplicaciones pueden indicar al navegador de DVD que se reanude desde la ubicación actual al reiniciar el gráfico de filtros o que inicie la reproducción desde el principio del disco.
-   Compatibilidad con audio de Digital Sound Systems (DTS) y Sonido digital dinámico de Sonar (SDDS). El navegador de DVD reconoce las secuencias de audio DTS y SDDS y se pasan al descodificador de audio. (Se requiere un descodificador compatible con DTS o SDDS de terceros para descodificar y reproducir el audio).
-   Compatibilidad mejorada con los cambios de nivel parental: el navegador de DVD permite que una aplicación acepte, rechace o ignore los comandos de cambio de nivel parental del disco.
-   Opciones avanzadas para administrar el estado del navegador de DVD y sincronizar comandos
-   Compatibilidad con la ejecución paso a paso de fotogramas, la búsqueda precisa de fotogramas y el juego inverso. Estas características requieren un descodificador de vídeo que las admita.
-   La capacidad de guardar la ubicación actual en un título y volver a ella en cualquier momento.
-   Compatibilidad simplificada con eventos de hora en títulos PGC no secuenciales: en el caso de los títulos PGC no secuenciales, el navegador de DVD retransmite la información de código de tiempo sin procesar a la aplicación.
-   Información de código de hora. La [**estructura \_ \_ TIMECODE de HMSF**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) de DVD se puede usar en lugar del formato decimal codificado binario (BCD). **DVD \_ HMSF \_ TIMECODE** contiene miembros a los que se accede fácilmente durante horas, minutos, segundos y fotogramas, y se puede convertir a o desde un **ULONG.**
-   La capacidad de controlar si el gráfico de filtro se vacía después de una operación de búsqueda: los búferes de grafo pueden contener hasta unos segundos de vídeo en un momento dado. Puede indicar al gráfico que termine de reproducir el vídeo almacenado en búfer después de una búsqueda o comience a reproducirse inmediatamente en la nueva ubicación.
-   La capacidad de establecer valores en registros de parámetros generales: una característica avanzada para aquellos que están familiarizados con la especificación de DVD que desean implementar funcionalidad avanzada.
-   La capacidad de generar identificadores numéricos de disco que son únicos para todos los propósitos prácticos

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>¿Qué fondo necesito para escribir una aplicación de DVD?

Todos los desarrolladores de aplicaciones deben estar familiarizados con las características proporcionadas por la tecnología de DVD, como los niveles de administración parental, varios flujos de audio y subpicture y bloques angulares. [Los conceptos básicos de DVD](dvd-basics.md) describen brevemente cada una de estas características. hay descripciones más completas disponibles en publicaciones de terceros. No es necesario hacer referencia a la especificación de DVD a menos que tenga previsto implementar características avanzadas más allá del conjunto de comandos del anexo J.

Los desarrolladores de C/C++ que usan DirectShow deben estar familiarizados con técnicas de programación de cliente COM, como la creación de objetos COM y la obtención y liberación de punteros de interfaz COM. Es posible que también necesite un conocimiento general de las operaciones de gráfico de filtro, ya que es posible que tenga que acceder al gráfico y manipularlo directamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



