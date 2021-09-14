---
description: Una aplicación llama al método SetExternalT120Address para configurar una dirección T.120 externa para el intercambio de datos.
ms.assetid: 094b43b9-eb15-468a-9986-86313490e1c3
title: Método IH323LineEx::SetExternalT120Address (H323priv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09756aaf77ba36497b3059f7e93829d7d6a57b42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068749"
---
# <a name="ih323lineexsetexternalt120address-method"></a>IH323LineEx::SetExternalT120Address (método)

\[**SetExternalT120Address** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Una aplicación llama al método **SetExternalT120Address** para configurar una dirección T.120 externa para el intercambio de datos. La funcionalidad T.120 se anunciará durante la negociación de H.245 y la dirección se usará en la confirmación del canal lógico abierto para que el otro punto de conexión pueda configurar sesiones de T.120 con el servicio que escucha en esa dirección. Si no se llama a esta función, el proveedor de servicios H.323 no anunciará la funcionalidad T.120.

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

*fEnable* \[ En\]
</dt> <dd>

**TRUE** para habilitar la funcionalidad T.120; **FALSE** para deshabilitar la funcionalidad T.120.

</dd> <dt>

*dwIP* \[ En\]
</dt> <dd>

**DWORD** que contiene la dirección IP en orden de bytes del host del servicio T.120 externo.

</dd> <dt>

*wPort* \[ En\]
</dt> <dd>

**WORD** que contiene el puerto del servicio T.120 externo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                          | Descripción                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | El método se realizó correctamente.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>H323priv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

 




