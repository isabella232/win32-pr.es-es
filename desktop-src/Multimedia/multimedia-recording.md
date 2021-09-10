---
title: Grabación multimedia
description: Grabación multimedia
ms.assetid: e37aaac2-be89-4907-b1a8-f2c64ab2f39e
keywords:
- Función MCIWndCreate
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b1793ff7653e87a631ce1a4599345ec78f4015
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372422"
---
# <a name="multimedia-recording"></a>Grabación multimedia

Puede implementar funcionalidades de grabación en la aplicación mediante la interfaz de usuario integrada en MCIWnd. Puede usar la función [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) y la macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) para proporcionar controles para iniciar y detener la grabación y para guardar la información grabada. Con **MCIWndCreate**, puede especificar estilos de ventana para mostrar una ventana de MCIWnd e incluir el botón **Grabar** en la barra de herramientas. Con **MCIWndNew**, puede especificar el tipo de dispositivo que se va a grabar y especificar que la información se va a capturar en un nuevo archivo.

Si la aplicación requiere más sofisticación, puede automatizar y personalizar la grabación mediante la macro [**MCIWndRecord.**](/windows/desktop/api/Vfw/nf-vfw-mciwndrecord) Para obtener más información, vea [Personalización del proceso de grabación.](customizing-the-recording-process.md)

> [!Note]  
> Algunos dispositivos, como el audio de CD y MCIAVI, solo se usan para la reproducción. Otros dispositivos, como los dispositivos de audio de forma de onda, se pueden usar para la grabación. Si especifica un dispositivo que no puede grabar, MCIWnd omite el **botón Grabar** de la barra de herramientas.

 

 

 




