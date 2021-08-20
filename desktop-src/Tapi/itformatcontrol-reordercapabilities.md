---
description: El método ReOrderCapabilities establece un nuevo orden para las funcionalidades de formato.
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: Método ITFormatControl::ReOrderCapabilities (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f1a105a659b89305a4f89bd7d647556e8d38d3e4320167cac9de1c0c3b68d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945061"
---
# <a name="itformatcontrolreordercapabilities-method"></a>ItFormatControl::ReOrderCapabilities (método)

\[Este método no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método ReOrderCapabilities** establece un nuevo orden para las funcionalidades de formato.

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

*pdwIndices* \[ En\]
</dt> <dd>

Índice del formato que se va a reordenar.

</dd> <dt>

*pfEnabled* \[ En\]
</dt> <dd>

Indica si el formato debe habilitarse o deshabilitarse.

</dd> <dt>

*pfPublicize* \[ En\]
</dt> <dd>

Indica si el formato debe estar disponible.

</dd> <dt>

*dwNumIndices* \[ En\]
</dt> <dd>

Nuevo número de índice para el formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="remarks"></a>Comentarios

Se [**debe llamar al método GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) antes de usar este método.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.1<br/>                                                         |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITFormatControl**](itformatcontrol.md)
</dt> <dt>

[**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




