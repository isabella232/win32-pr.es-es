---
title: El mapa de mensajes
description: El mapa de mensajes
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Reproductor de Windows Media complementos,mapa de mensajes
- complementos, mapa de mensajes
- complementos de interfaz de usuario, mapa de mensajes
- Complementos de interfaz de usuario, mapa de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168609"
---
# <a name="the-message-map"></a>El mapa de mensajes

La ventana del complemento responde a varios eventos mediante una llamada a métodos asignados a los mensajes de evento correspondientes. El asistente proporciona una asignación para que se llame a OnPaint y OnEraseBackground en el momento adecuado. Para crear el **botón Buscar** y responder a los clics de él, la sección del mapa de mensajes se modifica de la siguiente manera:


```C++
BEGIN_MSG_MAP(CPluginWindow)
    MESSAGE_HANDLER(WM_PAINT, OnPaint)
    MESSAGE_HANDLER(WM_ERASEBKGND, OnEraseBackground)
    MESSAGE_HANDLER(WM_CREATE, OnCreate)
    COMMAND_ID_HANDLER(IDC_SEARCH, OnSearch)
END_MSG_MAP()

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Implementación de CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




