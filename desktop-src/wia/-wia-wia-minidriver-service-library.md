---
description: Para simplificar la implementación del controlador en la medida de lo posible, Windows Image Acquisition (WIA) proporciona una biblioteca de servicios de Minidriver que realiza muchas de las tareas administrativas que requiere la arquitectura de WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Biblioteca de servicios minidriver de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0008e19fbbdb31000535fa10f34bfacebfd6c6180964fa3e3fb18502f22a28d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207935"
---
# <a name="wia-minidriver-service-library"></a>Biblioteca de servicios minidriver de WIA

Para simplificar la implementación del controlador en la medida de lo posible, Windows Image Acquisition (WIA) proporciona una biblioteca de servicios de Minidriver que realiza muchas de las tareas administrativas que requiere la arquitectura de WIA. La biblioteca de servicios proporciona funciones auxiliares para mantener el árbol del dispositivo de [objetos IWiaDrvItem Interface.](https://msdn.microsoft.com/library/ms793976.aspx)

Las funciones básicas de la biblioteca de servicios realizan funciones auxiliares que, de lo contrario, la mayoría de los controladores de dispositivos tendrían que implementar. Estas funciones leen y escriben propiedades. También crean objetos de elemento de controlador y copian las propiedades de información del dispositivo.

 

 



