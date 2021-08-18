---
description: El método put \_ AttributeList establece la lista de atributos.
ms.assetid: f7d57c0c-9114-42a4-b2bc-c812334d8136
title: ItAttributeList::p ut_AttributeList (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c68ccbf8349b9f78f2893263345f7f76af2dec3e197daa73789a471887d685c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003483"
---
# <a name="itattributelistput_attributelist-method"></a>ItAttributeList::p ut \_ AttributeList (método)

\[Las interfaces y los controles de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método put \_ AttributeList** establece la lista de atributos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AttributeList(
  [in] VARIANT newVal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*newVal* \[ En\]
</dt> <dd>

Matriz de atributos que se establecerán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro newVal* no es válido.<br/>                 |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Error no especificado.<br/>                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>     | Este método aún no se ha implementado.<br/>                  |



 

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
</dt> <dt>

[**ITAttributeList::get \_ AttributeList**](itattributelist-get-attributelist.md)
</dt> </dl>

 

 




