---
title: Propiedad TerminalServerPort de IVMGuestOS
description: Puerto utilizado por Servicios de Escritorio remoto en el sistema operativo invitado.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- TerminalServerPort, propiedad Virtual PC
- TerminalServerPort, propiedad Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Pc virtual, propiedad TerminalServerPort
topic_type:
- apiref
api_name:
- IVMGuestOS.TerminalServerPort
- IVMGuestOS.get_TerminalServerPort
api_location:
- IVMGuestOS.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5b9eea5c545613f05dbd828a9436175fab6bfc5a05ba2fe5f59588f78da913
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512165"
---
# <a name="ivmguestosterminalserverport-property"></a>IVMGuestOS::TerminalServerPort, propiedad

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Puerto utilizado por Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) en el sistema operativo invitado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a>Valor de propiedad

Devuelve el puerto utilizado por Servicios de Escritorio remoto en el sistema operativo invitado.



| Valor                                                                              | Significado                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>3389</dt> </dl>    | Valor predeterminado<br/>                      |
| <dl> <dt>1 65535</dt> </dl> | Intervalo válido<br/>                        |
| <dl> <dt>0</dt> </dl>       | El valor de puerto válido no está disponible.<br/> |



 

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                 |
| <dl> <dt>S \_ FALSE</dt> <dt>1</dt> </dl>                                       | Servicios de Escritorio remoto no se ha inicializado aún en el sistema operativo invitado.<br/> |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                            | El *parámetro tsPort* es **NULL.**<br/>                                           |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                                           |
| <dl> <dt>Máquina virtual \_ LA \_ CARACTERÍSTICA DE \_ ADICIONES \_ NO \_ ESTÁ</dt> DISPONIBLE <dt>0XA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/>             |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                             |



## <a name="remarks"></a>Comentarios

El valor de esta propiedad no es válido a menos que la propiedad [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) sea **VARIANT \_ TRUE.**

Si la [**propiedad TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) es **VARIANT \_ FALSE** debido a un error de conexión en el puerto, el valor devuelto por la propiedad **TerminalServerPort** contiene el valor de error.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                      |
| Idl<br/>                      | <dl> <dt>IVMGuestOS.idl</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS se define como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

