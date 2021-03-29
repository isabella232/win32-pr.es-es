---
title: Propiedad IVMVirtualMachine ShutdownActionOnQuit (VPCCOMInterfaces. h)
description: Acción que se realizará en esta máquina virtual si se ejecuta cuando se cierra Windows Virtual PC.
ms.assetid: 3f6b256e-c48a-4a7c-acee-83d996e13ec7
keywords:
- Propiedad ShutdownActionOnQuit Virtual PC
- Propiedad ShutdownActionOnQuit Virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad ShutdownActionOnQuit
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ShutdownActionOnQuit
- IVMVirtualMachine.get_ShutdownActionOnQuit
- IVMVirtualMachine.put_ShutdownActionOnQuit
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01469e48e767777c6ea3daa4d0f3a923dce67726
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492221"
---
# <a name="ivmvirtualmachineshutdownactiononquit-property"></a>IVMVirtualMachine:: ShutdownActionOnQuit (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera y establece la acción que se realizará en esta máquina virtual (VM) si se ejecuta cuando se cierra Windows Virtual PC.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_ShutdownActionOnQuit(
  [in]          VMShutdownAction shutdownAction
);

HRESULT get_ShutdownActionOnQuit(
  [out, retval] VMShutdownAction *shutdownAction
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica cómo apagar la máquina virtual si se ejecuta cuando se cierra Windows Virtual PC. Para obtener una lista de valores, vea [**VMShutdownAction**](vmshutdownaction.md).

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                    | Significado                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                       | La operación se realizó correctamente.<br/>                                       |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>         | El parámetro es **null** o no es un valor válido.<br/>                     |
| <dl> <dt>E \_ ACCESSDENIED</dt> <dt>0x80070005</dt> </dl>    | El usuario actual no tiene acceso suficiente al archivo de configuración.<br/> |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl> | La configuración es desconocida.<br/>                                       |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl> | Se produjo un error inesperado.<br/>                                   |



## <a name="remarks"></a>Observaciones

De forma predeterminada, las máquinas virtuales en ejecución se guardan cuando se sale de Windows Virtual PC. La acción de apagado **vmShutdownAction \_ Save** (0) guardará el estado de la máquina virtual. La acción de desactivación de **vmShutdownAction \_** (1) desconectará la máquina virtual. La acción de **\_ cierre de vmShutdownAction** (2) apagará el sistema operativo invitado si los componentes de integración están disponibles y guardará la máquina virtual en caso contrario.

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

[**VMShutdownAction**](vmshutdownaction.md)
</dt> </dl>

 

