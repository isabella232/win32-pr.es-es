---
description: El método get \_ FormatCodes obtiene la lista de códigos de formato de carga de medios. La variante devuelve una SAFEARRAY de BSTR. Cada BSTR dentro de esa matriz es una cadena de código de formato.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: Método ITMedia::get_FormatCodes (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a785bd4a5a4e45bf7a6be5e1c4cb68ee8125b28aa5808c19393f8be24df7a8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774915"
---
# <a name="itmediaget_formatcodes-method"></a>ItMedia::get \_ FormatCodes (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ FormatCodes** obtiene la lista de códigos de formato de carga de medios. La variante devuelve una SAFEARRAY de **BSTR** s. Cada **BSTR dentro** de esa matriz es una cadena de código de formato.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out\]
</dt> <dd>

Matriz de códigos de formato de carga de medios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pVal* no es un puntero válido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

Cuando se da una lista de formatos de carga, esto implica que todos estos formatos se pueden usar en la sesión, pero el primero de estos formatos es el formato predeterminado para la sesión. Cuando el protocolo de transporte es RTP, los códigos de formato son tipos de carga de RTP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::put \_ FormatCodes**](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




