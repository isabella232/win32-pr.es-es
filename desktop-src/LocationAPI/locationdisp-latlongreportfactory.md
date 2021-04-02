---
description: Administra los informes de latitud y longitud.
ms.assetid: 66025874-32dd-4494-a9ad-12fe3afa60f9
title: Objeto LocationDisp. LatLongReportFactory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9fad1ca0f4605f1167f9b86b0df5bc8f20e46285
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913510"
---
# <a name="locationdisplatlongreportfactory-object"></a>Objeto LocationDisp. LatLongReportFactory

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Administra los informes de latitud y longitud.

## <a name="members"></a>Miembros

El objeto **LocationDisp. LatLongReportFactory** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **LocationDisp. LatLongReportFactory** tiene estos métodos.



| Método                                                                                       | Descripción                                                                                   |
|:---------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**ListenForReports**](locationdisp-latlongreportfactory-listenforreports.md)               | Solicita eventos de informe de latitud y longitud.<br/>                                         |
| [**RequestPermissions**](locationdisp-latlongreportfactory-requestpermissions.md)           | Abre un cuadro de diálogo de sistema para solicitar permiso de usuario para dispositivos habilitados para la ubicación.<br/> |
| [**StopListeningForReports**](/previous-versions/windows/desktop/legacy/dd317718(v=vs.85)) | Cancela las solicitudes de eventos de informe de latitud y longitud.<br/>                             |



 

### <a name="properties"></a>Propiedades

El objeto **LocationDisp. LatLongReportFactory** tiene estas propiedades.



| Propiedad                                                                                | Tipo de acceso           | Descripción                                                                                      |
|:----------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**DesiredAccuracy**](locationdisp-latlongreportfactory-desiredaccuracy.md)<br/> | Lectura/escritura<br/> | Valor de precisión deseado actual.<br/>                                                   |
| [**LatLongReport**](locationdisp-latlongreportfactory-latlongreport.md)<br/>     | Solo lectura<br/>  | Actual [**LocationDisp. DispLatLongReport**](locationdisp-displatlongreport.md).<br/> |
| [**ReportInterval**](locationdisp-latlongreportfactory-reportinterval.md)<br/>   | Lectura/escritura<br/> | El intervalo de eventos de informe de latitud y longitud actual en milisegundos.<br/>                 |
| [**Status**](locationdisp-latlongreportfactory-status.md)<br/>                   | Solo lectura<br/>  | Estado actual del informe.<br/>                                                            |



 

## <a name="examples"></a>Ejemplos

En el código de ejemplo siguiente se muestra cómo crear este objeto en código HTML.


```
<object id="latlongfactory" 
    classid="clsid:9DCC3CC8-8609-4863-BAD4-03601F4C65E8"
    type="application/x-oleobject">
</object>
```



En el ejemplo de código siguiente se muestra cómo crear este objeto en JScript con Windows Script Host.


```JScript
var latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory");
```



En el ejemplo de código siguiente se muestra cómo crear este objeto en VBScript mediante Windows Script Host.


```VB
Dim latlongfactory
Set latlongfactory = WScript.CreateObject("LocationDisp.LatLongReportFactory")
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**LocationDisp.DispLatLongReport**](locationdisp-displatlongreport.md)
</dt> </dl>

 

