---
description: 'Método LocationDisp.CivicAddressReportFactory.RequestPermissions: abre un cuadro de diálogo del sistema para solicitar permiso de usuario para dispositivos habilitados para ubicación.'
ms.assetid: b213591a-2830-4979-b532-e71cdef1b994
title: Método LocationDisp.CivicAddressReportFactory.RequestPermissions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58feeedb7f2310a23386ae98a3ff6fe9542f0f7ab90e71e9961a89b0e4954c6e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822275"
---
# <a name="locationdispcivicaddressreportfactoryrequestpermissions-method"></a>Método LocationDisp.CivicAddressReportFactory.RequestPermissions

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use [**el Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Abre un cuadro de diálogo del sistema para solicitar permiso de usuario para dispositivos habilitados para la ubicación.

## <a name="syntax"></a>Sintaxis


```JScript
LocationDisp.CivicAddressReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* 
</dt> <dd>

Este parámetro no se usa y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La llamada es sincrónica y el autor de la llamada espera a que se cierre el cuadro de diálogo.

> [!Note]  
> Si una aplicación que se ejecuta en modo protegido, como un objeto del asistente del explorador (BHO) para Internet Explorer, llama a **RequestPermissions** y el usuario elige la opción No habilitar este **sensor** de ubicación en el cuadro de diálogo, el proveedor de ubicación no se habilitará, pero Windows volverá a mostrar el cuadro de diálogo si el mismo usuario llama de nuevo a **RequestPermissions.** Las aplicaciones que se ejecutan en modo protegido pueden optar por no llamar a [**RequestPermissions**](/windows/win32/api/locationapi/nf-locationapi-ilocation-requestpermissions) en el inicio para que el usuario no vea un cuadro de diálogo posiblemente no deseado cada vez que se inicia la aplicación.

 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [Listening for Civic Address Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

