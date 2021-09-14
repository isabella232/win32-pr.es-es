---
description: Los servicios se suelen escribir como aplicaciones de consola.
ms.assetid: ed6945fc-ac08-4776-8d75-d33e8df3882a
title: Punto de entrada de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de9e2683c4a69949b6f51c7d000c0ee3571fe118
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168882"
---
# <a name="service-entry-point"></a>Punto de entrada de servicio

Los servicios se suelen escribir como aplicaciones de consola. El punto de entrada de una aplicación de consola es su **función** principal. La **función main** recibe argumentos del valor **ImagePath** de la clave del Registro para el servicio. Para obtener más información, vea la sección Comentarios de la [**función CreateService.**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)

Cuando el SCM inicia un programa de servicio, espera a que llame a la [**función StartServiceCtrlDispatcher.**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) Use las siguientes directrices.

-   Un servicio de tipo SERVICE WIN32 OWN PROCESS debe llamar inmediatamente a \_ \_ \_ [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) desde su subproceso principal. Puede realizar cualquier inicialización después de iniciar el servicio, como se describe en [Service ServiceMain Function](service-servicemain-function.md).
-   Si el tipo de servicio es SERVICE WIN32 SHARE PROCESS y hay una inicialización común para todos los servicios del programa, puede realizar la inicialización en el subproceso principal antes de llamar a \_ \_ \_ [**StartServiceCtrlDispatcher,**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)siempre que tarde menos de 30 segundos. De lo contrario, debe crear otro subproceso para realizar la inicialización común, mientras que el subproceso principal llama a **StartServiceCtrlDispatcher**. Debe realizar cualquier inicialización específica del servicio después de que se inicie el servicio.

La [**función StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) toma una [**estructura SERVICE TABLE \_ \_ ENTRY**](/windows/desktop/api/Winsvc/ns-winsvc-service_table_entrya) para cada servicio incluido en el proceso. Cada estructura especifica el nombre del servicio y el punto de entrada del servicio. Para obtener un ejemplo, vea [Escribir la función principal de un programa de servicio.](writing-a-service-program-s-main-function.md)

Si [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera) se realiza correctamente, el subproceso que realiza la llamada no se devuelve hasta que todos los servicios en ejecución del proceso han entrado en el estado SERVICE \_ STOPPED. El SCM envía solicitudes de control a este subproceso a través de una canalización con nombre. El subproceso actúa como distribuidor de controles, realizando las siguientes tareas:

-   Cree un subproceso para llamar al punto de entrada adecuado cuando se inicia un nuevo servicio.
-   Llame a la función [de controlador adecuada](service-control-handler-function.md) para controlar las solicitudes de control de servicio.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escribir la función principal de un programa de servicio](writing-a-service-program-s-main-function.md)
</dt> </dl>

 

 



