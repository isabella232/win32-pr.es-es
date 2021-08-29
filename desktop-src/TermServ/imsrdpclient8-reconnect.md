---
title: Método IMsRdpClient8 Reconnect
description: Se vuelve a conectar a la sesión remota con el nuevo ancho y alto del escritorio.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Volver a conectar el método Servicios de Escritorio remoto
- Método reconnect Servicios de Escritorio remoto interfaz , IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto método , Reconnect
- Método reconnect Servicios de Escritorio remoto interfaz , IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto método , Reconnect
- Método reconnect Servicios de Escritorio remoto interfaz , IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto método , Reconnect
topic_type:
- apiref
api_name:
- IMsRdpClient8.Reconnect
- IMsRdpClient9.Reconnect
- IMsRdpClient10.Reconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c30c261d8387a98be5425cb1f8e60613fd1f9340a5414b7668f1c913317e25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990405"
---
# <a name="imsrdpclient8reconnect-method"></a>IMsRdpClient8::Reconnect (Método)

Se vuelve a conectar a la sesión remota con el nuevo ancho y alto del escritorio. El control ya debe estar conectado a una sesión remota para que este método se pueda realizar correctamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Reconnect(
  [in]          ULONG                  ulWidth,
  [in]          ULONG                  ulHeight,
  [out, retval] ControlReconnectStatus *pReconnectStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ulWidth* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Nuevo ancho de escritorio, en píxeles. Consulte la [**propiedad DesktopWidth**](imstscax-desktopwidth.md) para ver las restricciones de valor.

</dd> <dt>

*ulHeight* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Nuevo alto del escritorio, en píxeles. Consulte la [**propiedad DesktopHeight**](imstscax-desktopheight.md) para ver las restricciones de valor.

</dd> <dt>

*pReconnectStatus* \[ out, retval\]
</dt> <dd>

Tipo: **[ **ControlReconnectStatus**](controlreconnectstatus.md)\***

Puntero a una [**variable ControlReconnectStatus**](controlreconnectstatus.md) que recibe el estado de la operación de reconexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient8 se define como 4247E044-9271-43A9-BC49-E2AD9E855D62<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**ControlReconnectStatus**](controlreconnectstatus.md)
</dt> </dl>

 

 





