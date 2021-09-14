---
description: Los proveedores de paquetes de red (NPP) exponen las interfaces IDelaydC, IESP, IRTC e IStats.
ms.assetid: 269b26f5-b794-4920-98da-505eda83c990
title: Selección de una interfaz NPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8dba919302190e1fd89c859f61fca14aaf7d6e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074075"
---
# <a name="selecting-an-npp-interface"></a>Selección de una interfaz NPP

Los proveedores de paquetes de red (NPP) exponen las interfaces [**IDelaydC,**](idelaydc.md) [**IESP,**](iesp.md) [**IRTC**](irtc.md) [**e IStats.**](istats.md) Cada una de estas interfaces proporciona métodos similares para conectar el NPP a la red, capturar el tráfico de red y recopilar información estadística sobre los datos capturados. Para elegir la interfaz que se va a usar, consulte la tabla siguiente.

> [!Note]  
> Al conectar un NPP a la red con una de estas interfaces, solo puede usar los métodos proporcionados por esa interfaz. Por ejemplo, si se conecta a la red mediante la interfaz [**IRTC**](irtc.md) e intenta iniciar una captura con [**IDelaydC,**](idelaydc.md)se producirá un error en la llamada para iniciar la captura y se devolverá un código de error.

 



| Interfaz                    | Cuándo se usa                                                                                                                                                                                                                                                                                                                                     |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDelaydC**](idelaydc.md) | Use para capturar el tráfico de red y almacenarlo en un archivo de captura. Esta interfaz la usa la interfaz Monitor de red usuario y otras aplicaciones NPP, que requieren almacenar la información de red capturada.<br/>                                                                                                                                      |
| [**IESP**](iesp.md)         | Se usa para proporcionar estadísticas mejoradas en un formato de archivo ESP especial. Esta interfaz la usan las aplicaciones NPP que requieren las estadísticas mejoradas proporcionadas por el formato ESP.<br/>                                                                                                                                                        |
| [**IRTC**](irtc.md)         | Use para capturar el tráfico de red en tiempo real y desencadenar eventos cuando se produzcan. Esta interfaz la usan las aplicaciones NPP que requieren capturas en tiempo de ejecución. Tenga en cuenta que esta interfaz no proporciona las estadísticas que proporcionan las otras interfaces NPP, ni permite insertar fotogramas en el tráfico de red capturado.<br/> |
| [**IStats**](istats.md)     | Use para recuperar las estadísticas de captura, pero no los fotogramas capturados.                                                                                                                                                                                                                                                                                 |



 

 

 




