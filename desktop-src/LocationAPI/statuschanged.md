---
description: Se produce cuando cambia el estado operativo de un informe.
ms.assetid: f0c4e678-1666-4f99-89de-85879eacd0ac
title: Evento StatusChanged
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StatusChanged
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1d1babe150920bb587d24b0b16be0cf662feba252b2b38bc05dc53e3670dd49b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067935"
---
# <a name="statuschanged-event"></a>Evento StatusChanged

\[El modelo de objetos de la API de ubicación está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. En su lugar, para acceder a la ubicación desde un sitio web, use [la API de geolocalización de W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acceder a la ubicación desde una aplicación de escritorio, use el [**Windows. Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]

Se produce cuando cambia el estado operativo de un informe.

## <a name="syntax"></a>Sintaxis


```JScript
.StatusChanged(
  status
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*status* 
</dt> <dd>

Nuevo estado.



| Status                                                                                               | Significado                          |
|------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="0"></span><dl> <dt>**0**</dt> </dl> | Informe no admitido.<br/> |
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | Error.<br/>                |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Acceso denegado:<br/>        |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | Inicializando.<br/>         |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | En ejecución.<br/>              |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este evento no devuelve un valor.

## <a name="remarks"></a>Comentarios

Debe implementar controladores de informes de cambio de estado independientes para los informes de direcciones cívicos y los informes de latitud y longitud.

## <a name="examples"></a>Ejemplos

Para obtener un ejemplo de cómo usar este evento, vea [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/> |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                  |



 

