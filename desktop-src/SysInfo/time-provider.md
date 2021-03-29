---
description: El sistema operativo Microsoft Windows proporciona compatibilidad con una variedad de dispositivos de hardware y protocolos de tiempo de red que usan la arquitectura de proveedor de hora.
ms.assetid: a7575373-eeda-4f2a-85e5-d1b50994e7ae
title: Proveedor de hora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c844e2c4d0d49e87e978a47621338b167c4f5a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911998"
---
# <a name="time-provider"></a>Proveedor de hora

El sistema operativo Microsoft Windows proporciona compatibilidad con una variedad de dispositivos de hardware y protocolos de tiempo de red que usan la arquitectura de *proveedor de hora* . Los proveedores de hora de entrada recuperan las marcas de tiempo precisas del hardware o la red, y los proveedores de tiempo de salida proporcionan marcas de tiempo a otros clientes de la red.

Los proveedores de hora se administran mediante el *Administrador de proveedores de hora*. Es responsable de cargar, iniciar y detener los proveedores de hora según lo indicado por el administrador de control de servicios. Esta interfaz facilita la escritura de un proveedor de hora que escribir un servicio completo.

-   [Creación de un proveedor de hora](creating-a-time-provider.md)
-   [Registrar un proveedor de hora](registering-a-time-provider.md)
-   [Proveedor de tiempo de ejemplo](sample-time-provider.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicio de hora de Windows](https://www.microsoft.com/technet/prodtechnol/windowsserver2003/technologies/security/ws03mngd/26_s3wts.mspx)
</dt> </dl>

 

 



