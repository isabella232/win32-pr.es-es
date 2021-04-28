---
description: 'Método IEnumMedia::Skip: el método Skip omite el siguiente número especificado de elementos en la secuencia de enumeración.'
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: Método IEnumMedia::Skip (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d8c600a201d6800fcb04dba5f208fd5cb810078
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084193"
---
# <a name="ienummediaskip-method"></a>IEnumMedia::Skip (Método)

\[ Los controles e interfaces de conferencia de telefonía IP de Encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Skip** omite el siguiente número especificado de elementos en la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*celta* \[ En\]
</dt> <dd>

Número de elementos que se van a omitir.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                             | Descripción                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | El número de elementos omitido fue *celt*.<br/>     |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El número de elementos omitido no era *de centígrados.*<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




