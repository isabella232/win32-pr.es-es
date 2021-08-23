---
description: Si usa la API COM para WMI para recuperar o almacenar información de clase localizada, especifique la configuración regional en el parámetro strLocale en la interfaz IWbemLocator::ConnectServer.
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Recuperar clases modificadas mediante la API COM para WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3752be42a7111e677e7cd60e0bfe9996350f9ae19e7bd0e168d1fa5da82fe42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554029"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a>Recuperar clases modificadas mediante la API COM para WMI

Si usa la API COM para WMI para recuperar o almacenar información de clase localizada, especifique la configuración regional en el parámetro *strLocale* para la [**interfaz IWbemLocator::ConnectServer.**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) Al leer o escribir clases modificadas, indique que desea usar definiciones de clase localizadas especificando WBEM FLAG USE AMENDED QUALIFIERS como marca para el \_ \_ parámetro \_ \_ *iFlags.*

En la tabla siguiente se enumeran las versiones sincrónicas y asincrónicas de los métodos que usan la marca WBEM \_ FLAG \_ USE \_ AMENDED \_ QUALIFIERS.



| Método sincrónico                                                            | Método asincrónico                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IWbemServices::CreateClassEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [**IWbemServices::ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [**IWbemServices::P utClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [**IWbemServices::P utInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [**IWbemServices::P utInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



