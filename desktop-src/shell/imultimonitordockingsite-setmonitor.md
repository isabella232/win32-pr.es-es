---
description: Cambios que se usan para las barras de herramientas acopladas en un sistema de varios monitores.
title: IMultiMonitorDockingSite::SetMonitor (Método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite.SetMonitor
api_type:
- COM
api_location: ''
ms.assetid: ba4ace13-7096-4f05-bcb0-ab37f1632406
ms.openlocfilehash: be773ee68c214f6a2fab8da89f1f48b867e71239
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574552"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>IMultiMonitorDockingSite::SetMonitor (Método)

Cambios que se usan para las barras de herramientas acopladas en un sistema de varios monitores.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMonitor(
  [in]  IUnknown *punkSrc,
  [in]  HMONITOR hMonNew,
  [out] HMONITOR *phMonOld
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*después de la 1:00* \[ En\]
</dt> <dd>

Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Puntero al objeto que implementa la [**interfaz IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para la que se modifica el monitor.

</dd> <dt>

*hMonNew* \[ En\]
</dt> <dd>

Tipo: **HMONITOR**

Identificador del monitor que reemplaza al monitor predeterminado existente.

</dd> <dt>

*phMonOld* \[ out\]
</dt> <dd>

Tipo: **HMONITOR \***

Cuando esta función vuelve, contiene un puntero al identificador del monitor predeterminado anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows solo aplicaciones \[ de escritorio XP\]<br/> |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                   |



 

 
