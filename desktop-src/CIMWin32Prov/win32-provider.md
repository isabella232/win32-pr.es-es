---
description: Microsoft&\# 160; El proveedor win32 recupera y actualiza los datos relevantes para los sistemas Windows&8212; datos como la configuración actual de las variables de entorno y los atributos de un disco \# lógico.
ms.assetid: 71c13736-0504-4d50-b8a4-5d68d4ba9a90
ms.tgt_platform: multiple
title: Proveedor win32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dfb29b6f80ed833de0f4185070d46770c6cd2f9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174345"
---
# <a name="win32-provider"></a>Proveedor win32

El proveedor de Microsoft Win32 recupera y actualiza los datos pertinentes para los sistemas Windows, como la configuración actual de las variables de entorno y los atributos de un disco lógico. Con el proveedor Win32, las aplicaciones de administración pueden usar WMI para acceder fácilmente a estos datos. El proveedor de Win32 recupera su información mediante la realización Windows llamadas a funciones y la consulta del registro del sistema.

El proveedor win32 define las clases que se usan para describir el hardware o el software disponible en Windows y las relaciones entre ellos.

Como proveedor de instancias y métodos, el proveedor win32 implementa la interfaz [**IWbemProviderInit**](/windows/win32/api/wbemprov/nn-wbemprov-iwbemproviderinit) estándar, así como los métodos [**IWbemServices**](/windows/win32/api/wbemcli/nn-wbemcli-iwbemservices) siguientes:

-   [**CreateInstanceEnumAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-createinstanceenumasync)
-   [**DeleteInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-deleteinstanceasync)
-   [**ExecMethodAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execmethodasync)
-   [**ExecQueryAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-execqueryasync)
-   [**GetObjectAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-getobjectasync)
-   [**PutInstanceAsync**](/windows/win32/api/wbemcli/nf-wbemcli-iwbemservices-putinstanceasync)

En la tabla siguiente se enumeran las categorías de clases de proveedor de Win32.



| Clases                                                                             | Descripción                                                               |
|-------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)<br/> | Objetos relacionados con el hardware.<br/>                                      |
| [Clases de sistema operativo](operating-system-classes.md)<br/>                 | Objetos relacionados con el sistema operativo.<br/>                              |
| [Clases de contador de rendimiento](performance-counter-classes.md)<br/>           | Datos de rendimiento sin procesar y calculados de contadores de rendimiento.<br/> |
| [Clases de administración de servicios WMI](wmi-service-management-classes.md)<br/>     | Administración de WMI.<br/>                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Proveedor WMI CIMWin32](cimwin32-wmi-providers.md)
</dt> </dl>

 

 
