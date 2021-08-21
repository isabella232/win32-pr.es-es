---
description: Los módulos de salida personalizados deben implementar la interfaz ICertExit, a la que llama el motor del servidor.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Escribir módulos de salida personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d3a690d2ac8ae1d25607ca064e865b48f46fbc96afdb60b0ebcd54d3b1b15f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970682"
---
# <a name="writing-custom-exit-modules"></a>Escribir módulos de salida personalizados

Los módulos de salida personalizados deben implementar [**la interfaz ICertExit,**](/windows/desktop/api/Certexit/nn-certexit-icertexit) a la que llama el motor del servidor. El motor de servidor llama al método [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) cuando se carga el módulo de salida. Permite que el módulo de salida realice la inicialización y devuelve un valor que informa al motor del servidor de los tipos de eventos para los que desea recibir notificaciones. El [**método ICertExit::GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) debe devolver una cadena de descripción cuando el motor del servidor la solicite. El motor de servidor llama al método [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) para notificar al módulo de salida que se ha producido un evento.

Los módulos exit pueden llamar a la interfaz [**ICertServerExit,**](/windows/desktop/api/Certif/nn-certif-icertserverexit) que admite muchos de los mismos métodos que la interfaz [**ICertServerPolicy,**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) a excepción de los métodos [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) y [**SetCertificateProperty.**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)

Para obtener información sobre cómo quitar el módulo de salida existente e instalar uno nuevo, vea el tema Salir de personalización del módulo en la Ayuda.

 

 



