---
description: Las Windows image acquisition (WIA)APIs devuelven su estado de finalización en un valor devuelto HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Información de error de WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8181cb4d3f578fa9322ecaa81d588423bb403be3b38a76c2dbac17a19fe010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056965"
---
# <a name="wia-error-information"></a>Información de error de WIA

Las Windows image acquisition (WIA)APIs devuelven su estado de finalización en un valor devuelto HRESULT. Las aplicaciones comprueban estos valores devueltos con la constante WIA FACILITY para determinar si el error requiere la intervención del usuario para borrar, como una ruta de acceso de papel atorada, y notificarlos \_ al usuario. Además, todos los errores de nivel de controlador se registran en detalle en el registro de eventos, mediante cadenas de error proporcionadas por el minidriver del dispositivo. Para obtener una lista de códigos de error específicos de WIA, vea [Códigos de error](-wia-error-codes.md).

 

 



