---
title: Registrar objetos en la tabla ROT
description: Registrar objetos en la tabla ROT
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b452ead94a717791910ecceaa5082535bc1b233c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418751"
---
# <a name="registering-objects-in-the-rot"></a>Registrar objetos en la tabla ROT

Normalmente, cuando un cliente solicita a un servidor que cree una instancia de objeto, el servidor crea normalmente un moniker para el objeto y lo registra en la tabla de objetos en ejecución (ROT) a través de una llamada a [**IRunningObjectTable:: Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register).

Cuando el servidor llama a [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) para crear un moniker de archivo que se va a registrar en la tabla Rot, los servidores deben pasar nombres de archivo locales basados en unidad, no en formato UNC. Esto garantiza que los datos de comparación de moniker generados por la llamada de registro de la tabla ROT coincidan con lo que se usa al realizar una búsqueda de la tabla ROT en la parte de un cliente remoto. Esto se debe a que cuando el servicio COM distribuido recibe una solicitud de activación para un archivo local en el servidor desde un cliente remoto, el archivo se convierte en una ruta de acceso basada en unidad local.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalar como una aplicación de servicio](installing-as-a-service-application.md)
</dt> <dt>

[Registrar una clase durante la instalación](registering-a-class-at-installation.md)
</dt> <dt>

[Registrar un servidor EXE en ejecución](registering-a-running-exe-server.md)
</dt> <dt>

[Registro automático](self-registration.md)
</dt> </dl>

 

 




