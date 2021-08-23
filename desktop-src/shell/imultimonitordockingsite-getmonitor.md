---
description: Obtiene el monitor predeterminado actual.
title: IMultiMonitorDockingSite::GetMonitor (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.GetMonitor
api_type:
- COM
api_location: ''
ms.assetid: 0bae75eb-ebd5-4de4-9249-0e9bb489f61f
ms.openlocfilehash: 63609dc545e8f69ae2023e6659158297a65fdb7b549071126702b163c04555f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661895"
---
# <a name="imultimonitordockingsitegetmonitor-method"></a>IMultiMonitorDockingSite::GetMonitor (método)

Obtiene el monitor predeterminado actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMonitor(
  [in]  IUnknown *punkSrc,
  [out] HMONITOR *phMon
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*yerbaSrc* \[ En\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntero al objeto que implementa la [**interfaz IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para la que se solicita el monitor.

</dd> <dt>

*phMon* \[ out\]
</dt> <dd>

Tipo: **HMONITOR \***

Cuando la función vuelve, contiene un puntero al identificador del monitor predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                   |



 

 
