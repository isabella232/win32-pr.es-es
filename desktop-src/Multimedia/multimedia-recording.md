---
title: Grabación multimedia
description: Grabación multimedia
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- MCIWndCreate función)
- MCIWndNew (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418669"
---
# <a name="multimedia-recording"></a>Grabación multimedia

Puede implementar capacidades de grabación en la aplicación mediante la interfaz de usuario integrada en MCIWnd. Puede usar la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) y la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) para proporcionar controles para iniciar y detener la grabación y para guardar la información registrada. Con **MCIWndCreate**, puede especificar estilos de ventana para mostrar una ventana de MCIWnd e incluir el botón **grabar** en la barra de herramientas. Con **MCIWndNew**, puede especificar el tipo de dispositivo que se va a grabar y especificar que la información se va a capturar en un archivo nuevo.

Si la aplicación requiere más sofisticación, puede automatizar y personalizar la grabación mediante la macro [**MCIWndRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) . Para obtener más información, vea [personalizar el proceso de grabación](customizing-the-recording-process.md).

> [!Note]  
> Algunos dispositivos, como el audio de CD y MCIAVI, se usan solo para la reproducción. Otros dispositivos, como los dispositivos de audio de forma de onda, se pueden usar para la grabación. Si especifica un dispositivo que no puede grabar, MCIWnd omite el botón **grabar** de la barra de herramientas.

 

 

 




