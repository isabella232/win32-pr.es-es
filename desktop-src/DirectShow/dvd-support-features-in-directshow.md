---
description: Características de compatibilidad con DVD en DirectShow
ms.assetid: 20dc1067-696e-4f53-9c77-0f2da237c5af
title: Características de compatibilidad con DVD en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035af51bbe44ec8dcc95f199c502b71d37d834f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105677131"
---
# <a name="dvd-support-features-in-directshow"></a>Características de compatibilidad con DVD en DirectShow

La funcionalidad del filtro del [navegador de DVD](dvd-navigator-filter.md) se expone a través de dos interfaces, [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), que proporciona los métodos "SET" para el navegador de DVD y [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), que proporciona los métodos "Get".

El navegador de DVD admite las siguientes características:

-   Compatibilidad con Karaoke: puede escribir una aplicación de DVD-Karaoke mediante el navegador de DVD. (Esto requiere un descodificador compatible).
-   Acceso simplificado a cadenas de información de texto en DVD: el navegador de DVD analiza estas cadenas y permite a las aplicaciones enumerarlas, identificarlas y recuperarlas fácilmente.
-   Control de volumen de audio a través de [ **IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   Compatibilidad para personalizar el comportamiento del navegador de DVD cuando se emite el comando de detención: las aplicaciones pueden indicar al explorador de DVD que se reanude desde la ubicación actual cuando se reinicie el gráfico de filtro o comience a reproducir desde el principio del disco.
-   Compatibilidad con sistemas de cine digital (DTS) y audio de Sony Dynamic Digital Sound (SSD). El navegador de DVD reconoce las secuencias de audio DTS y SSD y se pasan al descodificador de audio. (Se requiere un descodificador compatible con DTS o compatible con SSD de terceros para descodificar y reproducir el audio).
-   Compatibilidad mejorada para los cambios de nivel parental: el navegador de DVD permite a una aplicación aceptar, rechazar u omitir comandos de cambio de nivel parental desde el disco.
-   Opciones avanzadas para administrar el estado del navegador de DVD y sincronizar comandos
-   Compatibilidad con la ejecución de fotogramas, la búsqueda con precisión de fotogramas y la reproducción inversa. Estas características requieren un descodificador de vídeo que las admita.
-   La capacidad de guardar la ubicación actual en un título y volver a ella en cualquier momento.
-   Compatibilidad simplificada para eventos de tiempo en títulos de PGC no secuenciales: en el caso de los títulos de PGC no secuenciales, el explorador de DVD retransmite la información de código de tiempo sin formato a la aplicación.
-   Información de código de tiempo. La estructura de código de [**\_ \_ tiempo HMSF de DVD**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) se puede usar en lugar del formato binario codificado decimal (BCD). **DVD \_ de El \_ código de tiempo HMSF** contiene los miembros a los que se tiene acceso fácilmente para horas, minutos, segundos y fotogramas, y se puede convertir a un **ULong**.
-   La capacidad de controlar si el gráfico de filtro se vacía después de una operación de búsqueda: los búferes del gráfico pueden contener hasta unos segundos de vídeo en un momento dado. Puede indicar al gráfico que termine de reproducir el vídeo almacenado en búfer después de una búsqueda o empezar a reproducir inmediatamente en la nueva ubicación.
-   La capacidad de establecer valores en registros de parámetros generales: una característica avanzada para los usuarios familiarizados con la especificación de DVD que desean implementar la funcionalidad avanzada.
-   La capacidad de generar identificadores de disco numéricos que tengan un único propósito práctico

### <a name="what-background-do-i-need-to-write-a-dvd-application"></a>¿Qué información general necesito para escribir una aplicación de DVD?

Todos los desarrolladores de aplicaciones deben estar familiarizados con las características proporcionadas por la tecnología de DVD, como los niveles de administración parental, varios flujos de audio y subimágenes, y los bloques de ángulo. [Conceptos básicos de DVD](dvd-basics.md) describe brevemente cada una de estas características; hay disponibles descripciones más completas en publicaciones de terceros. No es necesario hacer referencia a la especificación de DVD a menos que pretenda implementar características avanzadas más allá del conjunto de comandos J del anexo.

Los desarrolladores de C/C++ que utilizan DirectShow deben estar familiarizados con las técnicas de programación de cliente COM, como la creación de objetos COM y la obtención y liberación de punteros de interfaz COM. También podría necesitar un conocimiento general de las operaciones de gráficos de filtro, porque puede que necesite tener acceso y manipular el gráfico directamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



