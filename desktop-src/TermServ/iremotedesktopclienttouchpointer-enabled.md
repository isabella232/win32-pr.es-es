---
title: Propiedad IRemoteDesktopClientTouchPointer Enabled
description: Si la característica de puntero táctil está habilitada en el control de cliente del contenedor de aplicaciones RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Propiedades habilitadas Servicios de Escritorio remoto
- Propiedad habilitada Servicios de Escritorio remoto , interfaz IRemoteDesktopClientTouchPointer
- Interfaz IRemoteDesktopClientTouchPointer Servicios de Escritorio remoto propiedad , Enabled
topic_type:
- apiref
api_name:
- IRemoteDesktopClientTouchPointer.Enabled
- IRemoteDesktopClientTouchPointer.get_Enabled
- IRemoteDesktopClientTouchPointer.put_Enabled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ce04e38b41fce462973606f40f0099f010e6f4ab785900039e6771b0a9aaf4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124855"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>IRemoteDesktopClientTouchPointer::Enabled, propiedad

Si la característica de puntero táctil está habilitada en el control de cliente del contenedor de aplicaciones RDP.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a>Valor de propiedad

**True** si la característica de puntero táctil está habilitada; de lo contrario, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                      |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>              |
| IID<br/>                      | IID \_ IRemoteDesktopClientTouchPointer se define como 260EC22D-8CBC-44B5-9E88-2A37F6C93AE9<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IRemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer)
</dt> </dl>

 

