---
description: Comprueba que el monitor está activo y disponible.
title: IMultiMonitorDockingSite::RequestMonitor (Método)
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
ms.openlocfilehash: 7f219e5fd62fb4f85fd206501e6a53ac3927195a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579561"
---
# <a name="imultimonitordockingsiterequestmonitor-method"></a>IMultiMonitorDockingSite::RequestMonitor (Método)

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
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de \[ escritorio XP\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                   |



 

 
