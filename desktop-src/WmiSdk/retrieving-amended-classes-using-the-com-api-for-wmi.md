---
description: 'Si usa la API COM para que WMI recupere o almacene información de clase localizada, especifique la configuración regional en el parámetro strLocale de la interfaz IWbemLocator:: ConnectServer.'
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Recuperar clases modificadas mediante la API COM para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103818038"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a>Recuperar clases modificadas mediante la API COM para WMI

Si usa la API COM para que WMI recupere o almacene información de clase localizada, especifique la configuración regional en el parámetro *strLocale* de la interfaz [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) . Al leer o escribir clases modificadas, indique que quiere usar las definiciones de clase localizadas especificando \_ la marca \_ WBEM \_ usar \_ calificadores modificados como una marca para el parámetro *iFlags* .

En la tabla siguiente se enumeran las versiones sincrónicas y asincrónicas de los métodos que usan la marca WBEM \_ \_ usar el indicador de \_ \_ calificadores modificados.



| Método sincrónico                                                            | Método asincrónico                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IWbemServices:: CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



