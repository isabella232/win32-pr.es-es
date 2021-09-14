---
title: Mostrar interfaces de usuario modales
description: Mostrar interfaces de usuario modales
ms.assetid: 748a8db7-159d-4043-beac-e0516327bcef
keywords:
- Reproductor de Windows Media complementos, mostrar cuadros de diálogo y mensajes
- complementos, mostrar cuadros de diálogo y mensajes
- complementos de interfaz de usuario, mostrar cuadros de diálogo y mensajes
- Complementos de interfaz de usuario, mostrar cuadros de diálogo y mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d96387ca46864064c7b6ff7b9cd3dba8187eed0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068448"
---
# <a name="displaying-modal-user-interfaces"></a>Mostrar interfaces de usuario modales

Los complementos de interfaz de usuario no deben mostrar cuadros de diálogo modales ni cuadros de mensaje en respuesta a las llamadas a métodos Reproductor de Windows Media. Por ejemplo, no muestre un cuadro de mensaje de la implementación de **IWMPPluginUI::Create**.

Si debe mostrar un cuadro de diálogo o un cuadro de mensaje desde una implementación de método de complemento de interfaz de usuario a la que llama el reproductor, debe seguir estos pasos:

1.  Registre un nuevo mensaje de ventana **mediante RegisterWindowMessage**.
2.  Envíe el mensaje de ventana que registró en la ventana del complemento de interfaz de usuario mediante **PostMessage**.
3.  Mostrar el cuadro de diálogo o el cuadro de mensaje del controlador de mensajes para el nuevo mensaje de ventana.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información general sobre el complemento de interfaz de usuario**](ui-plug-in-overview.md)
</dt> </dl>

 

 




