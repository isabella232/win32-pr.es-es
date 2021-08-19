---
description: Microsoft Windows sistema operativo proporciona compatibilidad con diversos dispositivos de hardware y protocolos de hora de red mediante la arquitectura del proveedor de hora.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67f2073e94bdf893793b4ae1df2974226aa197de4ff429be9ce8f2a2e4b5f597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117957909"
---
# <a name="time-provider"></a>Proveedor de hora

El sistema Windows microsoft proporciona compatibilidad con diversos dispositivos de hardware y protocolos de hora de red mediante la *arquitectura del proveedor de* hora. Los proveedores de hora de entrada recuperan marcas de tiempo precisas del hardware o la red, y los proveedores de hora de salida proporcionan marcas de tiempo a otros clientes de la red.

El administrador de proveedores de hora administra los *proveedores de hora.* Es responsable de cargar, iniciar y detener los proveedores de hora según lo indicado por el administrador de control de servicios. Esta interfaz facilita la escritura de un proveedor de hora que la escritura de un servicio completo.

-   [Crear un proveedor de hora](creating-a-time-provider.md)
-   [Registro de un proveedor de hora](registering-a-time-provider.md)
-   [Proveedor de hora de ejemplo](sample-time-provider.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de hora de Windows](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



