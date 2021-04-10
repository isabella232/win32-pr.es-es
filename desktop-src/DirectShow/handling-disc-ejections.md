---
description: Control de expulsaciones de disco
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Control de expulsaciones de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906308"
---
# <a name="handling-disc-ejections"></a>Control de expulsaciones de disco

Cuando el usuario expulsa un DVD de la unidad, el explorador de DVD envía a la aplicación un \_ mensaje de extracción de disco DVD de EC \_ \_ . La aplicación puede omitir este mensaje sin ningún riesgo y dejar que el navegador de DVD administre el estado del gráfico. Una aplicación también puede controlar el \_ \_ \_ método expulsado del disco DVD de EC para implementar el comportamiento personalizado cuando se expulsa un disco. Si controla el mensaje, debe establecer la \_ marca ResetOnStop de DVD en **true** con el método [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) y, a continuación, llamar a [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) antes de cerrar la aplicación o reproducir otro disco.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



