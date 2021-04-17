---
description: El método siguiente obtiene el siguiente número de elementos especificado en la secuencia de enumeración.
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'IEnumMedia:: Next (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04b92220d8fe93058533427ff8cc7bcc7ad7a02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681143"
---
# <a name="ienummedianext-method"></a>IEnumMedia:: Next (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **siguiente** obtiene el siguiente número de elementos especificado en la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Celt* \[ de\]
</dt> <dd>

Número de elementos solicitados.

</dd> <dt>

*pval* \[ enuncia\]
</dt> <dd>

Puntero a la interfaz [**ITMedia**](itmedia.md) .

</dd> <dt>

*pceltFetched* \[ enuncia\]
</dt> <dd>

Puntero al número de elementos proporcionados realmente. Puede ser **null** si *Celt* es uno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                     | Significado                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El método devolvió un número de elementos de *Celt* .<br/>         |
| <dl> <dt>**S \_ false**</dt> </dl>   | El número de elementos restantes era menor que *Celt*.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl> | El parámetro *pval* no es un puntero válido.<br/>       |



 

## <a name="remarks"></a>Observaciones

TAPI llama al método **AddRef** en la interfaz [**ITMedia**](itmedia.md) devuelta por **IEnumMedia:: Next**. La aplicación debe llamar a **Release** en la interfaz **ITMedia** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




