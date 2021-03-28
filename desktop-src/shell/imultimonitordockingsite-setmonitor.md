---
description: Cambia el monitor que se usa para las barras de herramientas acopladas en un sistema de varios monitores.
title: 'IMultiMonitorDockingSite:: SetMonitor (método)'
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
ms.openlocfilehash: cc177316a850bbf5059cabf48362ab8d5cbe2466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997968"
---
# <a name="imultimonitordockingsitesetmonitor-method"></a>IMultiMonitorDockingSite:: SetMonitor (método)

Cambia el monitor que se usa para las barras de herramientas acopladas en un sistema de varios monitores.

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

*punkSrc* \[ de\]
</dt> <dd>

Tipo: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Puntero al objeto que implementa la interfaz [_ *IDockingWindow* *](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) para la que se está modificando el monitor.

</dd> <dt>

*hMonNew* \[ de\]
</dt> <dd>

Tipo: **HMONITOR**

Identificador del monitor que reemplaza el monitor predeterminado existente.

</dd> <dt>

*phMonOld* \[ enuncia\]
</dt> <dd>

Tipo: **HMONITOR \** _

Cuando esta función devuelve un valor, contiene un puntero al identificador del monitor predeterminado anterior.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/> |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                   |



 

 
