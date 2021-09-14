---
description: 'Método IDelaydC::D isconnect: el método Disconnect desconecta el NPP de la red.'
ms.assetid: 476bbce4-2e3c-448f-b85e-6adac424fb0d
title: Método IDelaydC::D isconnect (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 967bd9674cb28363804b8c8af12c541bcb8675ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074141"
---
# <a name="idelaydcdisconnect-method"></a>IDelaydC::D isconnect (método)

El **método Disconnect** desconecta el NPP de la red.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.

Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:



| Código devuelto                                                                                          | Descripción                                                                                                       |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**CAPTURA DE \_ NMERR**</dt> </dl>      | El NPP captura datos. No se puede desconectar el NPP de la red durante una captura.<br/>            |
| <dl> <dt>**NMERR \_ NO \_ CONECTADO**</dt> </dl> | El NPP no está conectado a la red.<br/>                                                               |
| <dl> <dt>**NMERR \_ NO \_ RETRASADA**</dt> </dl>   | El NPP está conectado a la red, pero no con [el método IDelaydC::Conectar.](idelaydc-connect.md)<br/> |



 

## <a name="remarks"></a>Observaciones

No se puede llamar a este método cuando el NPP captura datos. Debe llamar al método **IDelaydC::Stop** antes de llamar a **Disconnect**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                     |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IDelaydC](idelaydc.md)
</dt> <dt>

[IDelaydC::Conectar](idelaydc-connect.md)
</dt> <dt>

[IDelaydC::Stop](idelaydc-stop.md)
</dt> </dl>

 

 




