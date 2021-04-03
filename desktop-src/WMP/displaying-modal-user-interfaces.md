---
title: Mostrar interfaces de usuario modales
description: Mostrar interfaces de usuario modales
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Complementos de Windows Media Player, Mostrar cuadros de diálogo y cuadros de mensaje
- complementos, Mostrar cuadros de diálogo y cuadros de mensaje
- Complementos de la interfaz de usuario, Mostrar cuadros de diálogo y de mensajes
- Complementos de la interfaz de usuario, Mostrar cuadros de diálogo y de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780064"
---
# <a name="displaying-modal-user-interfaces"></a>Mostrar interfaces de usuario modales

Los complementos de interfaz de usuario no deben mostrar cuadros de diálogo modales ni cuadros de mensaje en respuesta a llamadas a métodos desde Media Player de Windows. Por ejemplo, no muestre un cuadro de mensaje de la implementación de **IWMPPluginUI:: Create**.

Si debe mostrar un cuadro de diálogo o un cuadro de mensaje desde una implementación del método de complemento de la interfaz de usuario a la que llama el reproductor, debe seguir estos pasos:

1.  Registra un nuevo mensaje de ventana mediante **RegisterWindowMessage**.
2.  Envíe el mensaje de ventana que registró a la ventana del complemento de la interfaz de usuario mediante **PostMessage**.
3.  Mostrar el cuadro de diálogo o el cuadro de mensaje del controlador de mensajes para el nuevo mensaje de ventana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general del complemento de la interfaz de usuario**](ui-plug-in-overview.md)
</dt> </dl>

 

 




