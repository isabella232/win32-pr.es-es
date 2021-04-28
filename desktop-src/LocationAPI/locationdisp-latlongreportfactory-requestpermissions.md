---
description: 'Método LocationDisp.LatLongReportFactory.RequestPermissions: abre un cuadro de diálogo del sistema para solicitar permiso de usuario para dispositivos habilitados para ubicación.'
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: Método LocationDisp.LatLongReportFactory.RequestPermissions
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
ms.openlocfilehash: 1b2d21a032a2e4c08c6f80e4f0ae79349a49ce21
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088933"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>Método LocationDisp.LatLongReportFactory.RequestPermissions

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use la API [**Windows.Devices.Geolocation.**](/uwp/api/Windows.Devices.Geolocation)\]

Abre un cuadro de diálogo del sistema para solicitar permiso de usuario para dispositivos habilitados para la ubicación.

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

Este parámetro no se usa y debe establecerse en cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La llamada es sincrónica y el autor de la llamada espera a que se cierre el cuadro de diálogo.

> [!Note]  
> Si una aplicación que se ejecuta en modo protegido, como un objeto del asistente del explorador (BHO) para Internet Explorer, llama a **RequestPermissions** y el usuario elige la opción No habilitar este **sensor** de ubicación en el cuadro de diálogo, el proveedor de ubicación no estará habilitado, pero Windows volverá a mostrar el cuadro de diálogo si el mismo usuario llama de nuevo a **RequestPermissions.** Las aplicaciones que se ejecutan en modo protegido pueden optar por no llamar a **RequestPermissions** en el inicio para que el usuario no vea un cuadro de diálogo posiblemente no deseado cada vez que se inicia la aplicación.

 

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este método, vea [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

