---
title: Método IVMVirtualPC RemoveConfigurationValue (VPCCOMInterfaces.h)
description: Quita el valor de la configuración especificada.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- RemoveConfigurationValue, método Virtual PC
- Método RemoveConfigurationValue de pc virtual, interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , RemoveConfigurationValue (método)
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 281837394967a15bce40173ead0ca02be66eb046bf7c15b63fdded57c2ecef84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998545"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a>IVMVirtualPC::RemoveConfigurationValue (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Quita el valor de la configuración especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*preferenceKey* \[ En\]
</dt> <dd>

Clave usada para identificar la preferencia, tal como se almacena en el archivo de configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                | El *parámetro preferenceKey* es **NULL.**<br/>                                           |
| <dl> <dt>**E \_ InvalidarG**</dt> <dt>0x80000003</dt> </dl>                             | El *parámetro preferenceKey* no es válido o es una cadena vacía.<br/>                    |
| <dl> <dt>**Máquina virtual \_ E \_ PREF \_ NOT \_ FOUND**</dt> <dt>0xA0040300</dt> </dl>                   | No se encontró la preferencia.<br/>                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ \_ VIRTUALIZACIÓN DE HARDWARE \_ DESHABILITADA**</dt> <dt>0xA0040951</dt> </dl> | El procesador no admite extensiones de virtualización acelerada de hardware (HAV).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Comentarios

Este método proporciona acceso de bajo nivel a cualquier valor de preferencia para el usuario actual. Se puede usar para quitar los valores de preferencia de las claves definidas por el cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

