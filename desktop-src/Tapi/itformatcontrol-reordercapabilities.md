---
description: El método ReOrderCapabilities establece un nuevo orden para las capacidades de formato.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'ITFormatControl:: ReOrderCapabilities (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680465"
---
# <a name="itformatcontrolreordercapabilities-method"></a>ITFormatControl:: ReOrderCapabilities (método)

\[ Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **ReOrderCapabilities** establece un nuevo orden para las capacidades de formato.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdwIndices* \[ de\]
</dt> <dd>

Índice del formato que se va a reordenar.

</dd> <dt>

*pfEnabled* \[ de\]
</dt> <dd>

Indica si el formato debe estar habilitado o deshabilitado.

</dd> <dt>

*pfPublicize* \[ de\]
</dt> <dd>

Indica si el formato debe estar disponible.

</dd> <dt>

*dwNumIndices* \[ de\]
</dt> <dd>

Nuevo número de índice para el formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

Se debe llamar al método [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,1<br/>                                                         |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




