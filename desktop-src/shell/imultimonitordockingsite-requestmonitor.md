---
description: Comprueba que el monitor está activo y disponible.
title: IMultiMonitorDockingSite::RequestMonitor (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.RequestMonitor
api_type:
- COM
api_location: ''
ms.assetid: 9aa6eb20-de39-41f7-a17e-183f4088f972
ms.openlocfilehash: 9e5eeb2b99455d81bae36f1c5f26ed38126122bb58a5b8964a47cfb205f71ce7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942905"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a>IMultiMonitorDockingSite::RequestMonitor (método)

Comprueba que el monitor está activo y disponible.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RequestMonitor(
  [in] IUnknown *punkSrc,
  [in] HMONITOR *phMon
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*yerbaSrc* \[ En\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntero al objeto que implementa la [**interfaz IDockingWindow.**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow)

</dd> <dt>

*phMon* \[ En\]
</dt> <dd>

Tipo: **HMONITOR \***

Puntero al identificador del monitor predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                   |



 

 
