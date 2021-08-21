---
description: Los sensores lógicos proporcionan datos sin depender de los dispositivos de hardware.
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: Acerca de los sensores lógicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 655bb7a6e67223bb959b155e55f6cc059ffd8280bc8c08fb00d4d88cb2c8b0a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003902"
---
# <a name="about-logical-sensors"></a>Acerca de los sensores lógicos

*Los sensores* lógicos proporcionan datos sin depender de los dispositivos de hardware. Por ejemplo, un sensor lógico podría proporcionar datos sobre la ubicación actual del usuario mediante un servicio que busca una dirección IP en una tabla. Los sensores lógicos se implementan como controladores de sensor. Para obtener información sobre cómo implementar un controlador de sensor, consulte el Windows Driver Kit.

Una vez instalado un sensor lógico en el equipo del usuario, puede usarlo de la misma manera que un sensor basado en hardware. Sensor API proporcionará una interfaz [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) para representar el sensor lógico y el programa puede solicitar datos a través de los mismos mecanismos que usaría para cualquier otro tipo de sensor. Los sensores lógicos también pueden usar las categorías de sensor definidas por la plataforma, los tipos, los tipos de datos, las propiedades y los eventos. O bien, puede definir valores personalizados.

La [**interfaz ILogicalSensorManager permite**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) a los desarrolladores que crean sensores lógicos administrar las conexiones a la plataforma Sensor y Location.

> [!Note]  
> Al igual que con otros controladores, la instalación o desinstalación de un controlador de sensor lógico requiere privilegios de administrador.

 

Para probar a usar un sensor lógico de ejemplo, consulte [Acerca de los ejemplos y las herramientas.](about-the-samples.md)

## <a name="managing-logical-sensors"></a>Administración de sensores lógicos

[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) tiene los métodos siguientes:

-   [**Conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**Desconectar**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**Desinstalar**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

Al llamar a Conectar , sensor API crea una instancia del controlador del sensor, si aún no existe, y, [**a**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))continuación, conecta el sensor lógico a la plataforma. Esto significa que el sensor lógico aparece con otros sensores en **el Ubicación y otros sensores** Panel de control. Cuando se llama [**a Desconectar**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)), la API de sensor desconecta el sensor lógico y lo quita del Panel de control. Al **llamar a Disconnect** no se quita el sensor lógico **Administrador de dispositivos**. Por lo tanto, las **llamadas Conectar** tendrán como resultado una conexión mucho más rápida al sensor lógico.

Para quitar un sensor lógico, debe llamar a [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)). Al desinstalar un sensor lógico, se quita el sensor **Administrador de dispositivos**. Dado que los dispositivos de sensor lógico solo existen en la memoria, se desinstala un sensor lógico cuando el usuario Windows.

La API de sensor identifica un sensor lógico determinado por su *identificador lógico*, que es un **GUID.** Cada vez que se conecta a un sensor lógico determinado, debe proporcionar un identificador lógico. Cada vez que desconecte o desinstale un sensor determinado, debe proporcionar el mismo identificador lógico que usó para conectarse. Si se conecta varias veces al mismo controlador de sensor lógico mediante identificadores lógicos diferentes, creará una instancia independiente del sensor lógico para cada nuevo identificador lógico. Incluso si llama a [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) para cada identificador lógico, estas instancias independientes permanecerán en Administrador de dispositivos hasta que llame **a** [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) para cada sensor lógico o el usuario reinicie Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de sensores lógicos](using-logical-sensors.md)
</dt> </dl>

 

 
