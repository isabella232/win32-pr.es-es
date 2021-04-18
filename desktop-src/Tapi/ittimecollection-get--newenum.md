---
description: El \_ \_ método get NewEnum devuelve un enumerador para la colección.
ms.assetid: 0c2d739d-736d-4773-9747-1107546a973c
title: 'Método ITTimeCollection:: get__NewEnum (Sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e3fbd171696b81bf5bd67c99b9a91294f4581d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690237"
---
# <a name="ittimecollectionget__newenum-method"></a>ITTimeCollection:: get \_ \_ NewEnum (método)

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ \_ NewEnum** devuelve un enumerador para la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pval* \[ enuncia\]
</dt> <dd>

Puntero a una interfaz [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) en un objeto de enumerador para la colección.

Llame al método [QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la interfaz **IUnknown** devuelta para obtener un puntero a una interfaz de enumeración [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en la colección. **IEnumVARIANT** proporciona varios métodos que puede usar para recorrer en iteración la colección.

Para obtener más información, vea la sección Comentarios que se muestra más adelante.

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

Este método es intercambiable con [**Get \_ EnumerationIf**](ittimecollection-get-enumerationif.md) , salvo que devuelve **IUnknown** en lugar de [**IEnumTime**](ienumtime.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

