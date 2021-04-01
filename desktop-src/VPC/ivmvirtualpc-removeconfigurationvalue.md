---
title: Método IVMVirtualPC RemoveConfigurationValue (VPCCOMInterfaces. h)
description: Quita el valor de la opción de configuración especificada.
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- Método RemoveConfigurationValue Virtual PC
- Método RemoveConfigurationValue Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método RemoveConfigurationValue
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
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905484"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a>IVMVirtualPC:: RemoveConfigurationValue (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Quita el valor de la opción de configuración especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*preferenceKey* \[ de\]
</dt> <dd>

Clave que se usa para identificar la preferencia, tal como se almacena en el archivo de configuración.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                | El parámetro *preferenceKey* es **null**.<br/>                                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | El parámetro *preferenceKey* no es válido o es una cadena vacía.<br/>                    |
| <dl> <dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xA0040300</dt> </dl>                   | No se encontró la preferencia.<br/>                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl> | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Observaciones

Este método proporciona acceso de bajo nivel a cualquier valor de preferencia para el usuario actual. Se puede usar para quitar los valores de preferencia de las claves definidas por el cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC se define como 236ba0d9-a24a-4292-A132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

