---
description: 'Método IEnumMedia::Clone: el método Clone crea otro enumerador que contiene el mismo estado de enumeración que el actual.'
ms.assetid: b48399f5-daaa-40e4-bd80-a918539d25c6
title: Método IEnumMedia::Clone (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9f81542e1b0e3fc5bfb44e59827608396d7d906c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068764"
---
# <a name="ienummediaclone-method"></a>IEnumMedia::Clone (método)

\[Los controles e interfaces de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método Clone** crea otro enumerador que contiene el mismo estado de enumeración que el actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] IEnumMedia **ppEnum
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

Puntero al nuevo [**objeto IEnumMedia.**](ienummedia.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppEnum* no es un puntero válido.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | Error por motivos desconocidos.<br/>                          |



 

## <a name="remarks"></a>Observaciones

TAPI llama al **método AddRef** en la [**interfaz IEnumMedia**](ienummedia.md) devuelta por **IEnumMedia::Clone.** La aplicación debe llamar **a Release** en la **interfaz IEnumMedia** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> </dl>

 

 




