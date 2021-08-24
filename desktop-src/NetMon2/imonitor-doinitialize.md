---
description: El monitor debe implementar el método DoInitialize. MCSVC llama a este método para obtener un filtro de captura inmediatamente antes de llamar al método IRTCConnect de NPP.
ms.assetid: 5e43be75-21b3-4f37-ad53-3ffdd55f56a1
title: Método IMonitorDoInitialize (Netmon.h)
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
ms.openlocfilehash: 013a1604c1cbc709f35ac23378bab008d6c67f9053c171190b20669106303f37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779185"
---
# <a name="imonitordoinitialize-method"></a>IMonitor::D oInitialize (método)

El monitor debe implementar el método **DoInitialize.** MCSVC llama a este método para obtener un filtro de captura inmediatamente antes de llamar al [método IRTC::Conectar del NPP.](irtc-connect.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DoInitialize(
  [in]      IUnknown *pUnkMonitorCtrl,
  [in, out] HBLOB    hNPPBlob
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUnkMonitorCtrl* \[ En\]
</dt> <dd>

Puntero [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) pasado por MCSVC. Para obtener una interfaz de control de monitor compatible, el monitor debe llamar a [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero.

</dd> <dt>

*hNPPBlob* \[ in, out\]
</dt> <dd>

En la entrada, identificador de un blob de NPP.

En la salida, un blob de NPP que contiene un filtro de captura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es S \_ OK (que es igual que NOERROR).

Si el método no es correcto, el valor devuelto es un código de error. En caso de error, MCSVC no creará el monitor ni llamará a [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) en el puntero de interfaz.

## <a name="remarks"></a>Comentarios

MCSVC llama al método **DoInitialize** para realizar cualquier inicialización de monitor necesaria.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

