---
title: MsimtfIsWindowFiltered función)
description: La función MsimtfIsWindowFiltered comprueba si AIMM (Administrador de métodos de entrada activos) filtra la ventana especificada.
ms.assetid: 1f5e98f1-3626-4aa5-b2da-b6bc48d02184
keywords:
- MsimtfIsWindowFiltered función de servicios de texto
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
ms.openlocfilehash: 70ad9bd9fb61c546ec3e2f1d96d5fc9cf932613a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150858"
---
# <a name="msimtfiswindowfiltered-function"></a>MsimtfIsWindowFiltered función)

La función **MsimtfIsWindowFiltered** comprueba si AIMM (Administrador de métodos de entrada activos) filtra la ventana especificada.

## <a name="syntax"></a>Sintaxis


```C++
BOOL CALLBACK MsimtfIsWindowFiltered(
  _In_ HWND hwnd
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Identificador de ventana que se va a probar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                          | Descripción                                                               |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**REALES**</dt> </dl>  | Si esta ventana está filtrada por el administrador de métodos de entrada activo.<br/>     |
| <dl> <dt>**ES**</dt> </dl> | Si esta ventana no está filtrada por el administrador de métodos de entrada activo.<br/> |



 

## <a name="remarks"></a>Observaciones

Una ventana se puede filtrar por IActiveIMMApp:: FilterClientWindows.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Msimtf.dll</dt> </dl> |



 

 





