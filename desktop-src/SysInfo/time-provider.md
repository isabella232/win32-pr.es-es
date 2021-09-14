---
description: El sistema operativo Windows microsoft proporciona compatibilidad con diversos dispositivos de hardware y protocolos de hora de red mediante la arquitectura del proveedor de hora.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243884"
---
# <a name="time-provider"></a>Proveedor de hora

El sistema operativo Windows microsoft proporciona compatibilidad con diversos dispositivos de hardware y protocolos de hora de red mediante la *arquitectura del proveedor de* hora. Los proveedores de hora de entrada recuperan marcas de tiempo precisas del hardware o la red, y los proveedores de hora de salida proporcionan marcas de tiempo a otros clientes de la red.

El administrador de proveedores de hora administra los proveedores *de hora.* Es responsable de cargar, iniciar y detener proveedores de hora según lo indicado por el administrador de control de servicios. Esta interfaz facilita la escritura de un proveedor de hora que la escritura de un servicio completo.

-   [Creación de un proveedor de hora](creating-a-time-provider.md)
-   [Registro de un proveedor de hora](registering-a-time-provider.md)
-   [Proveedor de hora de ejemplo](sample-time-provider.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de hora de Windows](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



