---
title: Método IVMVirtualPC GetConfigurationValue (VPCCOMInterfaces.h)
description: Recupera el valor de la opción de configuración especificada.
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- Método GetConfigurationValue de Virtual PC
- Método GetConfigurationValue virtual PC , interfaz IVMVirtualPC
- IVMVirtualPC interface Virtual PC , Método GetConfigurationValue
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
ms.openlocfilehash: a483211353474f3328fc4e5da3b80ecf3fbbece53bc306e546f85543ac9027e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591866"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a>IVMVirtualPC::GetConfigurationValue (método)

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

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

*preferenceKey* \[ En\]
</dt> <dd>

Clave usada para identificar la preferencia, tal como se almacena en el archivo de configuración.

</dd> <dt>

*preferenceValue* \[ out, retval\]
</dt> <dd>

Valor de preferencia. Este parámetro puede ser uno de los siguientes tipos **VARIANT:** **VT \_ ARRAY** \| **VT \_ UI1** (bytes sin procesar), **VT \_ BSTR** (cadena), **VT \_ I4** (entero) o **VT \_ BOOL** (booleano).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código o valor devuelto                                                                                                                                                                        | Descripción                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0</dt> </dl>                                              | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>**E \_ Puntero**</dt> <dt>0x80004003</dt> </dl>                                | El *parámetro preferenceKey* o *preferenceValue* es **NULL.**<br/>                      |
| <dl> <dt>**Máquina virtual \_ NO \_ SE ENCONTRÓ \_ E \_ PREF**</dt> <dt>0xa0040300</dt> </dl>                   | No se encontró la preferencia.<br/>                                                        |
| <dl> <dt>**Máquina virtual \_ E \_ HARDWARE VIRTUALIZATION DISABLED \_ \_ 0xA0040951**</dt> <dt></dt> </dl> | El procesador no admite extensiones de Virtualización acelerada por hardware (HAV).<br/> |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                        | Se produjo un error inesperado.<br/>                                                    |



 

## <a name="remarks"></a>Comentarios

Este método proporciona acceso de bajo nivel a cualquier valor de preferencia para el usuario actual. Se puede usar para recuperar los valores de preferencia de las claves definidas por el cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMVirtualPC se define como \_ 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

