---
title: Propiedad TerminalServerPort de IVMGuestOS
description: Puerto usado por Servicios de Escritorio remoto en el sistema operativo invitado.
ms.assetid: 25a9114a-0992-4a9d-997a-37138d389970
keywords:
- Propiedad TerminalServerPort Virtual PC
- Propiedad TerminalServerPort Virtual PC, interfaz IVMGuestOS
- Interfaz IVMGuestOS Virtual PC, propiedad TerminalServerPort
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
ms.openlocfilehash: e64415057eeeb91bfb85b664f5cbb44a66546005
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150998"
---
# <a name="ivmguestosterminalserverport-property"></a>IVMGuestOS:: TerminalServerPort (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Puerto usado por Servicios de Escritorio remoto (anteriormente conocido como Terminal Services) en el sistema operativo invitado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_TerminalServerPort(
  [out, retval] long *tsPort = 3389
);
```



## <a name="property-value"></a>Valor de propiedad

Devuelve el puerto utilizado por Servicios de Escritorio remoto en el sistema operativo invitado.



| Value                                                                              | Significado                                       |
|------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>3389</dt> </dl>    | Valor predeterminado<br/>                      |
| <dl> <dt>1 65535</dt> </dl> | Intervalo válido<br/>                        |
| <dl> <dt>0</dt> </dl>       | El valor de Puerto válido no está disponible.<br/> |



 

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                       | Significado                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                          | La operación se realizó correctamente.<br/>                                                 |
| <dl> <dt>S \_ FALSO</dt> <dt>1</dt> </dl>                                       | Servicios de Escritorio remoto aún no se ha inicializado en el sistema operativo invitado.<br/> |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                            | El parámetro *tsPort* es **null**.<br/>                                           |
| <dl> <dt>Máquina virtual \_ La \_ VM E \_ no \_ ejecuta</dt> <dt>0xA0040206</dt> </dl>               | La máquina virtual no se está ejecutando.<br/>                                           |
| <dl> <dt>Máquina virtual \_ La característica de E/s \_ \_ no está \_ \_ disponible</dt> <dt>0xA0040505</dt> </dl> | Los componentes de integración no están instalados en esta máquina virtual.<br/>             |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                    | Se produjo un error inesperado.<br/>                                             |



## <a name="remarks"></a>Observaciones

El valor de esta propiedad no es válido a menos que la propiedad [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) sea una **variante \_ verdadera**.

Si la propiedad [**TerminalServicesInitialized**](ivmguestos-terminalservicesinitialized.md) es una **variante \_ falsa** debido a un error de conexión en el puerto, el valor devuelto por la propiedad **TerminalServerPort** contiene el valor de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                 |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                      |
| IDL<br/>                      | <dl> <dt>IVMGuestOS. idl</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS se define como 99fea0db-4880-499A-b6d8-73dff9bc91be<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

