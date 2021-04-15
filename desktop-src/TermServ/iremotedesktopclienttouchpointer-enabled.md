---
title: Propiedad IRemoteDesktopClientTouchPointer habilitada
description: Si la característica de puntero táctil está habilitada en el control de cliente del contenedor de la aplicación RDP.
ms.assetid: f1e2f2f2-1b96-4c5a-b0dd-fd57627c5ec3
ms.tgt_platform: multiple
keywords:
- Propiedad Enabled Servicios de Escritorio remoto
- Servicios de Escritorio remoto de propiedad habilitada, interfaz IRemoteDesktopClientTouchPointer
- Interfaz IRemoteDesktopClientTouchPointer Servicios de Escritorio remoto, propiedad Enabled
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
ms.openlocfilehash: cdd534a9f8ec77903f196bbdfa10e1823a18dff4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686062"
---
# <a name="iremotedesktopclienttouchpointerenabled-property"></a>IRemoteDesktopClientTouchPointer:: Enabled (propiedad)

Si la característica de puntero táctil está habilitada en el control de cliente del contenedor de la aplicación RDP.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Enabled(
  [in]          VARIANT_BOOL Enabled
);

HRESULT get_Enabled(
  [out, retval] VARIANT_BOOL *Enabled
);
```



## <a name="property-value"></a>Valor de propiedad

**true** si está habilitada la característica de puntero táctil; en caso contrario, **false**.

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

 

