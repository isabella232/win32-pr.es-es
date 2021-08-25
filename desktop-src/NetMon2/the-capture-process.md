---
description: El proceso de captura es el mismo para cada una de las cuatro interfaces NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Proceso de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a6d82d721f0f85c6b1ab279d556aaad866f70fde7c8e422995cba5be513d8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889598"
---
# <a name="the-capture-process"></a>Proceso de captura

El proceso de captura es el mismo para cada una de las cuatro interfaces NPP. En cada caso, el proceso incluye:

-   Obtención del objeto de interfaz NPP que se usará
-   Conexión a la red
-   Inicio y detención de la [ *captura*](c.md)
-   Desconectarse de la red

> [!Note]  
> Cuando obtenga el objeto de interfaz que desee, asegúrese de llamar solo a los métodos incluidos en esa interfaz. En la ilustración siguiente se muestra que cada interfaz proporciona métodos similares para capturar datos de red. Se devuelve un error si se conecta a la red con una interfaz y, a continuación, intenta ejecutar una captura mediante los métodos de otra interfaz.

 

En las ilustraciones siguientes se muestran dos maneras diferentes de ejecutar una captura. En la primera ilustración se muestra cómo ejecutar una o varias capturas secuenciales, lo que le permite crear cualquier número de capturas independientes.

![captura secuencial](images/capt1.png)

Como se ha mostrado anteriormente, después de conectarse a la red, puede iniciar y detener una captura tantas veces como desee, iniciando una nueva captura y generando nuevas estadísticas cada vez que reinicie la captura. Por ejemplo, para una captura retrasada mediante la interfaz [](c.md) [**IDelaydC,**](idelaydc.md) se crearía un nuevo archivo de captura cada vez que se reiniciase la captura.

Sin embargo, tenga en cuenta que cada vez que reinicie el proceso de captura debe llamar al método de configuración adecuado para volver a configurar la conexión. Para que la llamada inicial inicie la captura, la llamada configura la conexión para conectarse a la red.

En la segunda ilustración se muestra cómo podría ejecutar una sola captura pausando y reiniciando.

![captura única pausando y reiniciando](images/capt2.png)

En este caso, puede pausar y reiniciar una captura tantas veces como desee. Con este enfoque, puede ejecutar una captura cuyos datos (y sus estadísticas relacionadas) se registran como una sola captura. Por ejemplo, para realizar una captura retrasada mediante la interfaz [**IDelaydC,**](idelaydc.md) toda la información de red capturada se guardaría en un único [*archivo de captura*](c.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CreateNPPInterface**](createnppinterface.md)
</dt> <dt>

[**IDelaydC::Configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC::Conectar**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::D isconnect**](idelaydc-disconnect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC::Resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC::Start**](idelaydc-start.md)
</dt> <dt>

[**IDelaydC::Stop**](idelaydc-stop.md)
</dt> <dt>

[**IESP::Configure**](iesp-configure.md)
</dt> <dt>

[**IESP::Conectar**](iesp-connect.md)
</dt> <dt>

[**IESP::D isconnect**](iesp-disconnect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP::Resume**](iesp-resume.md)
</dt> <dt>

[**IESP::Start**](iesp-start.md)
</dt> <dt>

[**IESP::Stop**](iesp-stop.md)
</dt> <dt>

[**IRTC::Configure**](irtc-configure.md)
</dt> <dt>

[**IRTC::Conectar**](irtc-connect.md)
</dt> <dt>

[**IRTC::D isconnect**](irtc-disconnect.md)
</dt> <dt>

[**IRTC::P ause**](irtc-pause.md)
</dt> <dt>

[**IRTC::Resume**](irtc-resume.md)
</dt> <dt>

[**IRTC::Start**](irtc-start.md)
</dt> <dt>

[**IRTC::Stop**](irtc-stop.md)
</dt> <dt>

[**IStats::Configure**](istats-configure.md)
</dt> <dt>

[**IStats::Conectar**](istats-connect.md)
</dt> <dt>

[**IStats::D isconnect**](istats-disconnect.md)
</dt> <dt>

[**IStats::P ause**](istats-pause.md)
</dt> <dt>

[**IStats::Resume**](istats-resume.md)
</dt> <dt>

[**IStats::Start**](istats-start.md)
</dt> <dt>

[**IStats::Stop**](istats-stop.md)
</dt> </dl>

 

 



