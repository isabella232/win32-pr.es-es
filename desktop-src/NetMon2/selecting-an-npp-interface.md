---
description: Los proveedores de paquetes de red (NPPs) exponen las interfaces IDelaydC, IESP, IRTC y IStas.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Seleccionar una interfaz NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908695"
---
# <a name="selecting-an-npp-interface"></a>Seleccionar una interfaz NPP

Los proveedores de paquetes de red (NPPs) exponen las interfaces [**IDelaydC**](idelaydc.md), [**iesp**](iesp.md), [**IRTC**](irtc.md)y [**istas**](istats.md) . Cada una de estas interfaces proporciona métodos similares para conectar el NPP a la red, capturar el tráfico de red y recopilar información estadística sobre los datos capturados. Para elegir la interfaz que se va a usar, consulte la tabla siguiente.

> [!Note]  
> Cuando conecta un NPP a la red con una de estas interfaces, solo puede usar los métodos proporcionados por esa interfaz. Por ejemplo, si se conecta a la red mediante la interfaz [**IRTC**](irtc.md) y, a continuación, intenta iniciar una captura con [**IDelaydC**](idelaydc.md), se producirá un error en la llamada para iniciar la captura y se devolverá un código de error.

 



| Interfaz                    | Cuándo se usa                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDelaydC**](idelaydc.md) | Use para capturar el tráfico de red y almacenarlo en un archivo de captura. Esta interfaz la utilizan la interfaz de usuario de Monitor de red y otras aplicaciones NPP, que requieren el almacenamiento de la información de red capturada.<br/>                                                                                                                                      |
| [**IESP**](iesp.md)         | Se utiliza para proporcionar estadísticas mejoradas en un formato de archivo ESP especial. Esta interfaz la usan las aplicaciones NPP que requieren las estadísticas mejoradas proporcionadas por el formato ESP.<br/>                                                                                                                                                        |
| [**IRTC**](irtc.md)         | Se usa para capturar el tráfico de red en tiempo real y desencadenar eventos cuando se producen. Esta interfaz la usan las aplicaciones NPP que requieren capturas en tiempo de ejecución. Tenga en cuenta que esta interfaz no proporciona las estadísticas que proporcionan las otras interfaces NPP, ni le permite insertar fotogramas en el tráfico de red capturado.<br/> |
| [**IStas**](istats.md)     | Use para recuperar estadísticas de captura, pero no los fotogramas capturados.                                                                                                                                                                                                                                                                                 |



 

 

 




