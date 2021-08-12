---
title: Propiedad IsBeating de IVMGuestOS (VPCCOMInterfaces.h)
description: Determina si la máquina virtual tiene un latido.
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- IsBeating, propiedad Virtual PC
- Propiedad IsBeatbeating Pc virtual, interfaz IVMGuestOS
- IVMGuestOS interface Virtual PC , Propiedad IsBeating
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91598284d3765c5ff6de185ca0cf3b652036c226d80b0fe01a9944a9d7480b43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594185"
---
# <a name="ivmguestosisheartbeating-property"></a>Propiedad IVMGuestOS::IsBeating

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Determina si la máquina virtual tiene un latido.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a>Valor de propiedad

**VARIANT \_ TRUE si** se detecta un latido, **VARIANT FALSE \_ en** caso contrario.

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                              | Significado                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Ok</dt> <dt>0</dt> </dl>                                 | La operación se realizó correctamente.<br/>                                                                                                                         |
| <dl> <dt>E \_ Puntero</dt> <dt>0x80004003</dt> </dl>                   | El parámetro es **NULL.**<br/>                                                                                                                            |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ UNKNOWN</dt> <dt>0xA0040207</dt> </dl>           | La configuración es desconocida.<br/>                                                                                                                         |
| <dl> <dt>Máquina virtual \_ E \_ VM \_ NOT \_ RUNNING</dt> <dt>0xA0040206</dt> </dl>      | La máquina virtual debe ejecutarse para esta operación.<br/>                                                                                               |
| <dl> <dt>Máquina virtual \_ E \_ LAS \_ ADICIONES NO ESTÁN \_ DISPONIBLES</dt> <dt>0xA0040504</dt> </dl> | La máquina virtual no está totalmente arrancada, la característica de componentes de integración no está instalada o la versión instalada no admite esta característica.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>           | Se produjo un error inesperado.<br/>                                                                                                                     |



## <a name="remarks"></a>Observaciones

Cuando se instalan componentes de integración en el sistema operativo invitado, se envía un "tick" o latido normal desde la sesión de máquina virtual a Windows Virtual PC. Si el sistema operativo invitado está muy cargado, es posible que el equipo virtual reciba menos latidos de los esperados. Si no se detecta ningún latido, es posible que el sistema operativo invitado no responda o se bloquea.

De forma predeterminada, una máquina virtual genera diez tics de latido por minuto. Si no se detecta ningún tic de latido durante un minuto completo, Windows Virtual PC intentará reiniciar la sesión de la máquina virtual una vez cada diez segundos durante un máximo de dos minutos. Este comportamiento se controla mediante los siguientes valores de clave en el archivo de configuración de la sesión de la máquina virtual.



| Clave de configuración                                            | Valor predeterminado       | Descripción                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| integration/microsoft/heartbeat/time<br/>              | 60<br/> | La duración del bloque de tiempo utilizado para generar tics de latido, en segundos.<br/>                                             |
| integration/microsoft/heartbeat/rate<br/>              | 10<br/> | Número de tics generados en cada bloque de tiempo de latido.<br/>                                                                  |
| integration/microsoft/heartbeat/failure \_ interval<br/> | 10<br/> | Número de segundos entre los intentos de reinicio, una vez que no se reciben tics de latido dentro de un bloque de tiempo de latido específico.<br/> |
| integration/microsoft/heartbeat/failure \_ attempts<br/> | 12<br/> | Número de intentos de reinicio realizados.<br/>                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMGuestOS se define como \_ 99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

