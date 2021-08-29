---
description: El método get \_ Item devuelve el atributo especificado por el índice.
ms.assetid: 67e36587-0bf5-4586-ace9-ef107f0b6548
title: Método ITAttributeList::get_Item (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21ffa22eadf9dac4af55b46b59c22a2b265b53a4ec582e36ab563d0fffb36fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003473"
---
# <a name="itattributelistget_item-method"></a>ITAttributeList::get \_ Item (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ Item** devuelve el atributo especificado por el índice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Item(
  [in]  LONG Index,
  [out] BSTR *pVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ En\]
</dt> <dd>

Índice del elemento que se obtiene.

</dd> <dt>

*pVal* \[ out\]
</dt> <dd>

Puntero a un **BSTR** que contiene los valores del elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pVal* no es un puntero válido.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro Index* no es válido.<br/>                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

## <a name="remarks"></a>Comentarios

La aplicación debe usar [**SysFreeString para**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) liberar la memoria asignada para el *parámetro pVal.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITAttributeList**](itattributelist.md)
</dt> </dl>

 

