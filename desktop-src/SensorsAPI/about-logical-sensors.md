---
description: Los sensores lógicos proporcionan datos sin depender de los dispositivos de hardware.
ms.assetid: fb0f0324-d72e-4759-9f4d-deedf8848e21
title: Acerca de los sensores lógicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6f8687575aaedbb006eb2ad6ebaad9cf8d3ab6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668301"
---
# <a name="about-logical-sensors"></a>Acerca de los sensores lógicos

Los *sensores lógicos* proporcionan datos sin depender de los dispositivos de hardware. Por ejemplo, un sensor lógico podría proporcionar datos sobre la ubicación actual del usuario mediante un servicio que busque una dirección IP en una tabla. Los sensores lógicos se implementan como controladores de sensor. Para obtener información sobre cómo implementar un controlador de sensor, consulte el kit de controladores de Windows.

Después de instalar un sensor lógico en el equipo del usuario, puede usarlo de la misma manera que un sensor basado en hardware. La API de sensor proporcionará una interfaz [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) para representar el sensor lógico y el programa puede solicitar datos a través de los mismos mecanismos que usaría para cualquier otro tipo de sensor. Los sensores lógicos también pueden usar las categorías de sensor, los tipos, los tipos de datos, las propiedades y los eventos definidos por la plataforma. O bien, puede definir valores personalizados.

La interfaz [**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) permite a los desarrolladores que crean sensores lógicos administrar las conexiones a la plataforma de sensor y ubicación.

> [!Note]  
> Como con otros controladores, la instalación o desinstalación de un controlador de sensor lógico requiere privilegios de administrador.

 

Para probar el uso de un sensor lógico de ejemplo, consulte [acerca de los ejemplos y las herramientas](about-the-samples.md).

## <a name="managing-logical-sensors"></a>Administrar sensores lógicos

[**ILogicalSensorManager**](/previous-versions/windows/desktop/legacy/dd318934(v=vs.85)) tiene los siguientes métodos:

-   [**Conectar**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85))
-   [**Desconectar**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85))
-   [**Desinstalar**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85))

Cuando se llama a [**Connect**](/previous-versions/windows/desktop/legacy/dd374029(v=vs.85)), la API del sensor crea una instancia del controlador del sensor, si aún no existe, y, a continuación, conecta el sensor lógico a la plataforma. Esto significa que el sensor lógico aparece con otros sensores en el panel de control **Ubicación y otros sensores** . Cuando se llama a [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)), la API de sensor desconecta el sensor lógico y lo quita del panel de control. La llamada a **Disconnect** no quita el sensor lógico de **Administrador de dispositivos**. Por lo tanto, las llamadas futuras a **Connect** darán lugar a una conexión mucho más rápida al sensor lógico.

Para quitar un sensor lógico, debe llamar a [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)). La desinstalación de un sensor lógico quita el sensor de **Administrador de dispositivos**. Dado que los dispositivos de sensor lógico solo existen en la memoria, se desinstala un sensor lógico cuando el usuario reinicia Windows.

La API de sensor identifica un sensor lógico determinado por su *identificador lógico*, que es un **GUID**. Cada vez que se conecta a un sensor lógico determinado, debe proporcionar un identificador lógico. Cada vez que desconecte o desinstale un sensor determinado, debe proporcionar el mismo identificador lógico que usó para conectarse. Si se conecta al mismo controlador de sensor lógico varias veces mediante identificadores lógicos diferentes, creará una instancia independiente del sensor lógico para cada nuevo identificador lógico. Incluso si se llama a [**Disconnect**](/previous-versions/windows/desktop/legacy/dd374030(v=vs.85)) para cada identificador lógico, estas instancias independientes permanecerán en **Administrador de dispositivos** hasta que se llame a [**Uninstall**](/previous-versions/windows/desktop/legacy/dd374031(v=vs.85)) para cada sensor lógico, o cuando el usuario reinicie Windows.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de sensores lógicos](using-logical-sensors.md)
</dt> </dl>

 

 
