---
description: Para simplificar la implementación del controlador lo máximo posible, la adquisición de imágenes de Windows (WIA) proporciona una biblioteca de servicio minicontrolador que realiza muchas de las tareas administrativas que requiere la arquitectura de WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Biblioteca de servicio minicontrolador de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696497"
---
# <a name="wia-minidriver-service-library"></a>Biblioteca de servicio minicontrolador de WIA

Para simplificar la implementación del controlador lo máximo posible, la adquisición de imágenes de Windows (WIA) proporciona una biblioteca de servicio minicontrolador que realiza muchas de las tareas administrativas que requiere la arquitectura de WIA. La biblioteca de servicios proporciona funciones auxiliares para mantener el árbol del dispositivo de objetos de [interfaz IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) .

Las funciones básicas de la biblioteca de servicios realizan funciones auxiliares que, de otro modo, necesitarían implementar. Estas funciones leen y escriben propiedades. También crean objetos de elementos de controlador y copian las propiedades de información del dispositivo.

 

 



