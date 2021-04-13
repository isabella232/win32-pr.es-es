---
title: IMsRdpClient8 método de reconexión
description: Vuelve a conectarse a la sesión remota con el nuevo ancho y alto del escritorio.
ms.assetid: A2C4101D-780A-4973-B87C-025D9140C4BC
ms.tgt_platform: multiple
keywords:
- Método de reconexión Servicios de Escritorio remoto
- Método de reconexión Servicios de Escritorio remoto, interfaz IMsRdpClient8
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto, método de reconexión
- Método de reconexión Servicios de Escritorio remoto, interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto, método de reconexión
- Método de reconexión Servicios de Escritorio remoto, interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto, método de reconexión
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
ms.openlocfilehash: d62072c56852af6be2965ce63aecf4634de87d11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535584"
---
# <a name="imsrdpclient8reconnect-method"></a>IMsRdpClient8:: reconnect (método)

Vuelve a conectarse a la sesión remota con el nuevo ancho y alto del escritorio. El control ya debe estar conectado a una sesión remota para que este método se ejecute correctamente.

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

*ulWidth* \[ de\]
</dt> <dd>

Tipo: **ULong**

Nuevo ancho del escritorio, en píxeles. Vea la propiedad [**DesktopWidth**](imstscax-desktopwidth.md) para conocer las restricciones de valor.

</dd> <dt>

*ulHeight* \[ de\]
</dt> <dd>

Tipo: **ULong**

El nuevo alto del escritorio, en píxeles. Vea la propiedad [**DesktopHeight**](imstscax-desktopheight.md) para conocer las restricciones de valor.

</dd> <dt>

*pReconnectStatus* \[ out, retval\]
</dt> <dd>

Tipo: **[**ControlReconnectStatus**](controlreconnectstatus.md) \** _

Un puntero a una variable [_ *ControlReconnectStatus* *](controlreconnectstatus.md) que recibe el estado de la operación de reconexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si este método se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

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

 

 





