---
title: Mapa de mensajes
description: Mapa de mensajes
ms.assetid: 4640b0f5-625e-4a9e-86f5-3e75d0afb40d
keywords:
- Reproductor de Windows Media complementos,mapa de mensajes
- complementos, mapa de mensajes
- complementos de interfaz de usuario, mapa de mensajes
- Complementos de interfaz de usuario, mapa de mensajes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ec00689257ee60ada8f9bdf027b1cd34e43d243492e8d8ce5b5b38d2d89044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831578"
---
# <a name="the-message-map"></a>Mapa de mensajes

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

 

 




