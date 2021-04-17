---
description: El método siguiente obtiene el siguiente número de elementos especificado en la secuencia de enumeración.
ms.assetid: e8ca77b8-0322-43b4-9996-26f584cf878a
title: 'IEnumTime:: Next (método) (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce3d88bc88e808c35ec64f827fd5925ddfe57f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681278"
---
# <a name="ienumtimenext-method"></a>IEnumTime:: Next (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **siguiente** obtiene el siguiente número de elementos especificado en la secuencia de enumeración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Next(
  [in]  ULONG  celt,
  [out] ITTime **pVal,
  [out] ULONG  *pceltFetched
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

Puntero a la interfaz [**ITTime**](ittime.md) .

</dd> <dt>

*pceltFetched* \[ enuncia\]
</dt> <dd>

Puntero al número de elementos proporcionados realmente. Puede ser **null** si *Celt* es 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                     | Significado                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El método devolvió un número de elementos de *Celt* .<br/>         |
| <dl> <dt>**S \_ false**</dt> </dl>   | El número de elementos restantes era menor que *Celt*.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl> | El parámetro *pval* no es un puntero válido.<br/>       |



 

## <a name="remarks"></a>Observaciones

TAPI llama al método **AddRef** en la interfaz [**ITTime**](ittime.md) devuelta por **IEnumTime:: Next**. La aplicación debe llamar a **Release** en la interfaz **ITTime** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> </dl>

 

 




