---
title: Difxapi.h
description: Esta sección contiene temas de referencia para el encabezado Difxapi.h.
ms.assetid: 84da7e54-0677-495e-9dc5-aca4ac12c0b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5dcace8f7f8c8ed528849da02016f04e0ca32b2132c7b0587a96872d7cc561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736033"
---
# <a name="difxapih"></a>Difxapi.h

Esta sección contiene temas de referencia para el encabezado Difxapi.h.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                 | Descripción                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*DIFLOGCALLBACK*](/previous-versions/windows/hardware/difxapi/diflogcallback)<br/>                     | Una función con tipo **DIFLOGCALLBACK** es una función de devolución de llamada proporcionada por la aplicación que una aplicación registra mediante una llamada a [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback). DIFxAPI llama a la función de devolución de llamada para registrar los eventos que se producen durante la operación de DIFxAPI.<br/>                        |
| [*DIFXAPILOGCALLBACK*](/previous-versions/windows/hardware/difxapi/difxapilogcallback)<br/>             | Una función con tipo **DIFXAPILOGCALLBACK** es una función de devolución de llamada proporcionada por la aplicación que una aplicación registra con DIFxAPI mediante una llamada a [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback). DIFxAPI llama a la función de devolución de llamada para registrar los eventos que se producen durante la operación de DIFxAPI.<br/> |
| [**DIFXAPISetLogCallback**](/previous-versions/windows/hardware/difxapi/difxapisetlogcallback)<br/>     | La **función DIFXAPISetLogCallback** registra una función de devolución de llamada proporcionada por el autor de la llamada a la que DIFxAPI llama para registrar información sobre los eventos que se producen durante las operaciones de DIFxAPI. <br/>                                                                                                            |
| [**DriverPackageGetPath**](/previous-versions/windows/hardware/difxapi/driverpackagegetpath)<br/>       | La **función DriverPackageGetPath** recupera la ruta de acceso completa del archivo [INF](/windows-hardware/drivers/install/overview-of-inf-files) para un paquete de [controladores preinstalado.](/windows-hardware/drivers/install/driver-packages)<br/>                                                                                                               |
| [**DriverPackageInstall**](/previous-versions/windows/hardware/difxapi/driverpackageinstall)<br/>       | La **función DriverPackageInstall** preinstala un paquete [de controladores](/windows-hardware/drivers/install/driver-packages) y, a continuación, instala el controlador en el sistema.<br/>                                                                                                                                                 |
| [**DriverPackagePreinstall**](/previous-versions/windows/hardware/difxapi/driverpackagepreinstall)<br/> | La **función DriverPackagePreinstall** preinstala [](/windows-hardware/drivers/install/driver-packages) un paquete de controladores para un controlador de función Plug and Play (PnP) e instala el archivo [INF](/windows-hardware/drivers/install/overview-of-inf-files) para el paquete de controladores en el directorio de archivos INF del sistema. [](/windows-hardware/drivers/kernel/function-drivers)<br/>             |
| [**DriverPackageUninstall**](/previous-versions/windows/hardware/difxapi/driverpackageuninstall)<br/>   | La **función DriverPackageUninstall** desinstala el paquete de [controladores](/windows-hardware/drivers/install/driver-packages) especificado del sistema y quita el paquete de controladores. <br/>                                                                                                                               |
| [**INSTALLERINFO**](/previous-versions/windows/hardware/difxapi/installerinfo)<br/>                     | La estructura INSTALLERINFO contiene información sobre una aplicación que DIFxAPI asocia a un paquete [de controladores](/windows-hardware/drivers/install/driver-packages). <br/>                                                                                                                                          |
| [**SetDifxLogCallback**](/previous-versions/windows/hardware/difxapi/setdifxlogcallback)<br/>           | La **función SetDifxLogCallback** registra una función de devolución de llamada proporcionada por el autor de la llamada a la que DIFxAPI llama para registrar información sobre los eventos que se producen durante las operaciones de DIFxAPI. <br/>                                                                                                               |



 

 

 

[Envío de comentarios sobre este tema a Microsoft](mailto:wsddocfb@microsoft.com?subject=Documentation%20feedback%20%5Bdevinst\devinst%5D:%20Difxapi.h%20%20RELEASE:%20%283/29/2018%29&body=%0A%0APRIVACY%20STATEMENT%0A%0AWe%20use%20your%20feedback%20to%20improve%20the%20documentation.%20We%20don't%20use%20your%20email%20address%20for%20any%20other%20purpose,%20and%20we'll%20remove%20your%20email%20address%20from%20our%20system%20after%20the%20issue%20that%20you're%20reporting%20is%20fixed.%20While%20we're%20working%20to%20fix%20this%20issue,%20we%20might%20send%20you%20an%20email%20message%20to%20ask%20for%20more%20info.%20Later,%20we%20might%20also%20send%20you%20an%20email%20message%20to%20let%20you%20know%20that%20we've%20addressed%20your%20feedback.%0A%0AFor%20more%20info%20about%20Microsoft's%20privacy%20policy,%20see%20http://privacy.microsoft.com/default.aspx. "Envío de comentarios sobre este tema a Microsoft")