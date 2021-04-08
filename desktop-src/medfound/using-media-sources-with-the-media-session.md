---
description: Uso de orígenes multimedia con la sesión multimedia
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Uso de orígenes multimedia con la sesión multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104003352"
---
# <a name="using-media-sources-with-the-media-session"></a>Uso de orígenes multimedia con la sesión multimedia

Si está utilizando la sesión multimedia para controlar la reproducción, se restringe el conjunto de métodos que debe llamar en un origen multimedia. En esta sección se describe cómo usar el origen de medios junto con la sesión multimedia.

Estos son los pasos básicos que realizará la aplicación:

1.  Cree el origen de medios. Para crear un origen multimedia, use la resolución de origen. Para obtener más información, consulte [solucionador de código fuente](source-resolver.md). La resolución de origen devuelve un puntero a la interfaz [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) del origen. (Si ha escrito un origen multimedia personalizado, puede proporcionar un método de creación personalizado en su lugar).

2.  Configure la presentación. Para configurar la presentación del origen, llame a [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Puede modificar esta copia, pero los cambios no se activan hasta que se inicia la reproducción. No modifique el descriptor de presentación durante la reproducción. Para obtener más información, vea [descriptores de presentación](presentation-descriptors.md).

3.  Cree una topología que contenga el origen de medios. Para obtener más información, vea [topologías](topologies.md).

4.  Utilice la sesión multimedia para controlar la reproducción. La sesión multimedia llama a métodos en el origen de medios. En este momento, la aplicación no debe llamar a ningún método en el origen de medios.

5.  Antes de liberar el origen multimedia, llame a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para cerrar el origen.

    > [!Note]  
    > Si usa el origen del secuenciador, el origen del secuenciador controla el cierre de los orígenes del segmento. Para obtener más información, vea [Sequencer Source](sequencer-source.md).

     

Si usa la sesión multimedia, los únicos métodos que debe llamar en el origen del medio son [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor), [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)y [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). En concreto:

-   No llamar a [**iniciar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**pausar**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)o [**detener**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); solo la sesión multimedia debe llamar a estos métodos.

-   No llame a ningún método [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) .

-   No recupere eventos directamente desde el origen de medios ni desde ninguna de las secuencias. La sesión multimedia debe recibir estos eventos para que la canalización funcione correctamente. La sesión multimedia reenvía los eventos necesarios para la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión de medios](media-session.md)
</dt> </dl>

 

 



