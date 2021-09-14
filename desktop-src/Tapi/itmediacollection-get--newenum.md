---
description: 'ItMediaCollection::get__NewEnum método : el método get \_ \_ NewEnum devuelve un enumerador para la colección.'
ms.assetid: 22b1eb48-e1ef-4694-a1dc-b2de326989c8
title: Método ITMediaCollection::get__NewEnum (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6683ce0a00f0128cb959dd5a2c39e8b06382f65d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160656"
---
# <a name="itmediacollectionget__newenum-method"></a>ItMediaCollection::get \_ \_ NewEnum (método)

\[Los controles e interfaces de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ \_ NewEnum** devuelve un enumerador para la colección.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get__NewEnum(
  [out] IUnknown **pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVal* \[ out\]
</dt> <dd>

Puntero a una [interfaz IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) en un objeto enumerador de la colección.

Llame al [método QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en la interfaz **IUnknown** devuelta para obtener un puntero a una interfaz de enumeración [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) en la colección. **IEnumVARIANT proporciona** una serie de métodos que puede usar para recorrer en iteración la colección.

Para obtener más información, vea la sección Comentarios que se muestra más adelante.

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



 

## <a name="remarks"></a>Observaciones

Este método es intercambiable con [**get \_ EnumerationIf, salvo**](itmediacollection-get-enumerationif.md) que devuelve **IUnknown en** lugar de [**IEnumMedia.**](ienummedia.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

