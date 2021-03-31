---
description: Administra informes de direcciones cívicas.
ms.assetid: 46c2d001-409a-4a0a-9006-1c2c9d327c13
title: Objeto LocationDisp. CivicAddressReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 451bb21822d1b56e4c7a45f1587df04761b67690
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816062"
---
# <a name="locationdispcivicaddressreportfactory-object"></a>Objeto LocationDisp. CivicAddressReportFactory

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Administra informes de direcciones cívicas.

## <a name="members"></a>Miembros

El objeto **LocationDisp. CivicAddressReportFactory** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **LocationDisp. CivicAddressReportFactory** tiene estos métodos.



| Método                                                                                            | Descripción                                                                                   |
|:--------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-civicaddressreportfactory-listenforreports.md)               | Solicita eventos del informe de direcciones cívica.<br/>                                              |
| [**RequestPermissions**](locationdisp-civicaddressreportfactory-requestpermissions.md)           | Abre un cuadro de diálogo de sistema para solicitar permiso de usuario para dispositivos habilitados para la ubicación.<br/> |
| [**StopListeningForReports**](locationdisp-civicaddressreportfactory-stoplisteningforreports.md) | Cancela las solicitudes de eventos del informe de direcciones cívica.<br/>                                       |



 

### <a name="properties"></a>Propiedades

El objeto **LocationDisp. CivicAddressReportFactory** tiene estas propiedades.



| Propiedad                                                                                        | Tipo de acceso           | Descripción                                                                                                |
|:------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**CivicAddressReport**](locationdisp-dispcivicaddressreport-civicaddressreport.md)<br/> | Solo lectura<br/>  | Actual [**LocationDisp. DispCivicAddressReport**](locationdisp-dispcivicaddressreport.md).<br/> |
| [**DesiredAccuracy**](locationdisp-civicaddressreportfactory-desiredaccuracy.md)<br/>    | Lectura/escritura<br/> | Configuración de precisión deseada actual.<br/>                                                           |
| [**ReportInterval**](locationdisp-civicaddressreportfactory-reportinterval.md)<br/>      | Lectura/escritura<br/> | El intervalo de eventos del informe de dirección cívica actual en milisegundos.<br/>                                |
| [**Status**](locationdisp-civicaddressreportfactory-status.md)<br/>                      | Solo lectura<br/>  | Estado actual del informe.<br/>                                                                      |



 

## <a name="examples"></a>Ejemplos

En el código de ejemplo siguiente se muestra cómo crear este objeto en código HTML.


```Text
<object id="civicfactory" 
    classid="clsid:2A11F42C-3E81-4ad4-9CBE-45579D89671A"
    type="application/x-oleobject">
</object>
```



En el ejemplo de código siguiente se muestra cómo crear este objeto en JScript con Windows Script Host.


```JScript
var civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory");
```



En el ejemplo de código siguiente se muestra cómo crear este objeto en VBScript mediante Windows Script Host.


```VB
Dim civicfactory
Set civicfactory = WScript.CreateObject("LocationDisp.CivicAddressReportFactory")
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LocationDisp.CivicAddressReport**](locationdisp-dispcivicaddressreport.md)
</dt> </dl>

 

