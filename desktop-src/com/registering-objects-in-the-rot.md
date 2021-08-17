---
title: Registro de objetos en ROT
description: Registro de objetos en ROT
ms.assetid: f479c2d1-0c55-4281-8f15-2f957fa03b70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d77e7bc6fe8b0a4d5896bf33575df2f57fb0e583f78acd02653f6ccb014f34ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118104825"
---
# <a name="registering-objects-in-the-rot"></a>Registro de objetos en ROT

Normalmente, cuando un cliente solicita a un servidor que cree una instancia de objeto, el servidor normalmente crea un moniker para el objeto y lo registra en la tabla de objetos en ejecución (ROT) mediante una llamada a [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register).

Cuando el servidor llama a [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) para crear un moniker de archivo que se va a registrar en ROT, los servidores deben pasar nombres de archivo locales basados en unidades, no en formato UNC. Esto garantiza que los datos de comparación del moniker generados por la llamada de registro de ROT coincidirán con lo que se usa al realizar una búsqueda de ROT por parte de un cliente remoto. Esto se debe a que cuando el servicio COM distribuido recibe una solicitud de activación para un archivo local en el servidor desde un cliente remoto, el archivo se convierte en una ruta de acceso basada en unidad local.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instalación como aplicación de servicio](installing-as-a-service-application.md)
</dt> <dt>

[Registro de una clase durante la instalación](registering-a-class-at-installation.md)
</dt> <dt>

[Registro de un servidor EXE en ejecución](registering-a-running-exe-server.md)
</dt> <dt>

[Registro propio](self-registration.md)
</dt> </dl>

 

 




