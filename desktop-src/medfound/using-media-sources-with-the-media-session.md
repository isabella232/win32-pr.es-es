---
description: Uso de orígenes multimedia con la sesión multimedia
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Uso de orígenes multimedia con la sesión multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268623"
---
# <a name="using-media-sources-with-the-media-session"></a>Uso de orígenes multimedia con la sesión multimedia

Si usa la sesión multimedia para controlar la reproducción, el conjunto de métodos a los que debe llamar en un origen multimedia está restringido. En esta sección se describe cómo usar el origen de medios junto con la sesión multimedia.

Estos son los pasos básicos que realizará la aplicación:

1.  Cree el origen multimedia. Para crear un origen multimedia, use la resolución de origen. Para obtener más información, vea [Solucionador de origen.](source-resolver.md) El solucionador de origen devuelve un puntero a la interfaz [**DEFUSMediaSource del**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) origen. (Si ha escrito un origen multimedia personalizado, puede proporcionar un método de creación personalizado en su lugar).

2.  Configure la presentación. Para configurar la presentación del origen, llame [**a IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Puede modificar esta copia, pero los cambios no se activarán hasta que se inicie la reproducción. No modifique el descriptor de presentación durante la reproducción. Para obtener más información, vea [Descriptores de presentación](presentation-descriptors.md).

3.  Cree una topología que contenga el origen multimedia. Para obtener más información, vea [Topologías](topologies.md).

4.  Use la sesión multimedia para controlar la reproducción. La sesión multimedia llama a métodos en el origen de medios. La aplicación no debe llamar a ningún método en el origen multimedia en este momento.

5.  Antes de liberar el origen de medios, llame [**a IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) para apagar el origen.

    > [!Note]  
    > Si usa el origen del secuenciador, el origen del secuenciador controla el apagado de los orígenes del segmento. Para obtener más información, vea [Sequencer Source](sequencer-source.md).

     

Si usa la sesión multimedia, los únicos métodos a los que debe llamar en el origen de medios son [**CreatePresentationDescriptor,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)y [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). En concreto:

-   No llame a [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start), [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)o [**Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop); La sesión multimedia solo debe llamar a estos métodos.

-   No llame a ningún [**método DENSMEDIASTREAM.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

-   No recupere eventos directamente del origen multimedia ni de ninguna de las secuencias. La sesión multimedia debe recibir estos eventos para que la canalización funcione correctamente. La sesión multimedia reenvía los eventos necesarios para la aplicación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Sesión multimedia](media-session.md)
</dt> </dl>

 

 



