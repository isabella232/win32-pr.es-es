---
title: Función RtmCloseEnumerationHandle (Rtm.h)
description: RtmCloseEnumerationHandle finaliza una enumeración especificada y libera los recursos asociados.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- Función RAS RtmCloseEnumerationHandle
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271932"
---
# <a name="rtmcloseenumerationhandle-function"></a>Función RtmCloseEnumerationHandle

\[Esta API se ha reemplazado por la API [de Routing Table Manager versión 2](about-routing-table-manager-version-2.md) y no estará disponible más allá de Windows Server 2003. Las aplicaciones deben usar la API de Routing Table Manager versión 2.\]

**RtmCloseEnumerationHandle** finaliza una enumeración especificada y libera los recursos asociados.

## <a name="syntax"></a>Sintaxis


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EnumerationHandle* \[ En\]
</dt> <dd>

Controlar la enumeración que se finalizará. Obtenga este identificador mediante una llamada [**a RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NO \_ ERROR.

Si se produce un error en la función, el valor devuelto es uno de los siguientes códigos de error.



| Value                                                                                                       | Descripción                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**IDENTIFICADOR \_ DE ERROR NO \_ VÁLIDO**</dt> </dl>       | Parámetro no válido.<br/>                                  |
| <dl> <dt>**ERROR \_ SIN RECURSOS DEL \_ \_ SISTEMA**</dt> </dl> | No hay recursos suficientes para llevar a cabo la operación.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Rtm.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Rtm.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Referencia de la versión 1 de Routing Table Manager](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Funciones de Routing Table Manager versión 1](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





