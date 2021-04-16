---
description: El monitor debe implementar el método de la función de inicialización. MCSVC llama a este método para obtener un filtro de captura inmediatamente antes de llamar al método IRTCConnect de NPPs.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Método IMonitorDoInitialize (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.DoInitialize
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 93133ce8204e49d080f87635ad6952685f2ba82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540179"
---
# <a name="imonitordoinitialize-method"></a>IMonitor::D método oInitialize

El monitor debe implementar el método de la función de **inicialización** . MCSVC llama a este método para obtener un filtro de captura inmediatamente antes de llamar al método [IRTC:: Connect](irtc-connect.md) de NPP.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUnkMonitorCtrl* \[ de\]
</dt> <dd>

Un puntero [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pasado por MCSVC. Para obtener una interfaz de control de supervisión compatible, el monitor debe llamar a [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero.

</dd> <dt>

*hNPPBlob* \[ in, out\]
</dt> <dd>

En la entrada, identificador de un BLOB NPP.

En la salida, un BLOB NPP que contiene un filtro de captura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError).

Si el método no se realiza correctamente, el valor devuelto es un código de error. Si se genera un error, MCSVC no creará el monitor o llamará a [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero de interfaz.

## <a name="remarks"></a>Observaciones

MCSVC llama al método **CoInitialize** para realizar cualquier inicialización del monitor necesaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

