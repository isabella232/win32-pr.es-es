---
title: El mapa de mensajes
description: El mapa de mensajes
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Complementos de Media Player de Windows, mapa de mensajes
- complementos, mapa de mensajes
- Complementos de la interfaz de usuario, mapa de mensajes
- Complementos de la interfaz de usuario, mapa de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7fc04caf752383368ab6e51ae19c82e8c3515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075832"
---
# <a name="the-message-map"></a>El mapa de mensajes

La ventana del complemento responde a varios eventos llamando a métodos que se asignan a los mensajes de eventos correspondientes. El asistente proporciona una asignación para que se llame a OnPaint y OnEraseBackground en el momento adecuado. Para crear el botón **Buscar** y responder a los clics de este, la sección mapa de mensajes se modifica de la siguiente manera:


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

 

 




