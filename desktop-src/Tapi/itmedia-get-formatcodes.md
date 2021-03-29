---
description: El \_ método get FormatCodes obtiene la lista de códigos de formato de carga de medios. La variante devuelve una SAFEARRAY de BSTR. Cada BSTR dentro de esa matriz es una cadena de código de formato.
ms.assetid: 8663d7e8-d46f-44d1-93db-9b5142bb28dd
title: 'Método ITMedia:: get_FormatCodes (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce9e28a0323ac001c948a3b19b8dae2cfe9daf5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680610"
---
# <a name="itmediaget_formatcodes-method"></a>ITMedia:: get \_ FormatCodes (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ FormatCodes** obtiene la lista de códigos de formato de carga de medios. La variante devuelve una matriz SAFEARRAY de **BSTR** s. Cada **BSTR** dentro de esa matriz es una cadena de código de formato.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_FormatCodes(
  [out] VARIANT *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ enuncia\]
</dt> <dd>

Matriz de códigos de formato de carga de medios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pval* no es un puntero válido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Cuando se proporciona una lista de formatos de carga, esto implica que todos estos formatos se pueden usar en la sesión, pero el primero de estos formatos es el predeterminado para la sesión. Cuando el protocolo de transporte es RTP, los códigos de formato son tipos de carga RTP.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITMedia::p UT \_ FormatCodes**](itmedia-put-formatcodes.md)
</dt> </dl>

 

 




