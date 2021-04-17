---
description: El \_ método get EnumerationIf obtiene un puntero a una interfaz de enumeración multimedia.
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'Método ITMediaCollection:: get_EnumerationIf (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a7e7d85c1f7a433a31360fabc8b5dac71e68ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690625"
---
# <a name="itmediacollectionget_enumerationif-method"></a>ITMediaCollection:: get \_ EnumerationIf (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ EnumerationIf** obtiene un puntero a una interfaz de enumeración multimedia.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ enuncia\]
</dt> <dd>

Puntero a la interfaz [**IEnumMedia**](ienummedia.md) para el elemento deseado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pval* no es un puntero válido.<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Observaciones

Este método es intercambiable con [**Get \_ \_ NewEnum**](itmediacollection-get--newenum.md) , salvo que devuelve [**IEnumMedia**](ienummedia.md) en lugar de **IUnknown**.

TAPI llama al método **AddRef** en la interfaz [**IEnumMedia**](ienummedia.md) devuelta por **ITMediaCollection:: get \_ Enumerationlf**. La aplicación debe llamar a **Release** en la interfaz **IEnumMedia** para liberar recursos asociados a ella.

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
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




