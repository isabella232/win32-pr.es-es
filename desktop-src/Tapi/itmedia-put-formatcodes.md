---
description: El método put \_ FormatCodes establece la lista de códigos de formato de carga de medios. La variante contiene una SAFEARRAY de BSTR. Cada BSTR dentro de esa matriz es una cadena de código de formato.
ms.assetid: b76a7fee-0fae-41fb-a8cd-6803458d9182
title: Método ITMedia::p ut_FormatCodes (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9131f946635c2bb066e704f1d6245c1c30d1372
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250274"
---
# <a name="itmediaput_formatcodes-method"></a>Método ITMedia::p ut \_ FormatCodes

\[Los controles e interfaces de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método put \_ FormatCodes** establece la lista de códigos de formato de carga de medios. La variante contiene una SAFEARRAY de **BSTR** s. Cada **BSTR dentro** de esa matriz es una cadena de código de formato.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_FormatCodes(
  [in] VARIANT NewVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewVal* \[ En\]
</dt> <dd>

Lista de códigos de formato de carga de medios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro NewVal* no es válido.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Cuando se da una lista de formatos de carga, esto implica que todos estos formatos se pueden usar en la sesión, pero el primero de estos formatos es el formato predeterminado para la sesión. Cuando el protocolo de transporte es RTP, los códigos de formato son tipos de carga de RTP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::get \_ FormatCodes**](itmedia-get-formatcodes.md)
</dt> </dl>

 

 




