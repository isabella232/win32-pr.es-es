---
description: El proceso de captura es el mismo para cada una de las cuatro interfaces NPP.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: El proceso de captura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552691"
---
# <a name="the-capture-process"></a>El proceso de captura

El proceso de captura es el mismo para cada una de las cuatro interfaces NPP. En cada caso, el proceso incluye:

-   Obtener el objeto de interfaz NPP que se va a usar
-   Conexión a la red
-   Inicio y detención de la [ *captura*](c.md)
-   Desconectar de la red

> [!Note]  
> Cuando obtenga el objeto de interfaz que desee, asegúrese de llamar solo a los métodos incluidos en esa interfaz. En la ilustración siguiente se muestra que cada interfaz proporciona métodos similares para capturar datos de red. Se devuelve un error si se conecta a la red con una interfaz y, a continuación, intenta ejecutar una captura con los métodos de otra interfaz.

 

En las ilustraciones siguientes se muestran dos formas diferentes de ejecutar una captura. En la primera ilustración se muestra cómo ejecutar una o varias capturas secuenciales, lo que le permite crear cualquier número de capturas independientes.

![captura secuencial](images/capt1.png)

Como se mostró anteriormente, después de conectarse a la red, puede iniciar y detener una captura tantas veces como desee, iniciando una nueva captura y generando nuevas estadísticas cada vez que reinicie la captura. Por ejemplo, para una captura retrasada mediante la interfaz [**IDelaydC**](idelaydc.md) , se creará un nuevo [*archivo de captura*](c.md) cada vez que reinicie la captura.

Sin embargo, tenga en cuenta también que cada vez que reinicie el proceso de captura, debe llamar al método configure adecuado para volver a configurar la conexión. Para que la llamada inicial inicie la captura, la llamada la configura para conectarse a la red.

En la segunda ilustración se muestra cómo se puede ejecutar una sola captura pausando y reiniciando.

![captura única mediante pausa y reinicio](images/capt2.png)

En este caso, puede pausar y reiniciar una captura tantas veces como desee. Con este enfoque, puede ejecutar una captura cuyos datos (y sus estadísticas relacionadas) se registran como una captura única. Por ejemplo, para realizar una captura diferida mediante la interfaz [**IDelaydC**](idelaydc.md) , toda la información de red capturada se guardaría en un único [*archivo de captura*](c.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CreateNPPInterface**](createnppinterface.md)
</dt> <dt>

[**IDelaydC:: configure**](idelaydc-configure.md)
</dt> <dt>

[**IDelaydC:: Connect**](idelaydc-connect.md)
</dt> <dt>

[**IDelaydC::D Ulta**](idelaydc-disconnect.md)
</dt> <dt>

[**IDelaydC::P ause**](idelaydc-pause.md)
</dt> <dt>

[**IDelaydC:: resume**](idelaydc-resume.md)
</dt> <dt>

[**IDelaydC:: Start**](idelaydc-start.md)
</dt> <dt>

[**IDelaydC:: Stop**](idelaydc-stop.md)
</dt> <dt>

[**IESP:: configure**](iesp-configure.md)
</dt> <dt>

[**IESP:: Connect**](iesp-connect.md)
</dt> <dt>

[**IESP::D Ulta**](iesp-disconnect.md)
</dt> <dt>

[**IESP::P ause**](iesp-pause.md)
</dt> <dt>

[**IESP:: resume**](iesp-resume.md)
</dt> <dt>

[**IESP:: Start**](iesp-start.md)
</dt> <dt>

[**IESP:: Stop**](iesp-stop.md)
</dt> <dt>

[**IRTC:: configure**](irtc-configure.md)
</dt> <dt>

[**IRTC:: Connect**](irtc-connect.md)
</dt> <dt>

[**IRTC::D Ulta**](irtc-disconnect.md)
</dt> <dt>

[**IRTC::P ause**](irtc-pause.md)
</dt> <dt>

[**IRTC:: resume**](irtc-resume.md)
</dt> <dt>

[**IRTC:: Start**](irtc-start.md)
</dt> <dt>

[**IRTC:: Stop**](irtc-stop.md)
</dt> <dt>

[**ISta:: configurar**](istats-configure.md)
</dt> <dt>

[**ISta:: Connect**](istats-connect.md)
</dt> <dt>

[**IStas::D Ulta**](istats-disconnect.md)
</dt> <dt>

[**IStas::P ause**](istats-pause.md)
</dt> <dt>

[**IStas:: resume**](istats-resume.md)
</dt> <dt>

[**ISta:: Start**](istats-start.md)
</dt> <dt>

[**IStas:: Stop**](istats-stop.md)
</dt> </dl>

 

 



