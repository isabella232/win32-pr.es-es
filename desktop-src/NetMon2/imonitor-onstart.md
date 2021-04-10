---
description: El método OnStart es un método opcional que puede ser implementado por el monitor. MCSVC llama a este método para solicitar que el monitor inicie la captura.
ms.assetid: 992ee27e-aaba-4e65-989b-e3f0fbd542ea
title: 'IMonitor:: OnStart (método) (Netmon. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor.OnStart
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: ca9e5e17de1d6baf2c79cc0077c5e2036a2a6246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153849"
---
# <a name="imonitoronstart-method"></a>IMonitor:: OnStart (método)

El método **OnStart** es un método opcional que puede ser implementado por el monitor. MCSVC llama a este método para solicitar que el monitor inicie la captura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OnStart(
  [in] IUnknown *pUnkNPP
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pUnkNPP* \[ de\]
</dt> <dd>

Un puntero [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) a la interfaz [IRTC](irtc.md) . El monitor puede utilizar esta interfaz para obtener estadísticas que se pueden usar para determinar si se debe iniciar la captura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si el método se realiza correctamente, el valor devuelto es S \_ OK (que es igual que NoError). Cuando \_ se devuelve, el MCSVC llama al método [IRTC:: Start](irtc-start.md) .

Si el método no se realiza correctamente, el valor devuelto es un código de error. El MCSVC no iniciará la captura si se devuelve algún código de error.

## <a name="remarks"></a>Observaciones

El MCSVC llama a este método antes de que se llame al método [IRTC:: Start](irtc-start.md) del NPP para iniciar la captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IMonitor](imonitor.md)
</dt> <dt>

[Proveedores de paquetes de red](network-packet-providers.md)
</dt> </dl>

 

