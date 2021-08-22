---
title: Función MsimtfIsWindowFiltered
description: La función MsimtfIsWindowFiltered comprueba si AIMM (Administrador de métodos de entrada activo) filtra la ventana determinada.
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- Función MsimtfIsWindowFiltered Text Services Framework
topic_type:
- apiref
api_name:
- MsimtfIsWindowFiltered
api_location:
- msimtf.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06f3841ed5c0436d991d02291c1e395f42d6b31b66f442a3caac0b2062fc27db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119476755"
---
# <a name="msimtfiswindowfiltered-function"></a>Función MsimtfIsWindowFiltered

La **función MsimtfIsWindowFiltered** comprueba si AIMM (Administrador de métodos de entrada activo) filtra la ventana determinada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hwnd* \[ En\]
</dt> <dd>

Identificador de ventana que se va a probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                          | Descripción                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**Verdad**</dt> </dl>  | Si el Administrador de métodos de entrada activo filtra esta ventana.<br/>     |
| <dl> <dt>**Falso**</dt> </dl> | Si el Administrador de métodos de entrada activo no filtra esta ventana.<br/> |



 

## <a name="remarks"></a>Observaciones

IActiveIMMApp::FilterClientWindows puede filtrar una ventana.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





