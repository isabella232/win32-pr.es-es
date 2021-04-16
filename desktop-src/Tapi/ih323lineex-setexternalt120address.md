---
description: Una aplicación llama al método SetExternalT120Address para configurar una dirección T. 120 externa para el intercambio de datos.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: 'IH323LineEx:: SetExternalT120Address (método) (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690168"
---
# <a name="ih323lineexsetexternalt120address-method"></a>IH323LineEx:: SetExternalT120Address (método)

\[**SetExternalT120Address** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

Una aplicación llama al método **SetExternalT120Address** para configurar una dirección T. 120 externa para el intercambio de datos. La capacidad t. 120 se anunciará durante la negociación H. 245 y la dirección se usará en la confirmación de canal de lógica abierta para que el otro punto de conexión pueda configurar las sesiones de T. 120 con el servicio escuchando en esa dirección. Si no se llama a esta función, el proveedor de servicios H. 323 no anunciará la capacidad T. 120.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetExternalT120Address(
  [in] BOOL  fEnable,
  [in] DWORD dwIP,
  [in] WORD  wPort
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fEnable* \[ de\]
</dt> <dd>

**True** para habilitar la capacidad T. 120; **False** para deshabilitar la capacidad T. 120.

</dd> <dt>

*dwIP* \[ de\]
</dt> <dd>

**DWORD** que contiene la dirección IP en el orden de bytes de host del servicio T. 120 externo.

</dd> <dt>

*wPort* \[ de\]
</dt> <dd>

**Palabra** que contiene el puerto del servicio T. 120 externo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl> | El método se realizó correctamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>H323priv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




