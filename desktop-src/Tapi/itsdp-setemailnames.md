---
description: El método SetEmailNames establece una matriz de direcciones de correo electrónico asociadas al blob de conferencia.
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: Método ITSdp::SetEmailNames (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ff31e66f5f69fe7fad43da5ec436c3f567cd49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073488"
---
# <a name="itsdpsetemailnames-method"></a>ItSdp::SetEmailNames (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método SetEmailNames** establece una matriz de direcciones de correo electrónico asociadas al blob de conferencia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Direcciones* \[ En\]
</dt> <dd>

SAFEARRAY de **BSTR** que enumeran direcciones de correo electrónico.

</dd> <dt>

*Nombres* \[ En\]
</dt> <dd>

SAFEARRAY de nombres de lista de **BSTR.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro Addresses* o *Names* no es válido.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Las listas a las *que apuntan* *Direcciones* y nombres tienen la misma longitud.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




