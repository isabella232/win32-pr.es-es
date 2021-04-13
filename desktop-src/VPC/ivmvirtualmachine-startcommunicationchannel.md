---
title: Método IVMVirtualMachine StartCommunicationChannel (VPCCOMInterfaces. h)
description: Configura un canal de comunicación entre el host y el sistema operativo invitado.
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- Método StartCommunicationChannel Virtual PC
- Método StartCommunicationChannel Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, método StartCommunicationChannel
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492215"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a>IVMVirtualMachine:: StartCommunicationChannel (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Configura un canal de comunicación entre el host y el sistema operativo invitado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inHostEndpointType* \[ de\]
</dt> <dd>

Este parámetro debe ser **vmEndpoint \_ NamedPipe** (0).

</dd> <dt>

*inHostEndPointName* \[ de\]
</dt> <dd>

Nombre único de la canalización. Esta cadena debe tener el formato siguiente: " \\ \\ . \\ canalización \\ *pipename*". La parte *pipename* del nombre puede incluir cualquier carácter que no sea una barra diagonal inversa, incluidos los números y los caracteres especiales. Toda la cadena de nombre de canalización puede tener una longitud de hasta 256 caracteres. Los nombres de canalización no distinguen mayúsculas de minúsculas.

</dd> <dt>

*inGuestEndpointType* \[ de\]
</dt> <dd>

Este parámetro debe ser **vmEndpoint \_ TCPIP** (1).

</dd> <dt>

*inGuestEndpointName* \[ de\]
</dt> <dd>

Número de puerto en el que escucha el servidor TCP en el invitado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                                  | Descripción                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                                        | La operación se realizó correctamente.<br/>                                                                                                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                       | El parámetro *inHostEndpointType* no es **vmEndpoint \_ NamedPipe** (0) o el parámetro *inGuestEndpointType* no es **vmEndpoint \_ TCPIP** (1).<br/> |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                          | El parámetro *inHostEndPointName* o *inGuestEndpointName* es **null** o no es un valor válido.<br/>                                                    |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                                  | Se produjo un error inesperado.<br/>                                                                                                                |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ identificador no válido)**</dt> <dt>0x80070006</dt> </dl>        | Un identificador no es válido.<br/>                                                                                                                           |
| <dl> <dt>**HRESULT \_ DE \_ Win32 (error \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>            | No hay suficiente memoria disponible para completar esta solicitud.<br/>                                                                                   |
| <dl> <dt>**HRESULT \_ DESDE \_ Win32 (error \_ no \_ preparado)**</dt> <dt>0x80070015</dt> </dl>             | El sistema subyacente que usa para proporcionar servicios de red se está inicializando actualmente.<br/>                                                        |
| <dl> <dt>**HRESULT \_ DESDE \_ Win32 (error \_ ya \_ existe)**</dt> <dt>0x800700b7</dt> </dl>        | El nombre de la canalización ya está en uso.<br/>                                                                                                                 |
| <dl> <dt>**HRESULT \_ De \_ Win32 ( \_ canalización de errores \_ ocupado)**</dt> <dt>0x800700e7</dt> </dl>             | Uno o más canales se están ejecutando y pueden estar disponibles en breve.<br/>                                                                          |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ máximo de \_ sesiones \_ alcanzadas)**</dt> <dt>0x80070161</dt> </dl> | El número máximo de canales de comunicación disponible está en uso. No se puede iniciar otro canal en este momento.<br/>                              |
| <dl> <dt>**HRESULT \_ Desde \_ Win32 (error \_ de \_ coincidencia de revisión)**</dt> <dt>0x8007051a</dt> </dl>     | Hay una discrepancia entre la versión del host y los subsistemas invitados. Vea el registro de eventos de Windows para obtener más detalles.<br/>                             |
| <dl> <dt>**Máquina virtual \_ La \_ VM E \_ no \_ ejecuta**</dt> <dt>0xA0040206</dt> </dl>                             | La máquina virtual no se está ejecutando.<br/>                                                                                                                           |



 

## <a name="remarks"></a>Observaciones

La implementación actual solo admite la interfaz de canalización con nombre en el host y la interfaz TCP/IP en el sistema operativo invitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**VMEndpointType**](vmendpointtype.md)
</dt> </dl>

 

