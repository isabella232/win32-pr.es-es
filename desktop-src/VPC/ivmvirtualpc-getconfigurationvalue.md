---
title: Método IVMVirtualPC GetConfigurationValue (VPCCOMInterfaces. h)
description: Recupera el valor de la opción de configuración especificada.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Método GetConfigurationValue Virtual PC
- Método GetConfigurationValue Virtual PC, interfaz IVMVirtualPC
- Interfaz IVMVirtualPC Virtual PC, método GetConfigurationValue
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150792"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a>IVMVirtualPC:: GetConfigurationValue (método)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera el valor de la opción de configuración especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*preferenceKey* \[ de\]
</dt> <dd>

Clave que se usa para identificar la preferencia, tal como se almacena en el archivo de configuración.

</dd> <dt>

*preferenceValue* \[ out, retval\]
</dt> <dd>

Valor de preferencia. Este parámetro puede ser uno de los siguientes tipos **Variant** : **VT \_ array** \| **VT \_ UI1** (bytes sin formato), **VT \_ BSTR** (String), **VT \_ I4** (integer) o **VT \_ bool** (Boolean).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Aceptar**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ PUNTERO**</dt> <dt>0x80004003</dt> </dl>                                | El parámetro *preferenceKey* o *preferenceValue* es **null**.<br/>                      |
| <dl> <dt>**Máquina virtual \_ E \_ Pref \_ not \_ found**</dt> <dt>0xa0040300</dt> </dl>                   | No se encontró la preferencia.<br/>                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ \_ virtualización de hardware \_ deshabilitada**</dt> <dt>0xA0040951</dt> </dl> | El procesador no es compatible con las extensiones de virtualización acelerada de hardware (haber).<br/> |
| <dl> <dt>**DISP \_ . E \_ excepción**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Observaciones

Este método proporciona acceso de bajo nivel a cualquier valor de preferencia para el usuario actual. Se puede usar para recuperar los valores de preferencia de las claves definidas por el cliente.

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

 

