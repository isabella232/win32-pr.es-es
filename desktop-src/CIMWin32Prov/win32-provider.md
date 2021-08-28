---
description: Microsoft&\# 160; El proveedor win32 recupera y actualiza los datos pertinentes para Windows systems&8212; datos como la configuración actual de las variables de entorno y los atributos de un \# disco lógico.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Proveedor win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dca4426f849b59dfbfb5f667c32e8e3b9cd47ca7482fd3547d631592a080f968
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118007778"
---
# <a name="win32-provider"></a>Proveedor win32

El proveedor Win32 de Microsoft recupera y actualiza los datos pertinentes para los sistemas Windows, como la configuración actual de las variables de entorno y los atributos de un disco lógico. Con el proveedor Win32, las aplicaciones de administración pueden usar WMI para acceder fácilmente a estos datos. El proveedor win32 recupera su información realizando llamadas Windows función y consultando el registro del sistema.

El proveedor win32 define las clases que se usan para describir el hardware o el software disponible en Windows y las relaciones entre ellos.

Como proveedor de instancias y métodos, el proveedor win32 implementa la interfaz [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como los siguientes [**métodos IWbemServices:**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices)

-   [**CreateInstanceEnumAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**DeleteInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [**ExecMethodAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

En la tabla siguiente se enumeran las categorías de clase de proveedor win32.



| Clases                                                                             | Descripción                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)<br/> | Objetos relacionados con el hardware.<br/>                                      |
| [Clases de sistema operativo](operating-system-classes.md)<br/>                 | Objetos relacionados con el sistema operativo.<br/>                              |
| [Clases de contadores de rendimiento](performance-counter-classes.md)<br/>           | Datos de rendimiento sin procesar y calculados de contadores de rendimiento.<br/> |
| [Clases de administración de servicios WMI](wmi-service-management-classes.md)<br/>     | Administración de WMI.<br/>                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedor WMI CIMWin32](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
