---
description: Abre un cuadro de diálogo de sistema para solicitar permiso de usuario para dispositivos habilitados para la ubicación.
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: LocationDisp. LatLongReportFactory. RequestPermissions, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed789aca4b6c9d0db50a3e7b6cae33d55d22920c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678035"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>LocationDisp. LatLongReportFactory. RequestPermissions, método

\[El modelo de objetos de API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use la [API de geolocalización del W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows. Devices. geolocation**](/uwp/api/Windows.Devices.Geolocation) .\]

Abre un cuadro de diálogo de sistema para solicitar permiso de usuario para dispositivos habilitados para la ubicación.

## <a name="syntax"></a>Sintaxis


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* 
</dt> <dd>

Este parámetro no se utiliza y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La llamada es sincrónica y el autor de la llamada espera a que se cierre el cuadro de diálogo.

> [!Note]  
> Si una aplicación que se ejecuta en modo protegido, como un objeto auxiliar de explorador (BHO) de Internet Explorer, llama a **RequestPermissions** y el usuario elige la opción **no habilitar este sensor de ubicación** en el cuadro de diálogo, el proveedor de ubicación no se habilitará, pero Windows volverá a mostrar el cuadro de diálogo si el mismo usuario llama a **RequestPermissions** de nuevo. Las aplicaciones que se ejecutan en modo protegido pueden optar por no llamar a **RequestPermissions** en el inicio para que el usuario no vea un cuadro de diálogo posiblemente no deseado cada vez que se inicie la aplicación.

 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, consulte [escucha de eventos de informe de LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

