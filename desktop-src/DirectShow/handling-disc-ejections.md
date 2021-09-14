---
description: Control de las eyección de disco
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Control de las eyección de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127169954"
---
# <a name="handling-disc-ejections"></a>Control de las eyección de disco

Cuando el usuario expulsa un DVD de la unidad, el navegador de DVD envía a la aplicación un mensaje EC \_ DVD \_ DISC \_ EYEED. La aplicación puede omitir este mensaje de forma segura y permitir que el navegador de DVD administre el estado del grafo. Una aplicación también puede controlar el método EC DVD DISC EYEED para implementar \_ un comportamiento personalizado cuando se \_ \_ expulsa un disco. Si controla el mensaje, debe establecer la marca RESETOnStop de DVD en TRUE con el método SetOption y, a continuación, llamar a \_ [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop)  antes de cerrar la aplicación o reproducir otro disco. [](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aplicaciones de DVD](dvd-applications.md)
</dt> </dl>

 

 



