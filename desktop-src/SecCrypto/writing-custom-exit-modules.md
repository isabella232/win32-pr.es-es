---
description: Los módulos de salida personalizados deben implementar la interfaz ICertExit, a la que llama el motor del servidor.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Escribir módulos de salida personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476349"
---
# <a name="writing-custom-exit-modules"></a>Escribir módulos de salida personalizados

Los módulos de salida personalizados deben implementar [**la interfaz ICertExit,**](/windows/desktop/api/Certexit/nn-certexit-icertexit) a la que llama el motor del servidor. El motor de servidor llama al método [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) cuando se carga el módulo de salida. Permite que el módulo de salida realice la inicialización y devuelve un valor que informa al motor del servidor de los tipos de eventos para los que desea recibir notificaciones. El [**método ICertExit::GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) debe devolver una cadena de descripción cuando el motor del servidor la solicite. El motor de servidor llama al método [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) para notificar al módulo de salida que se ha producido un evento.

Los módulos exit pueden llamar a la interfaz [**ICertServerExit,**](/windows/desktop/api/Certif/nn-certif-icertserverexit) que admite muchos de los mismos métodos que la interfaz [**ICertServerPolicy,**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) a excepción de los métodos [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) y [**SetCertificateProperty.**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)

Para obtener información sobre cómo quitar el módulo de salida existente e instalar uno nuevo, vea el tema Salir de personalización del módulo en la Ayuda.

 

 



